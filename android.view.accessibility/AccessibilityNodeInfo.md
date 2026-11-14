Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AccessibilityNodeInfo

```
open class AccessibilityNodeInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.accessibility.AccessibilityNodeInfo](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#) |

This class represents a node of the window content as well as actions that can be requested from its source. From the point of view of an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#` a window's content is presented as a tree of accessibility node infos, which may or may not map one-to-one to the view hierarchy. In other words, a custom view is free to report itself as a tree of accessibility node info.

<br />

Once an accessibility node info is delivered to an accessibility service it is made immutable and calling a state mutation method generates an error. See `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setQueryFromAppProcessEnabled(android.view.View,%20kotlin.Boolean)` if you would like to inspect the node tree from the app process for testing or debugging tools.

Please refer to `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#` for details about how to obtain a handle to window content as a tree of accessibility node info as well as details about the security model.

> [!NOTE]
>
> ### Developer Guides
>
> For more information about making applications accessible, read the [Accessibility](https://developer.android.com/guide/topics/ui/accessibility/index.html) developer guide.

**Note:** Use a androidx.core.view.accessibility.AccessibilityNodeInfoCompat wrapper instead of this class for backwards-compatibility.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction` A class defining an action that can be performed on an `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#`. |
| | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.CollectionInfo` Class with information if a node is a collection. |
| | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.CollectionItemInfo` Class with information if a node is a collection item. |
| --- | --- |
| | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.ExtraRenderingInfo` Class with information of a view useful to evaluate accessibility needs. |
| | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.MathInfo` A class that holds information about a node that represents a mathematical expression. |
| | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.RangeInfo` Class with information if a node is a range. |
| --- | --- |
| | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.Selection` Represents a selection of content that may extend across more than one `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#` instance. |
| | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.SelectionPosition` A class which defines either the start or end of a selection that can span across multiple AccessibilityNodeInfo objects. |
| abstract | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.StructuredDataInfo` An abstract base class for holding structured semantic information about a node. |
| --- | --- |
| | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.TouchDelegateInfo` Class with information of touch delegated views and regions from `https://developer.android.com/reference/kotlin/android/view/TouchDelegate.html#` for the `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#`. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_ACCESSIBILITY_FOCUS:kotlin.Int` Action that gives accessibility focus to the node. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_ARGUMENT_COLUMN_INT:kotlin.String` Argument for specifying the collection column to make visible on screen. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_ARGUMENT_DIRECTION_INT:kotlin.String` Argument to represent the direction when using `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_SCROLL_IN_DIRECTION:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction`. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_ARGUMENT_EXTEND_SELECTION_BOOLEAN:kotlin.String` Argument for whether when moving at granularity to extend the selection or to move it otherwise. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_ARGUMENT_HTML_ELEMENT_STRING:kotlin.String` Argument for which HTML element to get moving to the next/previous HTML element. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_ARGUMENT_MOVEMENT_GRANULARITY_INT:kotlin.String` Argument for which movement granularity to be used when traversing the node text. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_ARGUMENT_MOVE_WINDOW_X:kotlin.String` Argument for specifying the x coordinate to which to move a window. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_ARGUMENT_MOVE_WINDOW_Y:kotlin.String` Argument for specifying the y coordinate to which to move a window. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_ARGUMENT_PRESS_AND_HOLD_DURATION_MILLIS_INT:kotlin.String` Argument to represent the duration in milliseconds to press and hold a node. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_ARGUMENT_PROGRESS_VALUE:kotlin.String` Argument for specifying the progress value to set. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_ARGUMENT_ROW_INT:kotlin.String` Argument for specifying the collection row to make visible on screen. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_ARGUMENT_SCROLL_AMOUNT_FLOAT:kotlin.String` Argument to represent the scroll amount as a percent of the visible area of a node, with 1. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_ARGUMENT_SELECTION_END_INT:kotlin.String` Argument for specifying the selection end. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_ARGUMENT_SELECTION_PARCELABLE:kotlin.String` Argument for specifying the extended selection. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_ARGUMENT_SELECTION_START_INT:kotlin.String` Argument for specifying the selection start. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_ARGUMENT_SET_TEXT_CHARSEQUENCE:kotlin.String` Argument for specifying the text content to set. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_CLEAR_ACCESSIBILITY_FOCUS:kotlin.Int` Action that clears accessibility focus of the node. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_CLEAR_FOCUS:kotlin.Int` Action that clears input focus of the node. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_CLEAR_SELECTION:kotlin.Int` Action that deselects the node. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_CLICK:kotlin.Int` Action that clicks on the node info. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_COLLAPSE:kotlin.Int` Action to collapse an expandable node. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_COPY:kotlin.Int` Action to copy the current selection to the clipboard. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_CUT:kotlin.Int` Action to cut the current selection and place it to the clipboard. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_DISMISS:kotlin.Int` Action to dismiss a dismissable node. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_EXPAND:kotlin.Int` Action to expand an expandable node. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_FOCUS:kotlin.Int` Action that gives input focus to the node. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_LONG_CLICK:kotlin.Int` Action that long clicks on the node. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_NEXT_AT_MOVEMENT_GRANULARITY:kotlin.Int` Action that requests to go to the next entity in this node's text at a given movement granularity. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_NEXT_HTML_ELEMENT:kotlin.Int` Action to move to the next HTML element of a given type. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_PASTE:kotlin.Int` Action to paste the current clipboard content. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_PREVIOUS_AT_MOVEMENT_GRANULARITY:kotlin.Int` Action that requests to go to the previous entity in this node's text at a given movement granularity. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_PREVIOUS_HTML_ELEMENT:kotlin.Int` Action to move to the previous HTML element of a given type. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_SCROLL_BACKWARD:kotlin.Int` Action to scroll the node content backward. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_SCROLL_FORWARD:kotlin.Int` Action to scroll the node content forward. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_SELECT:kotlin.Int` Action that selects the node. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_SET_SELECTION:kotlin.Int` Action to set the selection. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_SET_TEXT:kotlin.Int` Action that sets the text of the node. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#CHECKED_STATE_FALSE:kotlin.Int` This node is not checked. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#CHECKED_STATE_PARTIAL:kotlin.Int` This node is partially checked. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#CHECKED_STATE_TRUE:kotlin.Int` This node is checked. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#EXPANDED_STATE_COLLAPSED:kotlin.Int` Expanded state for a collapsed expandable element. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#EXPANDED_STATE_FULL:kotlin.Int` Expanded state for a expanded expandable element that cannot be expanded further. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#EXPANDED_STATE_PARTIAL:kotlin.Int` Expanded state for an expanded expandable element that can still be expanded further. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#EXPANDED_STATE_UNDEFINED:kotlin.Int` Expanded state for a non-expandable element |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#EXTRA_DATA_RENDERING_INFO_KEY:kotlin.String` Key used to request extra data for the rendering information. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#EXTRA_DATA_REQUEST_LAYOUT_BASED_ACTIONS_KEY:kotlin.String` Key used to request that the node source re-evaluate and update this node's layout-dependent actions. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#EXTRA_DATA_TEXT_CHARACTER_LOCATION_ARG_LENGTH:kotlin.String` Integer argument specifying the end index of the requested text location data. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#EXTRA_DATA_TEXT_CHARACTER_LOCATION_ARG_MAX_LENGTH:kotlin.Int` The maximum allowed length of the requested text location data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#EXTRA_DATA_TEXT_CHARACTER_LOCATION_ARG_START_INDEX:kotlin.String` Integer argument specifying the start index of the requested text location data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#EXTRA_DATA_TEXT_CHARACTER_LOCATION_IN_WINDOW_KEY:kotlin.String` Key used to request and locate extra data for text character location in window coordinates. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#EXTRA_DATA_TEXT_CHARACTER_LOCATION_KEY:kotlin.String` Key used to request and locate extra data for text character location. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#FLAG_PREFETCH_ANCESTORS:kotlin.Int` Prefetching strategy that prefetches the ancestors of the requested node. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#FLAG_PREFETCH_DESCENDANTS_BREADTH_FIRST:kotlin.Int` Prefetching strategy that prefetches the descendants of the requested node breadth-first. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#FLAG_PREFETCH_DESCENDANTS_DEPTH_FIRST:kotlin.Int` Prefetching strategy that prefetches the descendants of the requested node depth-first. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#FLAG_PREFETCH_DESCENDANTS_HYBRID:kotlin.Int` Prefetching strategy that prefetches the descendants in a hybrid depth first and breadth first approach. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#FLAG_PREFETCH_SIBLINGS:kotlin.Int` Prefetching strategy that prefetches the siblings of the requested node. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#FLAG_PREFETCH_UNINTERRUPTIBLE:kotlin.Int` Prefetching flag that specifies prefetching should not be interrupted by a request to retrieve a node or perform an action on a node. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#FOCUS_ACCESSIBILITY:kotlin.Int` The accessibility focus. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#FOCUS_INPUT:kotlin.Int` The input focus. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#MAX_NUMBER_OF_PREFETCHED_NODES:kotlin.Int` Maximum batch size of prefetched nodes for a request. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#MOVEMENT_GRANULARITY_CHARACTER:kotlin.Int` Movement granularity bit for traversing the text of a node by character. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#MOVEMENT_GRANULARITY_LINE:kotlin.Int` Movement granularity bit for traversing the text of a node by line. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#MOVEMENT_GRANULARITY_PAGE:kotlin.Int` Movement granularity bit for traversing the text of a node by page. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#MOVEMENT_GRANULARITY_PARAGRAPH:kotlin.Int` Movement granularity bit for traversing the text of a node by paragraph. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#MOVEMENT_GRANULARITY_WORD:kotlin.Int` Movement granularity bit for traversing the text of a node by word. |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#AccessibilityNodeInfo()()` Creates a new `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#`. |
| `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#AccessibilityNodeInfo(android.view.accessibility.AccessibilityNodeInfo)(info: https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#)` Copy constructor. |
| `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#AccessibilityNodeInfo(android.view.View)(source: https://developer.android.com/reference/kotlin/android/view/View.html#)` Creates a new `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#` with the given `source`. |
| `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#AccessibilityNodeInfo(android.view.View,%20kotlin.Int)(root: https://developer.android.com/reference/kotlin/android/view/View.html#, virtualDescendantId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Creates a new `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#` with the given `source`. |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#addAction(android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction)(action: https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction!)` Adds an action that can be performed on the node. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#addAction(kotlin.Int)(action: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Adds an action that can be performed on the node. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#addChild(android.view.View)(child: https://developer.android.com/reference/kotlin/android/view/View.html#!)` Adds a child. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#addChild(android.view.View,%20kotlin.Int)(root: https://developer.android.com/reference/kotlin/android/view/View.html#!, virtualDescendantId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Adds a virtual child which is a descendant of the given `root`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#addLabeledBy(android.view.View)(label: https://developer.android.com/reference/kotlin/android/view/View.html#)` Adds the view which serves as the label of the view represented by this info for accessibility purposes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#addLabeledBy(android.view.View,%20kotlin.Int)(root: https://developer.android.com/reference/kotlin/android/view/View.html#, virtualDescendantId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Adds the view which serves as the label of the view represented by this info for accessibility purposes. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#canOpenPopup()()` Gets if this node opens a popup or a dialog. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| --- | --- |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [AccessibilityNodeInfo](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#)!\>! | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#findAccessibilityNodeInfosByText(kotlin.String)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Finds `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#`s by text. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [AccessibilityNodeInfo](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#)!\>! | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#findAccessibilityNodeInfosByViewId(kotlin.String)(viewId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Finds `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#`s by the fully qualified view id's resource name where a fully qualified id is of the from "package:id/id_resource_name". |
| open [AccessibilityNodeInfo](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#)! | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#findFocus(kotlin.Int)(focus: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Find the view that has the specified focus type. |
| --- | --- |
| open [AccessibilityNodeInfo](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#)! | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#focusSearch(kotlin.Int)(direction: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Searches for the nearest view in the specified direction that can take the input focus. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [AccessibilityNodeInfo.AccessibilityAction](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction)!\>! | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getActionList()()` Gets the actions that can be performed on the node. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getActions()()` Gets the actions that can be performed on the node. |
| --- | --- |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getAvailableExtraData()()` Get the extra data available for this node. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getBoundsInParent(android.graphics.Rect)(outBounds: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#!)` Gets the node bounds in the viewParent's coordinates. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getBoundsInScreen(android.graphics.Rect)(outBounds: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#!)` Gets the node bounds in screen coordinates. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getBoundsInWindow(android.graphics.Rect)(outBounds: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)` Gets the node bounds in window coordinates. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getChecked()()` Gets the checked state of this node. |
| open [AccessibilityNodeInfo](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#)! | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getChild(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Get the child at given index. |
| --- | --- |
| open [AccessibilityNodeInfo](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#)? | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getChild(kotlin.Int,%20kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, prefetchingStrategy: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Get the child at given index. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getChildCount()()` Gets the number of children. |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getClassName()()` Gets the class this node comes from. |
| --- | --- |
| open [AccessibilityNodeInfo.CollectionInfo](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.CollectionInfo)! | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getCollectionInfo()()` Gets the collection info if the node is a collection. |
| open [AccessibilityNodeInfo.CollectionItemInfo](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.CollectionItemInfo)! | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getCollectionItemInfo()()` Gets the collection item info if the node is a collection item. |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getContainerTitle()()` Returns the container title. |
| --- | --- |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getContentDescription()()` Gets the content description of this node. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getDrawingOrder()()` Get the drawing order of the view corresponding it this node. |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getError()()` Gets the error text of this node. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getExpandedState()()` Gets the expanded state for this node. |
| open [AccessibilityNodeInfo.ExtraRenderingInfo](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.ExtraRenderingInfo)? | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getExtraRenderingInfo()()` Gets the `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.ExtraRenderingInfo` if the node is meant to be refreshed with extra data to examine rendering related accessibility issues. |
| open [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)! | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getExtras()()` Gets an optional bundle with extra data. |
| --- | --- |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getHintText()()` Gets the hint text of this node. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getInputType()()` Gets the input type of the source as defined by `https://developer.android.com/reference/kotlin/android/text/InputType.html#`. |
| open [AccessibilityNodeInfo](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#)! | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getLabelFor()()` Gets the node info for which the view represented by this info serves as a label for accessibility purposes. |
| --- | --- |
| open [AccessibilityNodeInfo](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#)! | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getLabeledBy()()` Gets the node info which serves as the label of the view represented by this info for accessibility purposes. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [AccessibilityNodeInfo](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#)!\> | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getLabeledByList()()` Gets the list of node infos which serve as the labels of the view represented by this info for accessibility purposes. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getLiveRegion()()` Gets the node's live region mode. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getMaxTextLength()()` Returns the maximum text length for this node. |
| open [Duration](https://developer.android.com/reference/kotlin/java/time/Duration.html#) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getMinDurationBetweenContentChanges()()` Gets the minimum time duration between two content change events. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getMovementGranularities()()` Gets the movement granularities for traversing the text of this node. |
| --- | --- |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getPackageName()()` Gets the package this node comes from. |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getPaneTitle()()` Get the title of the pane represented by this node. |
| open [AccessibilityNodeInfo](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#)! | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getParent()()` Gets the parent. |
| --- | --- |
| open [AccessibilityNodeInfo](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#)? | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getParent(kotlin.Int)(prefetchingStrategy: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Gets the parent. |
| open [AccessibilityNodeInfo.RangeInfo](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.RangeInfo)! | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getRangeInfo()()` Gets the range info if this node is a range. |
| open [AccessibilityNodeInfo.Selection](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.Selection)? | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getSelection()()` Gets the extended selection, which is a representation of selection that spans multiple nodes that exist within the subtree of the node defining selection. |
| --- | --- |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getStateDescription()()` Get the state description of this node. |
| open [AccessibilityNodeInfo.StructuredDataInfo](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.StructuredDataInfo)? | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getStructuredDataInfo()()` Gets additional structured data properties of this node. |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getSupplementalDescription()()` Gets the supplemental description of this node. |
| --- | --- |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getText()()` Gets the text of this node. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getTextSelectionEnd()()` Gets the text selection end if text is selected. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getTextSelectionStart()()` Gets the text selection start or the cursor position. |
| --- | --- |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getTooltipText()()` Gets the tooltip text of this node. |
| open [AccessibilityNodeInfo.TouchDelegateInfo](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.TouchDelegateInfo)? | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getTouchDelegateInfo()()` Get the `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.TouchDelegateInfo` for touch delegate behavior with the represented view. |
| open [AccessibilityNodeInfo](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#)! | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getTraversalAfter()()` Gets the node after which this one is visited in accessibility traversal. |
| --- | --- |
| open [AccessibilityNodeInfo](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#)! | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getTraversalBefore()()` Gets the node before which this one is visited during traversal. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getUniqueId()()` Gets the unique id of the node. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getViewIdResourceName()()` Gets the fully qualified resource name of the source view's id. |
| --- | --- |
| open [AccessibilityWindowInfo](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo)! | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getWindow()()` Gets the window to which this node belongs. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getWindowId()()` Returns the id of the window that created this node. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#hasRequestInitialAccessibilityFocus()()` Gets whether the node has `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setRequestInitialAccessibilityFocus(kotlin.Boolean)`. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#hashCode()()` Returns a hash code value for the object. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#isAccessibilityDataSensitive()()` Gets if the node's accessibility data is considered sensitive. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#isAccessibilityFocused()()` Gets whether this node is accessibility focused. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#isCheckable()()` Gets whether this node is checkable. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#isChecked()()` Gets whether this node is checked. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#isClickable()()` Gets whether this node is clickable. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#isContentInvalid()()` Gets if the content of this node is invalid. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#isContextClickable()()` Gets whether this node is context clickable. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#isDismissable()()` Gets if the node can be dismissed. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#isEditable()()` Gets if the node is editable. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#isEnabled()()` Gets whether this node is enabled. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#isFieldRequired()()` Gets whether a node representing a form field requires input or selection. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#isFocusable()()` Gets whether this node is focusable. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#isFocused()()` Gets whether this node is focused. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#isGranularScrollingSupported()()` Gets if the node supports granular scrolling. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#isHeading()()` Returns whether node represents a heading. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#isImportantForAccessibility()()` Returns whether the node originates from a view considered important for accessibility. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#isLongClickable()()` Gets whether this node is long clickable. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#isMultiLine()()` Gets if the node is a multi line editable text. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#isPassword()()` Gets whether this node is a password. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#isScreenReaderFocusable()()` Returns whether the node is explicitly marked as a focusable unit by a screen reader. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#isScrollable()()` Gets if the node is scrollable. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#isSelected()()` Gets whether this node is selected. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#isShowingHintText()()` Returns whether the node's text represents a hint for the user to enter text. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#isTextEntryKey()()` Returns whether node represents a text entry key that is part of a keyboard or keypad. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#isTextSelectable()()` Gets if the node has selectable text. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#isVisibleToUser()()` Gets whether this node is visible to the user. |
| --- | --- |
| open static [AccessibilityNodeInfo](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#)! | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#obtain()()` Instantiates a new AccessibilityNodeInfo. |
| open static [AccessibilityNodeInfo](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#)! | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#obtain(android.view.accessibility.AccessibilityNodeInfo)(info: https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#!)` Instantiates a new AccessibilityNodeInfo initialized from the given `info`. |
| open static [AccessibilityNodeInfo](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#)! | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#obtain(android.view.View)(source: https://developer.android.com/reference/kotlin/android/view/View.html#!)` Returns a cached instance if such is available otherwise a new one and sets the source. |
| --- | --- |
| open static [AccessibilityNodeInfo](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#)! | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#obtain(android.view.View,%20kotlin.Int)(root: https://developer.android.com/reference/kotlin/android/view/View.html#!, virtualDescendantId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns a cached instance if such is available otherwise a new one and sets the source. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#performAction(kotlin.Int)(action: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Performs an action on the node. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#performAction(kotlin.Int,%20android.os.Bundle)(action: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, arguments: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!)` Performs an action on the node. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#recycle()()` Would previously return an instance back to be reused. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#refresh()()` Refreshes this info with the latest state of the view it represents. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#refreshWithExtraData(kotlin.String,%20android.os.Bundle)(extraDataKey: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, args: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!)` Refreshes this info with the latest state of the view it represents, and request new data be added by the View. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#removeAction(android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction)(action: https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction!)` Removes an action that can be performed on the node. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#removeAction(kotlin.Int)(action: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Removes an action that can be performed on the node. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#removeChild(android.view.View)(child: https://developer.android.com/reference/kotlin/android/view/View.html#!)` Removes a child. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#removeChild(android.view.View,%20kotlin.Int)(root: https://developer.android.com/reference/kotlin/android/view/View.html#!, virtualDescendantId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Removes a virtual child which is a descendant of the given `root`. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#removeLabeledBy(android.view.View)(label: https://developer.android.com/reference/kotlin/android/view/View.html#)` Removes a label. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#removeLabeledBy(android.view.View,%20kotlin.Int)(root: https://developer.android.com/reference/kotlin/android/view/View.html#, virtualDescendantId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Removes a label which is a virtual descendant of the given `root`. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setAccessibilityDataSensitive(kotlin.Boolean)(accessibilityDataSensitive: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets whether this node's accessibility data is considered sensitive. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setAccessibilityFocused(kotlin.Boolean)(focused: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets whether this node is accessibility focused. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setAvailableExtraData(kotlin.collections.MutableList)(extraDataKeys: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!)` Set the extra data available for this node. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setBoundsInParent(android.graphics.Rect)(bounds: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#!)` Sets the node bounds in the viewParent's coordinates. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setBoundsInScreen(android.graphics.Rect)(bounds: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#!)` Sets the node bounds in screen coordinates. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setBoundsInWindow(android.graphics.Rect)(bounds: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)` Sets the node bounds in window coordinates. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setCanOpenPopup(kotlin.Boolean)(opensPopup: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets if this node opens a popup or a dialog. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setCheckable(kotlin.Boolean)(checkable: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets whether this node is checkable. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setChecked(kotlin.Boolean)(checked: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets whether this node is checked. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setChecked(kotlin.Int)(checked: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the checked state of this node. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setClassName(kotlin.CharSequence)(className: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!)` Sets the class this node comes from. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setClickable(kotlin.Boolean)(clickable: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets whether this node is clickable. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setCollectionInfo(android.view.accessibility.AccessibilityNodeInfo.CollectionInfo)(collectionInfo: https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.CollectionInfo!)` Sets the collection info if the node is a collection. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setCollectionItemInfo(android.view.accessibility.AccessibilityNodeInfo.CollectionItemInfo)(collectionItemInfo: https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.CollectionItemInfo!)` Sets the collection item info if the node is a collection item. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setContainerTitle(kotlin.CharSequence)(containerTitle: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?)` Sets the container title for app-developer-defined container which can be any type of ViewGroup or layout. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setContentDescription(kotlin.CharSequence)(contentDescription: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!)` Sets the content description of this node. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setContentInvalid(kotlin.Boolean)(contentInvalid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets if the content of this node is invalid. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setContextClickable(kotlin.Boolean)(contextClickable: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets whether this node is context clickable. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setDismissable(kotlin.Boolean)(dismissable: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets if the node can be dismissed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setDrawingOrder(kotlin.Int)(drawingOrderInParent: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set the drawing order of the view corresponding it this node. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setEditable(kotlin.Boolean)(editable: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets whether this node is editable. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setEnabled(kotlin.Boolean)(enabled: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets whether this node is enabled. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setError(kotlin.CharSequence)(error: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!)` Sets the error text of this node. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setExpandedState(kotlin.Int)(state: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the expanded state of the node. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setExtraRenderingInfo(android.view.accessibility.AccessibilityNodeInfo.ExtraRenderingInfo)(extraRenderingInfo: https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.ExtraRenderingInfo?)` Sets the extra rendering info, `extraRenderingInfo, if the node is meant to be refreshed with extra data. ` `` Note: Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService. `` ` ` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setFieldRequired(kotlin.Boolean)(required: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets whether `this` node represents a form field that requires input or selection. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setFocusable(kotlin.Boolean)(focusable: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets whether this node is focusable. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setFocused(kotlin.Boolean)(focused: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets whether this node is focused. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setGranularScrollingSupported(kotlin.Boolean)(granularScrollingSupported: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets if the node supports granular scrolling. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setHeading(kotlin.Boolean)(isHeading: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets whether the node represents a heading. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setHintText(kotlin.CharSequence)(hintText: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!)` Sets the hint text of this node. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setImportantForAccessibility(kotlin.Boolean)(important: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets whether the node is considered important for accessibility. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setInputType(kotlin.Int)(inputType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the input type of the source as defined by `https://developer.android.com/reference/kotlin/android/text/InputType.html#`. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setLabelFor(android.view.View)(labeled: https://developer.android.com/reference/kotlin/android/view/View.html#!)` Sets the view for which the view represented by this info serves as a label for accessibility purposes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setLabelFor(android.view.View,%20kotlin.Int)(root: https://developer.android.com/reference/kotlin/android/view/View.html#!, virtualDescendantId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the view for which the view represented by this info serves as a label for accessibility purposes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setLabeledBy(android.view.View)(label: https://developer.android.com/reference/kotlin/android/view/View.html#!)` Sets the view which serves as the label of the view represented by this info for accessibility purposes. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setLabeledBy(android.view.View,%20kotlin.Int)(root: https://developer.android.com/reference/kotlin/android/view/View.html#!, virtualDescendantId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the view which serves as the label of the view represented by this info for accessibility purposes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setLiveRegion(kotlin.Int)(mode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the node's live region mode. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setLongClickable(kotlin.Boolean)(longClickable: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets whether this node is long clickable. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setMaxTextLength(kotlin.Int)(max: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the maximum text length, or -1 for no limit. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setMinDurationBetweenContentChanges(java.time.Duration)(duration: https://developer.android.com/reference/kotlin/java/time/Duration.html#)` Sets the minimum time duration between two content change events, which is used in throttling content change events in accessibility services. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setMovementGranularities(kotlin.Int)(granularities: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the movement granularities for traversing the text of this node. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setMultiLine(kotlin.Boolean)(multiLine: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets if the node is a multi line editable text. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setPackageName(kotlin.CharSequence)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!)` Sets the package this node comes from. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setPaneTitle(kotlin.CharSequence)(paneTitle: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?)` If this node represents a visually distinct region of the screen that may update separately from the rest of the window, it is considered a pane. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setParent(android.view.View)(parent: https://developer.android.com/reference/kotlin/android/view/View.html#!)` Sets the parent. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setParent(android.view.View,%20kotlin.Int)(root: https://developer.android.com/reference/kotlin/android/view/View.html#!, virtualDescendantId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the parent to be a virtual descendant of the given `root`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setPassword(kotlin.Boolean)(password: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets whether this node is a password. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setQueryFromAppProcessEnabled(android.view.View,%20kotlin.Boolean)(view: https://developer.android.com/reference/kotlin/android/view/View.html#, enabled: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Connects this node to the View's root so that operations on this node can query the entire `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#` tree and perform accessibility actions on nodes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setRangeInfo(android.view.accessibility.AccessibilityNodeInfo.RangeInfo)(rangeInfo: https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.RangeInfo!)` Sets the range info if this node is a range. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setRequestInitialAccessibilityFocus(kotlin.Boolean)(requestInitialAccessibilityFocus: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets whether the node has requested initial accessibility focus. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setScreenReaderFocusable(kotlin.Boolean)(screenReaderFocusable: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets whether the node should be considered a focusable unit by a screen reader. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setScrollable(kotlin.Boolean)(scrollable: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets if the node is scrollable. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setSelected(kotlin.Boolean)(selected: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets whether this node is selected. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setSelection(android.view.accessibility.AccessibilityNodeInfo.Selection)(selection: https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.Selection?)` Sets the extended selection, which is a representation of selection that spans multiple nodes that exist within the subtree of the node defining selection. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setShowingHintText(kotlin.Boolean)(showingHintText: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets whether the node's text represents a hint for the user to enter text. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setSource(android.view.View)(source: https://developer.android.com/reference/kotlin/android/view/View.html#!)` Sets the source. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setSource(android.view.View,%20kotlin.Int)(root: https://developer.android.com/reference/kotlin/android/view/View.html#!, virtualDescendantId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the source to be a virtual descendant of the given `root`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setStateDescription(kotlin.CharSequence)(stateDescription: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?)` Sets the state description of this node. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setStructuredDataInfo(android.view.accessibility.AccessibilityNodeInfo.StructuredDataInfo)(info: https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.StructuredDataInfo?)` Sets additional structured data properties of this node, such as for a mathematical expression. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setSupplementalDescription(kotlin.CharSequence)(supplementalDescription: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?)` Sets the supplemental description of this node. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setText(kotlin.CharSequence)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!)` Sets the text of this node. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setTextEntryKey(kotlin.Boolean)(isTextEntryKey: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets whether the node represents a text entry key that is part of a keyboard or keypad. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setTextSelectable(kotlin.Boolean)(selectableText: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets if the node has selectable text. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setTextSelection(kotlin.Int,%20kotlin.Int)(start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, end: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the text selection start and end. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setTooltipText(kotlin.CharSequence)(tooltipText: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?)` Sets the tooltip text of this node. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setTouchDelegateInfo(android.view.accessibility.AccessibilityNodeInfo.TouchDelegateInfo)(delegatedInfo: https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.TouchDelegateInfo)` Set touch delegate info if the represented view has a `https://developer.android.com/reference/kotlin/android/view/TouchDelegate.html#`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setTraversalAfter(android.view.View)(view: https://developer.android.com/reference/kotlin/android/view/View.html#!)` Sets the view whose node is visited after this one in accessibility traversal. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setTraversalAfter(android.view.View,%20kotlin.Int)(root: https://developer.android.com/reference/kotlin/android/view/View.html#!, virtualDescendantId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the node after which this one is visited in accessibility traversal. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setTraversalBefore(android.view.View)(view: https://developer.android.com/reference/kotlin/android/view/View.html#!)` Sets the view before whose node this one should be visited during traversal. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setTraversalBefore(android.view.View,%20kotlin.Int)(root: https://developer.android.com/reference/kotlin/android/view/View.html#!, virtualDescendantId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the node before which this one is visited during traversal. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setUniqueId(kotlin.String)(uniqueId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Sets the unique id to act as a key to identify the node. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setViewIdResourceName(kotlin.String)(viewIdResName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Sets the fully qualified resource name of the source view's id. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setVisibleToUser(kotlin.Boolean)(visibleToUser: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets whether this node is visible to the user. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#toString()()` Returns a string representation of the object. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#writeToParcel(android.os.Parcel,%20kotlin.Int)(parcel: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [AccessibilityNodeInfo](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#)!\> | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### ACTION_ACCESSIBILITY_FOCUS

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_ACCESSIBILITY_FOCUS: Int
```

Action that gives accessibility focus to the node. See `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_ACCESSIBILITY_FOCUS:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction`

 Value: 64

### ACTION_ARGUMENT_COLUMN_INT

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_ARGUMENT_COLUMN_INT: String
```

Argument for specifying the collection column to make visible on screen.

**Type:** int 
**Actions:**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_SCROLL_TO_POSITION:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction`

 Value: "android.view.accessibility.action.ARGUMENT_COLUMN_INT"

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_SCROLL_TO_POSITION:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction`

### ACTION_ARGUMENT_DIRECTION_INT

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_ARGUMENT_DIRECTION_INT: String
```

Argument to represent the direction when using `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_SCROLL_IN_DIRECTION:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction`.

The value of this argument can be one of:

- `https://developer.android.com/reference/kotlin/android/view/View.html#FOCUS_DOWN:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/View.html#FOCUS_UP:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/View.html#FOCUS_LEFT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/View.html#FOCUS_RIGHT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/View.html#FOCUS_FORWARD:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/View.html#FOCUS_BACKWARD:kotlin.Int`

<br />

 Value: "android.view.accessibility.action.ARGUMENT_DIRECTION_INT"

### ACTION_ARGUMENT_EXTEND_SELECTION_BOOLEAN

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_ARGUMENT_EXTEND_SELECTION_BOOLEAN: String
```

Argument for whether when moving at granularity to extend the selection or to move it otherwise.

**Type:** boolean 
**Actions:**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_NEXT_AT_MOVEMENT_GRANULARITY:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_PREVIOUS_AT_MOVEMENT_GRANULARITY:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction`

 Value: "ACTION_ARGUMENT_EXTEND_SELECTION_BOOLEAN"

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_NEXT_AT_MOVEMENT_GRANULARITY:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_PREVIOUS_AT_MOVEMENT_GRANULARITY:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction`

### ACTION_ARGUMENT_HTML_ELEMENT_STRING

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_ARGUMENT_HTML_ELEMENT_STRING: String
```

Argument for which HTML element to get moving to the next/previous HTML element.

**Type:** String 
**Actions:**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_NEXT_HTML_ELEMENT:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_PREVIOUS_HTML_ELEMENT:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction`

<br />

 Value: "ACTION_ARGUMENT_HTML_ELEMENT_STRING"

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_NEXT_HTML_ELEMENT:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_PREVIOUS_HTML_ELEMENT:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction`

### ACTION_ARGUMENT_MOVEMENT_GRANULARITY_INT

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_ARGUMENT_MOVEMENT_GRANULARITY_INT: String
```

Argument for which movement granularity to be used when traversing the node text.

**Type:** int 
**Actions:**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_NEXT_AT_MOVEMENT_GRANULARITY:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_PREVIOUS_AT_MOVEMENT_GRANULARITY:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction`

<br />

 Value: "ACTION_ARGUMENT_MOVEMENT_GRANULARITY_INT"

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_NEXT_AT_MOVEMENT_GRANULARITY:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_PREVIOUS_AT_MOVEMENT_GRANULARITY:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction`

### ACTION_ARGUMENT_MOVE_WINDOW_X

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_ARGUMENT_MOVE_WINDOW_X: String
```

Argument for specifying the x coordinate to which to move a window.

**Type:** int 
**Actions:**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_MOVE_WINDOW:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction`

 Value: "ACTION_ARGUMENT_MOVE_WINDOW_X"

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_MOVE_WINDOW:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction`

### ACTION_ARGUMENT_MOVE_WINDOW_Y

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_ARGUMENT_MOVE_WINDOW_Y: String
```

Argument for specifying the y coordinate to which to move a window.

**Type:** int 
**Actions:**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_MOVE_WINDOW:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction`

 Value: "ACTION_ARGUMENT_MOVE_WINDOW_Y"

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_MOVE_WINDOW:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction`

### ACTION_ARGUMENT_PRESS_AND_HOLD_DURATION_MILLIS_INT

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_ARGUMENT_PRESS_AND_HOLD_DURATION_MILLIS_INT: String
```

Argument to represent the duration in milliseconds to press and hold a node.

**Type:** int 
**Actions:**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_PRESS_AND_HOLD:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction`

 Value: "android.view.accessibility.action.ARGUMENT_PRESS_AND_HOLD_DURATION_MILLIS_INT"

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_PRESS_AND_HOLD:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction`

### ACTION_ARGUMENT_PROGRESS_VALUE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_ARGUMENT_PROGRESS_VALUE: String
```

Argument for specifying the progress value to set.

**Type:** float 
**Actions:**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_SET_PROGRESS:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction`

 Value: "android.view.accessibility.action.ARGUMENT_PROGRESS_VALUE"

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_SET_PROGRESS:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction`

### ACTION_ARGUMENT_ROW_INT

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_ARGUMENT_ROW_INT: String
```

Argument for specifying the collection row to make visible on screen.

**Type:** int 
**Actions:**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_SCROLL_TO_POSITION:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction`

 Value: "android.view.accessibility.action.ARGUMENT_ROW_INT"

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_SCROLL_TO_POSITION:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction`

### ACTION_ARGUMENT_SCROLL_AMOUNT_FLOAT

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_ARGUMENT_SCROLL_AMOUNT_FLOAT: String
```

Argument to represent the scroll amount as a percent of the visible area of a node, with 1.0F as the default. Values smaller than 1.0F represent a partial scroll of the node, and values larger than 1.0F represent a scroll that extends beyond the currently visible node Rect. Setting this to `https://developer.android.com/reference/kotlin/java/lang/Float.html#POSITIVE_INFINITY:kotlin.Float` or to another "too large" value should scroll to the end of the node. Negative values should not be used with this argument.

This argument should be used with the following scroll actions:

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_SCROLL_FORWARD:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_SCROLL_BACKWARD:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_SCROLL_UP:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_SCROLL_DOWN:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_SCROLL_LEFT:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_SCROLL_RIGHT:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction`

<br />

Example: if a view representing a list of items implements `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_SCROLL_FORWARD:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction` to scroll forward by an entire screen (one "page"), then passing a value of .25F via this argument should scroll that view only by 1/4th of a screen. Passing a value of 1.50F via this argument should scroll the view by 1 1/2 screens or to end of the node if the node doesn't extend to 1 1/2 screens.

This argument should not be used with the following scroll actions, which don't cleanly conform to granular scroll semantics:

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_SCROLL_IN_DIRECTION:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_SCROLL_TO_POSITION:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction`

<br />

Views that support this argument should set `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setGranularScrollingSupported(kotlin.Boolean)` to true. Clients should use `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#isGranularScrollingSupported()` to check if granular scrolling is supported.

 Value: "android.view.accessibility.action.ARGUMENT_SCROLL_AMOUNT_FLOAT"

### ACTION_ARGUMENT_SELECTION_END_INT

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_ARGUMENT_SELECTION_END_INT: String
```

Argument for specifying the selection end.

**Type:** int 
**Actions:**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_SET_SELECTION:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction`

 Value: "ACTION_ARGUMENT_SELECTION_END_INT"

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_SET_SELECTION:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction`

### ACTION_ARGUMENT_SELECTION_PARCELABLE

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_ARGUMENT_SELECTION_PARCELABLE: String
```

Argument for specifying the extended selection.

**Type:** `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.Selection` 
**Actions:**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_SET_EXTENDED_SELECTION:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction`

 Value: "android.view.accessibility.action.ARGUMENT_SELECTION_PARCELABLE"

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_SET_EXTENDED_SELECTION:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction`

### ACTION_ARGUMENT_SELECTION_START_INT

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_ARGUMENT_SELECTION_START_INT: String
```

Argument for specifying the selection start.

**Type:** int 
**Actions:**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_SET_SELECTION:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction`

 Value: "ACTION_ARGUMENT_SELECTION_START_INT"

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_SET_SELECTION:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction`

### ACTION_ARGUMENT_SET_TEXT_CHARSEQUENCE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_ARGUMENT_SET_TEXT_CHARSEQUENCE: String
```

Argument for specifying the text content to set.

**Type:** CharSequence 
**Actions:**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_SET_TEXT:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction`

 Value: "ACTION_ARGUMENT_SET_TEXT_CHARSEQUENCE"

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_SET_TEXT:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction`

### ACTION_CLEAR_ACCESSIBILITY_FOCUS

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_CLEAR_ACCESSIBILITY_FOCUS: Int
```

Action that clears accessibility focus of the node. See `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_CLEAR_ACCESSIBILITY_FOCUS:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction`

 Value: 128

### ACTION_CLEAR_FOCUS

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_CLEAR_FOCUS: Int
```

Action that clears input focus of the node. See `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_CLEAR_FOCUS:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction`

 Value: 2

### ACTION_CLEAR_SELECTION

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_CLEAR_SELECTION: Int
```

Action that deselects the node.

 Value: 8

### ACTION_CLICK

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_CLICK: Int
```

Action that clicks on the node info.

 Value: 16

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_CLICK:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction`

### ACTION_COLLAPSE

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_COLLAPSE: Int
```

Action to collapse an expandable node.

 Value: 524288

### ACTION_COPY

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_COPY: Int
```

Action to copy the current selection to the clipboard.

 Value: 16384

### ACTION_CUT

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_CUT: Int
```

Action to cut the current selection and place it to the clipboard.

 Value: 65536

### ACTION_DISMISS

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_DISMISS: Int
```

Action to dismiss a dismissable node.

 Value: 1048576

### ACTION_EXPAND

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_EXPAND: Int
```

Action to expand an expandable node.

 Value: 262144

### ACTION_FOCUS

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_FOCUS: Int
```

Action that gives input focus to the node. See `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_FOCUS:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction`

 Value: 1

### ACTION_LONG_CLICK

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_LONG_CLICK: Int
```

Action that long clicks on the node.

It does not support coordinate information for anchoring.

 Value: 32

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_LONG_CLICK:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction`

### ACTION_NEXT_AT_MOVEMENT_GRANULARITY

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_NEXT_AT_MOVEMENT_GRANULARITY: Int
```

Action that requests to go to the next entity in this node's text at a given movement granularity. For example, move to the next character, word, etc.

**Arguments:** `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_ARGUMENT_MOVEMENT_GRANULARITY_INT:kotlin.String`\<, `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_ARGUMENT_EXTEND_SELECTION_BOOLEAN:kotlin.String` 
**Example:** Move to the previous character and do not extend selection.

```kotlin
<p><code> Bundle arguments = new Bundle(); arguments.putInt(AccessibilityNodeInfo.ACTION_ARGUMENT_MOVEMENT_GRANULARITY_INT, AccessibilityNodeInfo.MOVEMENT_GRANULARITY_CHARACTER); arguments.putBoolean(AccessibilityNodeInfo.ACTION_ARGUMENT_EXTEND_SELECTION_BOOLEAN, false); info.performAction(AccessibilityNodeInfo.ACTION_NEXT_AT_MOVEMENT_GRANULARITY, arguments); </code></p>
```

<br />

<br />

 Value: 256

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_ARGUMENT_MOVEMENT_GRANULARITY_INT:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_ARGUMENT_EXTEND_SELECTION_BOOLEAN:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setMovementGranularities(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getMovementGranularities()`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#MOVEMENT_GRANULARITY_CHARACTER:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#MOVEMENT_GRANULARITY_WORD:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#MOVEMENT_GRANULARITY_LINE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#MOVEMENT_GRANULARITY_PARAGRAPH:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#MOVEMENT_GRANULARITY_PAGE:kotlin.Int`

### ACTION_NEXT_HTML_ELEMENT

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_NEXT_HTML_ELEMENT: Int
```

Action to move to the next HTML element of a given type. For example, move to the BUTTON, INPUT, TABLE, etc.

**Arguments:** `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_ARGUMENT_HTML_ELEMENT_STRING:kotlin.String` 
**Example:**

```kotlin
<p><code> Bundle arguments = new Bundle(); arguments.putString(AccessibilityNodeInfo.ACTION_ARGUMENT_HTML_ELEMENT_STRING, "BUTTON"); info.performAction(AccessibilityNodeInfo.ACTION_NEXT_HTML_ELEMENT, arguments); </code></p>
```

<br />

<br />

 Value: 1024

### ACTION_PASTE

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_PASTE: Int
```

Action to paste the current clipboard content.

 Value: 32768

### ACTION_PREVIOUS_AT_MOVEMENT_GRANULARITY

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_PREVIOUS_AT_MOVEMENT_GRANULARITY: Int
```

Action that requests to go to the previous entity in this node's text at a given movement granularity. For example, move to the next character, word, etc.

**Arguments:** `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_ARGUMENT_MOVEMENT_GRANULARITY_INT:kotlin.String`\<, `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_ARGUMENT_EXTEND_SELECTION_BOOLEAN:kotlin.String` 
**Example:** Move to the next character and do not extend selection.

```kotlin
<p><code> Bundle arguments = new Bundle(); arguments.putInt(AccessibilityNodeInfo.ACTION_ARGUMENT_MOVEMENT_GRANULARITY_INT, AccessibilityNodeInfo.MOVEMENT_GRANULARITY_CHARACTER); arguments.putBoolean(AccessibilityNodeInfo.ACTION_ARGUMENT_EXTEND_SELECTION_BOOLEAN, false); info.performAction(AccessibilityNodeInfo.ACTION_PREVIOUS_AT_MOVEMENT_GRANULARITY, arguments); </code></p>
```

<br />

<br />

 Value: 512

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_ARGUMENT_MOVEMENT_GRANULARITY_INT:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_ARGUMENT_EXTEND_SELECTION_BOOLEAN:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setMovementGranularities(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getMovementGranularities()`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#MOVEMENT_GRANULARITY_CHARACTER:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#MOVEMENT_GRANULARITY_WORD:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#MOVEMENT_GRANULARITY_LINE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#MOVEMENT_GRANULARITY_PARAGRAPH:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#MOVEMENT_GRANULARITY_PAGE:kotlin.Int`

### ACTION_PREVIOUS_HTML_ELEMENT

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_PREVIOUS_HTML_ELEMENT: Int
```

Action to move to the previous HTML element of a given type. For example, move to the BUTTON, INPUT, TABLE, etc.

**Arguments:** `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_ARGUMENT_HTML_ELEMENT_STRING:kotlin.String` 
**Example:**

```kotlin
<p><code> Bundle arguments = new Bundle(); arguments.putString(AccessibilityNodeInfo.ACTION_ARGUMENT_HTML_ELEMENT_STRING, "BUTTON"); info.performAction(AccessibilityNodeInfo.ACTION_PREVIOUS_HTML_ELEMENT, arguments); </code></p>
```

<br />

<br />

 Value: 2048

### ACTION_SCROLL_BACKWARD

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_SCROLL_BACKWARD: Int
```

Action to scroll the node content backward.

 Value: 8192

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_SCROLL_BACKWARD:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction`

### ACTION_SCROLL_FORWARD

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_SCROLL_FORWARD: Int
```

Action to scroll the node content forward.

 Value: 4096

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_SCROLL_FORWARD:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction`

### ACTION_SELECT

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_SELECT: Int
```

Action that selects the node.

 Value: 4

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_SELECT:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction`

### ACTION_SET_SELECTION

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_SET_SELECTION: Int
```

Action to set the selection. Performing this action with no arguments clears the selection.

 Value: 131072

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_SET_SELECTION:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_ARGUMENT_SELECTION_START_INT:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_ARGUMENT_SELECTION_END_INT:kotlin.String`

### ACTION_SET_TEXT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_SET_TEXT: Int
```

Action that sets the text of the node. Performing the action without argument, using ` null` or empty `https://developer.android.com/reference/kotlin/java/lang/CharSequence.html#` will clear the text. This action will also put the cursor at the end of text.

 Value: 2097152

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_SET_TEXT:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction`

### CHECKED_STATE_FALSE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHECKED_STATE_FALSE: Int
```

This node is not checked.

 Value: 0

### CHECKED_STATE_PARTIAL

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHECKED_STATE_PARTIAL: Int
```

This node is partially checked. For example, when a checkbox owns a number of sub-options and they have different states, then the main checkbox is in a partially-checked state.

 Value: 2

### CHECKED_STATE_TRUE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHECKED_STATE_TRUE: Int
```

This node is checked.

 Value: 1

### EXPANDED_STATE_COLLAPSED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXPANDED_STATE_COLLAPSED: Int
```

Expanded state for a collapsed expandable element.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getExpandedState()`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setExpandedState(kotlin.Int)`

### EXPANDED_STATE_FULL

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXPANDED_STATE_FULL: Int
```

Expanded state for a expanded expandable element that cannot be expanded further.

 Value: 3

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getExpandedState()`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setExpandedState(kotlin.Int)`

### EXPANDED_STATE_PARTIAL

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXPANDED_STATE_PARTIAL: Int
```

Expanded state for an expanded expandable element that can still be expanded further.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getExpandedState()`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setExpandedState(kotlin.Int)`

### EXPANDED_STATE_UNDEFINED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXPANDED_STATE_UNDEFINED: Int
```

Expanded state for a non-expandable element

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getExpandedState()`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setExpandedState(kotlin.Int)`

### EXTRA_DATA_RENDERING_INFO_KEY

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_DATA_RENDERING_INFO_KEY: String
```

Key used to request extra data for the rendering information. The key requests that a `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.ExtraRenderingInfo` be added to this info. This request is made with `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#refreshWithExtraData(kotlin.String,%20android.os.Bundle)` without argument.

The data can be retrieved from the `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.ExtraRenderingInfo` returned by `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getExtraRenderingInfo()` using `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.ExtraRenderingInfo#getLayoutSize()`, `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.ExtraRenderingInfo#getTextSizeInPx()` and `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.ExtraRenderingInfo#getTextSizeUnit()`. For layout params, it is supported by both `https://developer.android.com/reference/kotlin/android/widget/TextView.html#` and `https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#`. For text size and unit, it is only supported by `https://developer.android.com/reference/kotlin/android/widget/TextView.html#`.

 Value: "android.view.accessibility.extra.DATA_RENDERING_INFO_KEY"

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#refreshWithExtraData(kotlin.String,%20android.os.Bundle)`

### EXTRA_DATA_REQUEST_LAYOUT_BASED_ACTIONS_KEY

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_DATA_REQUEST_LAYOUT_BASED_ACTIONS_KEY: String
```

Key used to request that the node source re-evaluate and update this node's layout-dependent actions. This request is made with `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#refreshWithExtraData(kotlin.String,%20android.os.Bundle)` and takes no arguments.

Some actions may depend on the on-screen layout of a node. In complex or dynamic UIs, it may be difficult for a source to determine if a node is truly actionable without more intensive inspection. For example, a node may be misreported as clickable despite being occluded, requiring a hit-test to confirm the availability of the action.

Using this key requests that the source perform a more intensive, layout-based analysis to determine which actions are available to the user. After this request, the source will update the actions and related properties of this node. For example, for clickability, this may result in changes to the value returned by `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#isClickable()` and the presence of `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_CLICK:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction` in the node's `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getActionList()`.

This analysis can be computationally expensive and should only be requested when needed to resolve ambiguous or inaccurate actions.

Providers may advertise that they support this request using `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setAvailableExtraData(kotlin.collections.MutableList)`. Services may check for support with `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getAvailableExtraData()`.

 Value: "android.view.accessibility.extra.DATA_REQUEST_LAYOUT_BASED_ACTIONS_KEY"

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#refreshWithExtraData(kotlin.String,%20android.os.Bundle)`

### EXTRA_DATA_TEXT_CHARACTER_LOCATION_ARG_LENGTH

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_DATA_TEXT_CHARACTER_LOCATION_ARG_LENGTH: String
```

Integer argument specifying the end index of the requested text location data. Must be positive and no larger than `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#EXTRA_DATA_TEXT_CHARACTER_LOCATION_ARG_MAX_LENGTH:kotlin.Int`.

 Value: "android.view.accessibility.extra.DATA_TEXT_CHARACTER_LOCATION_ARG_LENGTH"

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#EXTRA_DATA_TEXT_CHARACTER_LOCATION_KEY:kotlin.String`

### EXTRA_DATA_TEXT_CHARACTER_LOCATION_ARG_MAX_LENGTH

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_DATA_TEXT_CHARACTER_LOCATION_ARG_MAX_LENGTH: Int
```

The maximum allowed length of the requested text location data.

 Value: 20000

### EXTRA_DATA_TEXT_CHARACTER_LOCATION_ARG_START_INDEX

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_DATA_TEXT_CHARACTER_LOCATION_ARG_START_INDEX: String
```

Integer argument specifying the start index of the requested text location data. Must be valid inside the CharSequence returned by `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getText()`.

 Value: "android.view.accessibility.extra.DATA_TEXT_CHARACTER_LOCATION_ARG_START_INDEX"

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#EXTRA_DATA_TEXT_CHARACTER_LOCATION_KEY:kotlin.String`

### EXTRA_DATA_TEXT_CHARACTER_LOCATION_IN_WINDOW_KEY

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_DATA_TEXT_CHARACTER_LOCATION_IN_WINDOW_KEY: String
```

Key used to request and locate extra data for text character location in window coordinates. This key requests that an array of `https://developer.android.com/reference/kotlin/android/graphics/RectF.html#`s be added to the extras. This request is made with `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#refreshWithExtraData(kotlin.String,%20android.os.Bundle)`. The arguments taken by this request are two integers: `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#EXTRA_DATA_TEXT_CHARACTER_LOCATION_ARG_START_INDEX:kotlin.String` and `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#EXTRA_DATA_TEXT_CHARACTER_LOCATION_ARG_LENGTH:kotlin.String`. The starting index must be valid inside the CharSequence returned by `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getText()`, and the length must be positive.

Providers may advertise that they support text characters in window coordinates using `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setAvailableExtraData(kotlin.collections.MutableList)`. Services may check if an implementation supports text characters in window coordinates with `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getAvailableExtraData()`.

The data can be retrieved from the `Bundle` returned by `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getExtras()` using this string as a key for `https://developer.android.com/reference/kotlin/android/os/Bundle.html#getParcelableArray(kotlin.String,%20java.lang.Class)`. The `https://developer.android.com/reference/kotlin/android/graphics/RectF.html#` will be `null` for characters that either do not exist or are outside of the window bounds.

Note that character locations in window bounds are not modified by changes in display magnification.

 Value: "android.view.accessibility.extra.DATA_TEXT_CHARACTER_LOCATION_IN_WINDOW_KEY"

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#refreshWithExtraData(kotlin.String,%20android.os.Bundle)`

### EXTRA_DATA_TEXT_CHARACTER_LOCATION_KEY

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_DATA_TEXT_CHARACTER_LOCATION_KEY: String
```

Key used to request and locate extra data for text character location. This key requests that an array of `https://developer.android.com/reference/kotlin/android/graphics/RectF.html#`s be added to the extras. This request is made with `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#refreshWithExtraData(kotlin.String,%20android.os.Bundle)`. The arguments taken by this request are two integers: `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#EXTRA_DATA_TEXT_CHARACTER_LOCATION_ARG_START_INDEX:kotlin.String` and `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#EXTRA_DATA_TEXT_CHARACTER_LOCATION_ARG_LENGTH:kotlin.String`. The starting index must be valid inside the CharSequence returned by `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getText()`, and the length must be positive.

The data can be retrieved from the `Bundle` returned by `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getExtras()` using this string as a key for `https://developer.android.com/reference/kotlin/android/os/Bundle.html#getParcelableArray(kotlin.String,%20java.lang.Class)`. The `https://developer.android.com/reference/kotlin/android/graphics/RectF.html#` will be `null` for characters that either do not exist or are off the screen.

Note that character locations returned are modified by changes in display magnification.

 Value: "android.view.accessibility.extra.DATA_TEXT_CHARACTER_LOCATION_KEY"

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#refreshWithExtraData(kotlin.String,%20android.os.Bundle)`

### FLAG_PREFETCH_ANCESTORS

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_PREFETCH_ANCESTORS: Int
```

Prefetching strategy that prefetches the ancestors of the requested node.

Ancestors will be prefetched before siblings and descendants.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getChild(kotlin.Int,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getParent(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#getRoot(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#getRootInActiveWindow(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getSource(kotlin.Int)`

### FLAG_PREFETCH_DESCENDANTS_BREADTH_FIRST

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_PREFETCH_DESCENDANTS_BREADTH_FIRST: Int
```

Prefetching strategy that prefetches the descendants of the requested node breadth-first.

This must not be combined with `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#FLAG_PREFETCH_DESCENDANTS_HYBRID:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#FLAG_PREFETCH_DESCENDANTS_DEPTH_FIRST:kotlin.Int` or this will trigger an IllegalArgumentException.

See `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#FLAG_PREFETCH_ANCESTORS:kotlin.Int` for information on where these flags can be used.

 Value: 16

### FLAG_PREFETCH_DESCENDANTS_DEPTH_FIRST

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_PREFETCH_DESCENDANTS_DEPTH_FIRST: Int
```

Prefetching strategy that prefetches the descendants of the requested node depth-first.

This must not be combined with `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#FLAG_PREFETCH_DESCENDANTS_HYBRID:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#FLAG_PREFETCH_DESCENDANTS_BREADTH_FIRST:kotlin.Int` or this will trigger an IllegalArgumentException.

See `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#FLAG_PREFETCH_ANCESTORS:kotlin.Int` for information on where these flags can be used.

 Value: 8

### FLAG_PREFETCH_DESCENDANTS_HYBRID

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_PREFETCH_DESCENDANTS_HYBRID: Int
```

Prefetching strategy that prefetches the descendants in a hybrid depth first and breadth first approach.

The children of the root node is prefetched before recursing on the children. This must not be combined with `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#FLAG_PREFETCH_DESCENDANTS_DEPTH_FIRST:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#FLAG_PREFETCH_DESCENDANTS_BREADTH_FIRST:kotlin.Int` or this will trigger an IllegalArgumentException.

See `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#FLAG_PREFETCH_ANCESTORS:kotlin.Int` for information on where these flags can be used.

 Value: 4

### FLAG_PREFETCH_SIBLINGS

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_PREFETCH_SIBLINGS: Int
```

Prefetching strategy that prefetches the siblings of the requested node.

To avoid disconnected trees, this flag will also prefetch the parent. Siblings will be prefetched before descendants.

See `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#FLAG_PREFETCH_ANCESTORS:kotlin.Int` for information on where these flags can be used.

 Value: 2

### FLAG_PREFETCH_UNINTERRUPTIBLE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_PREFETCH_UNINTERRUPTIBLE: Int
```

Prefetching flag that specifies prefetching should not be interrupted by a request to retrieve a node or perform an action on a node.

See `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#FLAG_PREFETCH_ANCESTORS:kotlin.Int` for information on where these flags can be used.

 Value: 32

### FOCUS_ACCESSIBILITY

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FOCUS_ACCESSIBILITY: Int
```

The accessibility focus.

 Value: 2

### FOCUS_INPUT

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FOCUS_INPUT: Int
```

The input focus.

 Value: 1

### MAX_NUMBER_OF_PREFETCHED_NODES

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MAX_NUMBER_OF_PREFETCHED_NODES: Int
```

Maximum batch size of prefetched nodes for a request.

 Value: 50

### MOVEMENT_GRANULARITY_CHARACTER

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MOVEMENT_GRANULARITY_CHARACTER: Int
```

Movement granularity bit for traversing the text of a node by character.

 Value: 1

### MOVEMENT_GRANULARITY_LINE

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MOVEMENT_GRANULARITY_LINE: Int
```

Movement granularity bit for traversing the text of a node by line.

 Value: 4

### MOVEMENT_GRANULARITY_PAGE

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MOVEMENT_GRANULARITY_PAGE: Int
```

Movement granularity bit for traversing the text of a node by page.

 Value: 16

### MOVEMENT_GRANULARITY_PARAGRAPH

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MOVEMENT_GRANULARITY_PARAGRAPH: Int
```

Movement granularity bit for traversing the text of a node by paragraph.

 Value: 8

### MOVEMENT_GRANULARITY_WORD

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MOVEMENT_GRANULARITY_WORD: Int
```

Movement granularity bit for traversing the text of a node by word.

 Value: 2

## Public constructors

### AccessibilityNodeInfo

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
AccessibilityNodeInfo()
```

Creates a new `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#`.

### AccessibilityNodeInfo

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
AccessibilityNodeInfo(info: AccessibilityNodeInfo)
```

Copy constructor. Creates a new `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#`, and this new instance is initialized from the given `info`.

| Parameters ||
|---|---|
| `info` | [AccessibilityNodeInfo](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#): The other info. This value cannot be `null`. |

### AccessibilityNodeInfo

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
AccessibilityNodeInfo(source: View)
```

Creates a new `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#` with the given `source`.

| Parameters ||
|---|---|
| `source` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#): The source view. This value cannot be `null`. |

### AccessibilityNodeInfo

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
AccessibilityNodeInfo(
    root: View, 
    virtualDescendantId: Int)
```

Creates a new `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#` with the given `source`.

| Parameters ||
|---|---|
| `root` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#): The root of the virtual subtree. This value cannot be `null`. |
| `virtualDescendantId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the virtual descendant. |

## Public methods

### addAction

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addAction(action: AccessibilityNodeInfo.AccessibilityAction!): Unit
```

Adds an action that can be performed on the node.

To add a standard action use the static constants on `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction`. To add a custom action create a new `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction` by passing in a resource id from your application as the action id and an optional label that describes the action. To override one of the standard actions use as the action id of a standard action id such as `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_CLICK:kotlin.Int` and an optional label that describes the action.

Use androidx.core.view.ViewCompat#addAccessibilityAction(android.view.View,java.lang.CharSequence,AccessibilityViewCommand) to register an action directly on the view.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService.

| Parameters ||
|---|---|
| `action` | [AccessibilityNodeInfo.AccessibilityAction](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction)!: The action. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If called from an AccessibilityService. |

### addAction

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addAction(action: Int): Unit
```

**Deprecated:** *This has been deprecated for `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#addAction(android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction)`*

Adds an action that can be performed on the node.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService.

| Parameters ||
|---|---|
| `action` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The action. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If the argument is not one of the standard actions. |
| `java.lang.IllegalStateException` | If called from an AccessibilityService. |

### addChild

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addChild(child: View!): Unit
```

Adds a child.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService. Note that a view cannot be made its own child.

| Parameters ||
|---|---|
| `child` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!: The child. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If called from an AccessibilityService. |

### addChild

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addChild(
    root: View!, 
    virtualDescendantId: Int
): Unit
```

Adds a virtual child which is a descendant of the given `root`. If `virtualDescendantId` is `https://developer.android.com/reference/kotlin/android/view/View.html#NO_ID:kotlin.Int` the root is added as a child.

A virtual descendant is an imaginary View that is reported as a part of the view hierarchy for accessibility purposes. This enables custom views that draw complex content to report them selves as a tree of virtual views, thus conveying their logical structure. Note that a view cannot be made its own child.

| Parameters ||
|---|---|
| `root` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!: The root of the virtual subtree. |
| `virtualDescendantId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the virtual child. |

### addLabeledBy

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addLabeledBy(label: View): Unit
```

Adds the view which serves as the label of the view represented by this info for accessibility purposes. When multiple labels are added, the content from each label is combined in the order that they are added.

If visible text can be used to describe or give meaning to this UI, this method is preferred. For example, a TextView before an EditText in the UI usually specifies what information is contained in the EditText. Hence, the EditText is labeled by the TextView.

| Parameters ||
|---|---|
| `label` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#): A view that labels this node's source. This value cannot be `null`. |

### addLabeledBy

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addLabeledBy(
    root: View, 
    virtualDescendantId: Int
): Unit
```

Adds the view which serves as the label of the view represented by this info for accessibility purposes. If `virtualDescendantId` is `https://developer.android.com/reference/kotlin/android/view/View.html#NO_ID:kotlin.Int` the root is set as the label. When multiple labels are added, the content from each label is combined in the order that they are added.

A virtual descendant is an imaginary View that is reported as a part of the view hierarchy for accessibility purposes. This enables custom views that draw complex content to report themselves as a tree of virtual views, thus conveying their logical structure.

If visible text can be used to describe or give meaning to this UI, this method is preferred. For example, a TextView before an EditText in the UI usually specifies what information is contained in the EditText. Hence, the EditText is labeled by the TextView.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService.

| Parameters ||
|---|---|
| `root` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#): A root whose virtual descendant labels this node's source. This value cannot be `null`. |
| `virtualDescendantId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the virtual descendant. |

### canOpenPopup

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun canOpenPopup(): Boolean
```

Gets if this node opens a popup or a dialog.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | If the the node opens a popup. |

### describeContents

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### equals

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The `equals` method implements an equivalence relation on non-null object references:

- It is *reflexive* : for any non-null reference value `x`, `x.equals(x)` should return `true`.
- It is *symmetric* : for any non-null reference values `x` and `y`, `x.equals(y)` should return `true` if and only if `y.equals(x)` returns `true`.
- It is *transitive* : for any non-null reference values `x`, `y`, and `z`, if `x.equals(y)` returns `true` and `y.equals(z)` returns `true`, then `x.equals(z)` should return `true`.
- It is *consistent* : for any non-null reference values `x` and `y`, multiple invocations of `x.equals(y)` consistently return `true` or consistently return `false`, provided no information used in `equals` comparisons on the objects is modified.
- For any non-null reference value `x`, `x.equals(null)` should return `false`.

An equivalence relation partitions the elements it operates on into *equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |
| `object` | This value may be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

### findAccessibilityNodeInfosByText

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun findAccessibilityNodeInfosByText(text: String!): MutableList<AccessibilityNodeInfo!>!
```

Finds `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#`s by text. The match is case insensitive containment. The search is relative to this info i.e. this info is the root of the traversed tree.

**Note:** If this view hierarchy has a `https://developer.android.com/reference/kotlin/android/view/SurfaceView.html#` embedding another view hierarchy via `https://developer.android.com/reference/kotlin/android/view/SurfaceView.html#setChildSurfacePackage(android.view.SurfaceControlViewHost.SurfacePackage)`, there is a limitation that this API won't be able to find the node for the view on the embedded view hierarchy. It's because views don't know about the embedded hierarchies. Instead, you could traverse all the children to find the node.

| Parameters ||
|---|---|
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The searched text. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#!>!` | A list of node info. |

### findAccessibilityNodeInfosByViewId

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun findAccessibilityNodeInfosByViewId(viewId: String): MutableList<AccessibilityNodeInfo!>!
```

Finds `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#`s by the fully qualified view id's resource name where a fully qualified id is of the from "package:id/id_resource_name". For example, if the target application's package is "foo.bar" and the id resource name is "baz", the fully qualified resource id is "foo.bar:id/baz".

**Note:** The primary usage of this API is for UI test automation and in order to report the fully qualified view id if an `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#` the client has to set the `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo.html#FLAG_REPORT_VIEW_IDS:kotlin.Int` flag when configuring the `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`.

**Note:** If this view hierarchy has a `https://developer.android.com/reference/kotlin/android/view/SurfaceView.html#` embedding another view hierarchy via `https://developer.android.com/reference/kotlin/android/view/SurfaceView.html#setChildSurfacePackage(android.view.SurfaceControlViewHost.SurfacePackage)`, there is a limitation that this API won't be able to find the node for the view on the embedded view hierarchy. It's because views don't know about the embedded hierarchies. Instead, you could traverse all the children to find the node.

| Parameters ||
|---|---|
| `viewId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The fully qualified resource name of the view id to find. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#!>!` | A list of node info. |

### findFocus

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun findFocus(focus: Int): AccessibilityNodeInfo!
```

Find the view that has the specified focus type. The search starts from the view represented by this node info.

**Note:** If this view hierarchy has a `https://developer.android.com/reference/kotlin/android/view/SurfaceView.html#` embedding another view hierarchy via `https://developer.android.com/reference/kotlin/android/view/SurfaceView.html#setChildSurfacePackage(android.view.SurfaceControlViewHost.SurfacePackage)`, there is a limitation that this API won't be able to find the node for the view on the embedded view hierarchy. It's because views don't know about the embedded hierarchies. Instead, you could traverse all the children to find the node. Or, use `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#findFocus(kotlin.Int)` for `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#FOCUS_ACCESSIBILITY:kotlin.Int` only since it has no such limitation.

| Parameters ||
|---|---|
| `focus` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The focus to find. One of `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#FOCUS_INPUT:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#FOCUS_ACCESSIBILITY:kotlin.Int`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#!` | The node info of the focused view or null. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#FOCUS_INPUT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#FOCUS_ACCESSIBILITY:kotlin.Int`

### focusSearch

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun focusSearch(direction: Int): AccessibilityNodeInfo!
```

Searches for the nearest view in the specified direction that can take the input focus.

**Note:** If this view hierarchy has a `https://developer.android.com/reference/kotlin/android/view/SurfaceView.html#` embedding another view hierarchy via `https://developer.android.com/reference/kotlin/android/view/SurfaceView.html#setChildSurfacePackage(android.view.SurfaceControlViewHost.SurfacePackage)`, there is a limitation that this API won't be able to find the node for the view in the specified direction on the embedded view hierarchy. It's because views don't know about the embedded hierarchies. Instead, you could traverse all the children to find the node.

| Parameters ||
|---|---|
| `direction` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The direction. Can be one of: `https://developer.android.com/reference/kotlin/android/view/View.html#FOCUS_DOWN:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View.html#FOCUS_UP:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View.html#FOCUS_LEFT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View.html#FOCUS_RIGHT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View.html#FOCUS_FORWARD:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/View.html#FOCUS_BACKWARD:kotlin.Int`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#!` | The node info for the view that can take accessibility focus. |

### getActionList

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getActionList(): MutableList<AccessibilityNodeInfo.AccessibilityAction!>!
```

Gets the actions that can be performed on the node.

### getActions

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getActions(): Int
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getActionList()`.*

Gets the actions that can be performed on the node.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The bit mask of with actions. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_FOCUS:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_CLEAR_FOCUS:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_SELECT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_CLEAR_SELECTION:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_ACCESSIBILITY_FOCUS:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_CLEAR_ACCESSIBILITY_FOCUS:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_CLICK:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_LONG_CLICK:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_NEXT_AT_MOVEMENT_GRANULARITY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_PREVIOUS_AT_MOVEMENT_GRANULARITY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_NEXT_HTML_ELEMENT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_PREVIOUS_HTML_ELEMENT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_SCROLL_FORWARD:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_SCROLL_BACKWARD:kotlin.Int`

### getAvailableExtraData

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAvailableExtraData(): MutableList<String!>!
```

Get the extra data available for this node.

Some data that is useful for some accessibility services is expensive to compute, and would place undue overhead on apps to compute all the time. That data can be requested with `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#refreshWithExtraData(kotlin.String,%20android.os.Bundle)`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | An unmodifiable list of keys corresponding to extra data that can be requested. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#EXTRA_DATA_RENDERING_INFO_KEY:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#EXTRA_DATA_TEXT_CHARACTER_LOCATION_KEY:kotlin.String`

### getBoundsInParent

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getBoundsInParent(outBounds: Rect!): Unit
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getBoundsInScreen(android.graphics.Rect)` instead.*

Gets the node bounds in the viewParent's coordinates. `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getParent()` does not represent the source's viewParent. Instead it represents the result of `https://developer.android.com/reference/kotlin/android/view/View.html#getParentForAccessibility()`, which returns the closest ancestor where `https://developer.android.com/reference/kotlin/android/view/View.html#isImportantForAccessibility()` is true. So this method is not reliable.

When magnification is enabled, the bounds in parent are also scaled up by magnification scale. For example, it returns Rect(20, 20, 200, 200) for original bounds Rect(10, 10, 100, 100), when the magnification scale is 2.

<br />

| Parameters ||
|---|---|
| `outBounds` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)!: The output node bounds. |

### getBoundsInScreen

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getBoundsInScreen(outBounds: Rect!): Unit
```

Gets the node bounds in screen coordinates.

When magnification is enabled, the bounds in screen are scaled up by magnification scale and the positions are also adjusted according to the offset of magnification viewport. For example, it returns Rect(-180, -180, 0, 0) for original bounds Rect(10, 10, 100, 100), when the magnification scale is 2 and offsets for X and Y are both 200.

<br />

| Parameters ||
|---|---|
| `outBounds` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)!: The output node bounds. |

### getBoundsInWindow

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getBoundsInWindow(outBounds: Rect): Unit
```

Gets the node bounds in window coordinates.

The node bounds returned are not scaled by magnification.

<br />

| Parameters ||
|---|---|
| `outBounds` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#): The output node bounds. This value cannot be `null`. |

### getChecked

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getChecked(): Int
```

Gets the checked state of this node. This is only meaningful when `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#isCheckable()` returns `true`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The checked state, one of: - `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#CHECKED_STATE_FALSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#CHECKED_STATE_TRUE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#CHECKED_STATE_PARTIAL:kotlin.Int` . Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#CHECKED_STATE_FALSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#CHECKED_STATE_TRUE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#CHECKED_STATE_PARTIAL:kotlin.Int` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setCheckable(kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#isCheckable()`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setChecked(kotlin.Int)`

### getChild

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getChild(index: Int): AccessibilityNodeInfo!
```

Get the child at given index.

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The child index. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#!` | The child node. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If called outside of an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#` and before calling `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setQueryFromAppProcessEnabled(android.view.View,%20kotlin.Boolean)`. |

### getChild

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getChild(
    index: Int, 
    prefetchingStrategy: Int
): AccessibilityNodeInfo?
```

Get the child at given index.

See `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getParent(kotlin.Int)` for a description of prefetching.

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The child index. |
| `prefetchingStrategy` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the prefetching strategy. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#FLAG_PREFETCH_ANCESTORS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#FLAG_PREFETCH_SIBLINGS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#FLAG_PREFETCH_DESCENDANTS_HYBRID:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#FLAG_PREFETCH_DESCENDANTS_DEPTH_FIRST:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#FLAG_PREFETCH_DESCENDANTS_BREADTH_FIRST:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#FLAG_PREFETCH_UNINTERRUPTIBLE:kotlin.Int` |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#?` | The child node. This value may be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If called outside of an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#` and before calling `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setQueryFromAppProcessEnabled(android.view.View,%20kotlin.Boolean)`. |

### getChildCount

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getChildCount(): Int
```

Gets the number of children.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The child count. |

### getClassName

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getClassName(): CharSequence!
```

Gets the class this node comes from.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!` | The class name. |

### getCollectionInfo

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCollectionInfo(): AccessibilityNodeInfo.CollectionInfo!
```

Gets the collection info if the node is a collection. A collection child is always a collection item.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.CollectionInfo!` | The collection info. |

### getCollectionItemInfo

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCollectionItemInfo(): AccessibilityNodeInfo.CollectionItemInfo!
```

Gets the collection item info if the node is a collection item. A collection item is always a child of a collection.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.CollectionItemInfo!` | The collection item info. |

### getContainerTitle

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getContainerTitle(): CharSequence?
```

Returns the container title.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?` | This value may be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setContainerTitle(kotlin.CharSequence)`

### getContentDescription

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getContentDescription(): CharSequence!
```

Gets the content description of this node.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!` | The content description. |

### getDrawingOrder

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDrawingOrder(): Int
```

Get the drawing order of the view corresponding it this node.

Drawing order is determined only within the node's parent, so this index is only relative to its siblings.

In some cases, the drawing order is essentially simultaneous, so it is possible for two siblings to return the same value. It is also possible that values will be skipped.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The drawing position of the view corresponding to this node relative to its siblings. |

### getError

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getError(): CharSequence!
```

Gets the error text of this node.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!` | The error text. |

### getExpandedState

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getExpandedState(): Int
```

Gets the expanded state for this node.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The expanded state, one of: - `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#EXPANDED_STATE_UNDEFINED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#EXPANDED_STATE_COLLAPSED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#EXPANDED_STATE_FULL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#EXPANDED_STATE_PARTIAL:kotlin.Int` . Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#EXPANDED_STATE_UNDEFINED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#EXPANDED_STATE_COLLAPSED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#EXPANDED_STATE_PARTIAL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#EXPANDED_STATE_FULL:kotlin.Int` |

### getExtraRenderingInfo

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getExtraRenderingInfo(): AccessibilityNodeInfo.ExtraRenderingInfo?
```

Gets the `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.ExtraRenderingInfo` if the node is meant to be refreshed with extra data to examine rendering related accessibility issues.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.ExtraRenderingInfo?` | The `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.ExtraRenderingInfo`. This value may be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#EXTRA_DATA_RENDERING_INFO_KEY:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#refreshWithExtraData(kotlin.String,%20android.os.Bundle)`

### getExtras

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getExtras(): Bundle!
```

Gets an optional bundle with extra data. The bundle is lazily created and never `null`.

**Note:** It is recommended to use the package name of your application as a prefix for the keys to avoid collisions which may confuse an accessibility service if the same key has different meaning when emitted from different applications.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/Bundle.html#!` | The bundle. |

### getHintText

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getHintText(): CharSequence!
```

Gets the hint text of this node. Only applies to nodes where text can be entered.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!` | The hint text. |

### getInputType

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getInputType(): Int
```

Gets the input type of the source as defined by `https://developer.android.com/reference/kotlin/android/text/InputType.html#`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The input type. |

### getLabelFor

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLabelFor(): AccessibilityNodeInfo!
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getLabeledByList()` on the labeled node instead, since calling `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#addLabeledBy(android.view.View)` or `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#addLabeledBy(android.view.View,%20kotlin.Int)` on the labeled node do not automatically provide that node from this method.*

Gets the node info for which the view represented by this info serves as a label for accessibility purposes.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#!` | The labeled info. |

### getLabeledBy

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLabeledBy(): AccessibilityNodeInfo!
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getLabeledByList()` instead.*

Gets the node info which serves as the label of the view represented by this info for accessibility purposes.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#!` | The label. |

### getLabeledByList

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLabeledByList(): MutableList<AccessibilityNodeInfo!>
```

Gets the list of node infos which serve as the labels of the view represented by this info for accessibility purposes.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#!>` | The list of labels in the order that they were added. This value cannot be `null`. |

### getLiveRegion

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLiveRegion(): Int
```

Gets the node's live region mode.

A live region is a node that contains information that is important for the user and when it changes the user should be notified. For example, a Snackbar that displays a confirmation notification should be marked as a live region with mode `https://developer.android.com/reference/kotlin/android/view/View.html#ACCESSIBILITY_LIVE_REGION_POLITE:kotlin.Int`.

It is the responsibility of the accessibility service to monitor `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOW_CONTENT_CHANGED:kotlin.Int` events indicating changes to live region nodes and their children.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The live region mode, or `https://developer.android.com/reference/kotlin/android/view/View.html#ACCESSIBILITY_LIVE_REGION_NONE:kotlin.Int` if the view is not a live region. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/View.html#getAccessibilityLiveRegion()`

### getMaxTextLength

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMaxTextLength(): Int
```

Returns the maximum text length for this node.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The maximum text length, or -1 for no limit. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setMaxTextLength(kotlin.Int)`

### getMinDurationBetweenContentChanges

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMinDurationBetweenContentChanges(): Duration
```

Gets the minimum time duration between two content change events.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/Duration.html#` | This value cannot be `null`. |

### getMovementGranularities

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMovementGranularities(): Int
```

Gets the movement granularities for traversing the text of this node.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The bit mask with granularities. |

### getPackageName

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPackageName(): CharSequence!
```

Gets the package this node comes from.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!` | The package name. |

### getPaneTitle

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPaneTitle(): CharSequence?
```

Get the title of the pane represented by this node.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?` | The title of the pane represented by this node, or `null` if this node does not represent a pane. |

### getParent

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getParent(): AccessibilityNodeInfo!
```

Gets the parent.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#!` | The parent. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If called outside of an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#` and before calling `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setQueryFromAppProcessEnabled(android.view.View,%20kotlin.Boolean)`. |

### getParent

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getParent(prefetchingStrategy: Int): AccessibilityNodeInfo?
```

Gets the parent.

Use `prefetchingStrategy` to determine the types of nodes prefetched from the app if the requested node is not in the cache and must be retrieved by the app. The default strategy for `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getParent()` is a combination of ancestor and sibling strategies. The app will prefetch until all nodes fulfilling the strategies are fetched, another node request is sent, or the maximum prefetch batch size of `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#MAX_NUMBER_OF_PREFETCHED_NODES:kotlin.Int` nodes is reached. To prevent interruption by another request and to force prefetching of the max batch size, use `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#FLAG_PREFETCH_UNINTERRUPTIBLE:kotlin.Int`.

| Parameters ||
|---|---|
| `prefetchingStrategy` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the prefetching strategy. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#FLAG_PREFETCH_ANCESTORS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#FLAG_PREFETCH_SIBLINGS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#FLAG_PREFETCH_DESCENDANTS_HYBRID:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#FLAG_PREFETCH_DESCENDANTS_DEPTH_FIRST:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#FLAG_PREFETCH_DESCENDANTS_BREADTH_FIRST:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#FLAG_PREFETCH_UNINTERRUPTIBLE:kotlin.Int` |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#?` | The parent. This value may be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If called outside of an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#` and before calling `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setQueryFromAppProcessEnabled(android.view.View,%20kotlin.Boolean)`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#FLAG_PREFETCH_ANCESTORS:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#FLAG_PREFETCH_DESCENDANTS_BREADTH_FIRST:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#FLAG_PREFETCH_DESCENDANTS_DEPTH_FIRST:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#FLAG_PREFETCH_DESCENDANTS_HYBRID:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#FLAG_PREFETCH_SIBLINGS:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#FLAG_PREFETCH_UNINTERRUPTIBLE:kotlin.Int`

### getRangeInfo

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getRangeInfo(): AccessibilityNodeInfo.RangeInfo!
```

Gets the range info if this node is a range.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.RangeInfo!` | The range. |

### getSelection

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSelection(): AccessibilityNodeInfo.Selection?
```

Gets the extended selection, which is a representation of selection that spans multiple nodes that exist within the subtree of the node defining selection.

**Note:** Nodes that are candidates to contain a selection should return `true` from `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#isFocusable()` and `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#isFocused()`. The start and end `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.SelectionPosition`s of this `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.Selection` should exist within `this` node or its descendants.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.Selection?` | The extended selection within the node's subtree, or `null` if no selection exists. |

### getStateDescription

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getStateDescription(): CharSequence?
```

Get the state description of this node.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?` | the state description. This value may be `null`. |

### getStructuredDataInfo

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getStructuredDataInfo(): AccessibilityNodeInfo.StructuredDataInfo?
```

Gets additional structured data properties of this node. This is only populated for nodes that offer additional structured data, like a mathematical expression.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.StructuredDataInfo?` | A concrete subclass of `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.StructuredDataInfo` representing the type and additional structured data for this node, or `null` if this node does not have additional structured data attached. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setStructuredDataInfo(android.view.accessibility.AccessibilityNodeInfo.StructuredDataInfo)`

### getSupplementalDescription

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSupplementalDescription(): CharSequence?
```

Gets the supplemental description of this node. A supplemental description provides brief supplemental information for this node, such as the purpose of the node when that purpose is not conveyed within its textual representation. For example, if a dropdown select has a purpose of setting font family, the supplemental description could be "font family". If this node has children, its supplemental description serves as additional information and is not intended to replace any existing information in the subtree. This is different from the `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getContentDescription()` in that this description is purely supplemental while a content description may be used to replace a description for a node or its subtree that an assistive technology would otherwise compute based on other properties of the node and its descendants.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?` | The supplemental description. This value may be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setSupplementalDescription(kotlin.CharSequence)`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getContentDescription()`

### getText

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getText(): CharSequence!
```

Gets the text of this node.

**Note:** If the text contains `https://developer.android.com/reference/kotlin/android/text/style/ClickableSpan.html#`s or `https://developer.android.com/reference/kotlin/android/text/style/URLSpan.html#`s, these spans will have been replaced with ones whose `https://developer.android.com/reference/kotlin/android/text/style/ClickableSpan.html#onClick(android.view.View)` can be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. When called from a service, the `https://developer.android.com/reference/kotlin/android/view/View.html#` argument is ignored and the corresponding span will be found on the view that this `AccessibilityNodeInfo` represents and called with that view as its argument.

This treatment of `https://developer.android.com/reference/kotlin/android/text/style/ClickableSpan.html#`s means that the text returned from this method may different slightly one passed to `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setText(kotlin.CharSequence)`, although they will be equivalent according to `https://developer.android.com/reference/kotlin/android/text/TextUtils.html#equals(kotlin.CharSequence,%20kotlin.CharSequence)`. The `https://developer.android.com/reference/kotlin/android/text/style/ClickableSpan.html#onClick(android.view.View)` of any spans, however, will generally not work outside of an accessibility service.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!` | The text. |

### getTextSelectionEnd

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTextSelectionEnd(): Int
```

Gets the text selection end if text is selected.

If no text is selected, both this method and `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getTextSelectionStart()` return the same value: the current location of the cursor.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The text selection end, the cursor location if there is no selection, or -1 if there is no text selection and no cursor. |

### getTextSelectionStart

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTextSelectionStart(): Int
```

Gets the text selection start or the cursor position.

If no text is selected, both this method and `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getTextSelectionEnd()` return the same value: the current location of the cursor.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The text selection start, the cursor location if there is no selection, or -1 if there is no text selection and no cursor. |

### getTooltipText

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTooltipText(): CharSequence?
```

Gets the tooltip text of this node.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?` | The tooltip text. This value may be `null`. |

### getTouchDelegateInfo

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTouchDelegateInfo(): AccessibilityNodeInfo.TouchDelegateInfo?
```

Get the `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.TouchDelegateInfo` for touch delegate behavior with the represented view. It is possible for the same node to be pointed to by several regions. Use `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.TouchDelegateInfo#getRegionAt(kotlin.Int)` to get touch delegate target `https://developer.android.com/reference/kotlin/android/graphics/Region.html#`, and `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.TouchDelegateInfo#getTargetForRegion(android.graphics.Region)` for `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#` from the given region.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.TouchDelegateInfo?` | `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.TouchDelegateInfo` or `null` if there are no touch delegates. |

### getTraversalAfter

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTraversalAfter(): AccessibilityNodeInfo!
```

Gets the node after which this one is visited in accessibility traversal. A screen-reader must visit the content of the other node before the content of this one.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#!` | The succeeding node if such or `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setTraversalAfter(android.view.View)`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setTraversalAfter(android.view.View,%20kotlin.Int)`

### getTraversalBefore

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTraversalBefore(): AccessibilityNodeInfo!
```

Gets the node before which this one is visited during traversal. A screen-reader must visit the content of this node before the content of the one it precedes.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#!` | The succeeding node if such or `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setTraversalBefore(android.view.View)`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setTraversalBefore(android.view.View,%20kotlin.Int)`

### getUniqueId

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getUniqueId(): String?
```

Gets the unique id of the node.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | The unique id. This value may be `null`. |

### getViewIdResourceName

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getViewIdResourceName(): String!
```

Gets the fully qualified resource name of the source view's id.

**Note:** The primary usage of this API is for UI test automation and in order to report the source view id of an `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#` the client has to set the `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo.html#FLAG_REPORT_VIEW_IDS:kotlin.Int` flag when configuring the `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | The id resource name. |

### getWindow

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getWindow(): AccessibilityWindowInfo!
```

Gets the window to which this node belongs.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo!` | The window. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#getWindows()`

### getWindowId

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getWindowId(): Int
```

Returns the id of the window that created this node.

**Note:** If this node comes from a window that is embedded in another window using `https://developer.android.com/reference/kotlin/android/view/SurfaceView.html#` then the return value is the id of the window that embeds this node's window.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The window id. |

### hasRequestInitialAccessibilityFocus

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hasRequestInitialAccessibilityFocus(): Boolean
```

Gets whether the node has `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setRequestInitialAccessibilityFocus(kotlin.Boolean)`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the node has requested initial accessibility focus. |

### hashCode

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by `https://developer.android.com/reference/kotlin/java/util/HashMap.html#`.

The general contract of `hashCode` is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the `hashCode` method must consistently return the same integer, provided no information used in `equals` comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce the same integer result.
- It is *not* required that if two objects are unequal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

### isAccessibilityDataSensitive

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isAccessibilityDataSensitive(): Boolean
```

Gets if the node's accessibility data is considered sensitive.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the node's data is considered sensitive, false otherwise. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/View.html#isAccessibilityDataSensitive()`

### isAccessibilityFocused

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isAccessibilityFocused(): Boolean
```

Gets whether this node is accessibility focused.

This is distinct from `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#isFocused()`, which is used to track system focus. See `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_ACCESSIBILITY_FOCUS:kotlin.Int` for details.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the node is accessibility focused. |

### isCheckable

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isCheckable(): Boolean
```

Gets whether this node is checkable.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the node is checkable. |

### isChecked

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isChecked(): Boolean
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getChecked()` instead.*

Gets whether this node is checked. This is only meaningful when `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#isCheckable()` returns `true`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the node is checked. |

### isClickable

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isClickable(): Boolean
```

Gets whether this node is clickable.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the node is clickable. |

### isContentInvalid

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isContentInvalid(): Boolean
```

Gets if the content of this node is invalid. For example, a date is not well-formed.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | If the node content is invalid. |

### isContextClickable

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isContextClickable(): Boolean
```

Gets whether this node is context clickable.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the node is context clickable. |

### isDismissable

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isDismissable(): Boolean
```

Gets if the node can be dismissed.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | If the node can be dismissed. |

### isEditable

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isEditable(): Boolean
```

Gets if the node is editable.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the node is editable, false otherwise. |

### isEnabled

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isEnabled(): Boolean
```

Gets whether this node is enabled.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the node is enabled. |

### isFieldRequired

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isFieldRequired(): Boolean
```

Gets whether a node representing a form field requires input or selection.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if `this` node represents a form field that requires input or selection, `false` otherwise. |

### isFocusable

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isFocusable(): Boolean
```

Gets whether this node is focusable.

In the View system, this typically maps to `https://developer.android.com/reference/kotlin/android/view/View.html#isFocusable()`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the node is focusable. |

### isFocused

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isFocused(): Boolean
```

Gets whether this node is focused.

This is distinct from `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#isAccessibilityFocused()`, which is used by screen readers. See `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_ACCESSIBILITY_FOCUS:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction` for details.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the node is focused. |

### isGranularScrollingSupported

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isGranularScrollingSupported(): Boolean
```

Gets if the node supports granular scrolling.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if all scroll actions that could support `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_ARGUMENT_SCROLL_AMOUNT_FLOAT:kotlin.String` have done so, false otherwise. |

### isHeading

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isHeading(): Boolean
```

Returns whether node represents a heading.

**Note:** Returns `true` if either `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setHeading(kotlin.Boolean)` marks this node as a heading or if the node has a `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.CollectionItemInfo` that marks it as such, to accomodate apps that use the now-deprecated API.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the node is a heading, `false` otherwise. |

### isImportantForAccessibility

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isImportantForAccessibility(): Boolean
```

Returns whether the node originates from a view considered important for accessibility.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the node originates from a view considered important for accessibility, `false` otherwise |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/View.html#isImportantForAccessibility()`

### isLongClickable

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isLongClickable(): Boolean
```

Gets whether this node is long clickable.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the node is long clickable. |

### isMultiLine

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isMultiLine(): Boolean
```

Gets if the node is a multi line editable text.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the node is multi line. |

### isPassword

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isPassword(): Boolean
```

Gets whether this node is a password.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the node is a password. |

### isScreenReaderFocusable

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isScreenReaderFocusable(): Boolean
```

Returns whether the node is explicitly marked as a focusable unit by a screen reader. Note that `false` indicates that it is not explicitly marked, not that the node is not a focusable unit. Screen readers should generally use other signals, such as `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#isFocusable()`, or the presence of text in a node, to determine what should receive focus.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the node is specifically marked as a focusable unit for screen readers, `false` otherwise. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/View.html#isScreenReaderFocusable()`

### isScrollable

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isScrollable(): Boolean
```

Gets if the node is scrollable.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the node is scrollable, false otherwise. |

### isSelected

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isSelected(): Boolean
```

Gets whether this node is selected.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the node is selected. |

### isShowingHintText

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isShowingHintText(): Boolean
```

Returns whether the node's text represents a hint for the user to enter text. It should only be `true` if the node has editable text.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the text in the node represents a hint to the user, `false` otherwise. |

### isTextEntryKey

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isTextEntryKey(): Boolean
```

Returns whether node represents a text entry key that is part of a keyboard or keypad.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the node is a text entry key., `false` otherwise. |

### isTextSelectable

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isTextSelectable(): Boolean
```

Gets if the node has selectable text.

Services should use `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_SET_SELECTION:kotlin.Int` for selection. Editable text nodes must also be selectable. But not all UIs will populate this field, so services should consider 'isTextSelectable | isEditable' to ensure they don't miss nodes with selectable text.
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the node has selectable text. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#isEditable()`

### isVisibleToUser

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isVisibleToUser(): Boolean
```

Gets whether this node is visible to the user.

Between `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#JELLY_BEAN:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int`, this method may incorrectly return false when magnification is enabled. On other versions, a node is considered visible even if it is not on the screen because magnification is active.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Whether the node is visible to the user. |

### obtain

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun obtain(): AccessibilityNodeInfo!
```

**Deprecated:** *Object pooling has been discontinued. Create a new instance using the constructor `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#AccessibilityNodeInfo()` instead.*

Instantiates a new AccessibilityNodeInfo.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#!` | An instance. |

### obtain

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun obtain(info: AccessibilityNodeInfo!): AccessibilityNodeInfo!
```

**Deprecated:** *Object pooling has been discontinued. Create a new instance using the constructor `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#AccessibilityNodeInfo(android.view.accessibility.AccessibilityNodeInfo)` instead.*

Instantiates a new AccessibilityNodeInfo initialized from the given `info`.

| Parameters ||
|---|---|
| `info` | [AccessibilityNodeInfo](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#)!: The other info. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#!` | An instance. |

### obtain

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun obtain(source: View!): AccessibilityNodeInfo!
```

**Deprecated:** *Object pooling has been discontinued. Create a new instance using the constructor `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#AccessibilityNodeInfo(android.view.View)` instead.*

Returns a cached instance if such is available otherwise a new one and sets the source.

| Parameters ||
|---|---|
| `source` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!: The source view. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#!` | An instance. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setSource(android.view.View)`

### obtain

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun obtain(
    root: View!, 
    virtualDescendantId: Int
): AccessibilityNodeInfo!
```

**Deprecated:** *Object pooling has been discontinued. Create a new instance using the constructor `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#AccessibilityNodeInfo(android.view.View,%20kotlin.Int)` instead.*

Returns a cached instance if such is available otherwise a new one and sets the source.

| Parameters ||
|---|---|
| `root` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!: The root of the virtual subtree. |
| `virtualDescendantId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the virtual descendant. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#!` | An instance. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setSource(android.view.View,%20kotlin.Int)`

### performAction

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun performAction(action: Int): Boolean
```

Performs an action on the node.

**Note:** An action can be performed only if the request is made from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`.

| Parameters ||
|---|---|
| `action` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The action to perform. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the action was performed. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If called outside of an AccessibilityService. |

### performAction

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun performAction(
    action: Int, 
    arguments: Bundle!
): Boolean
```

Performs an action on the node.

**Note:** An action can be performed only if the request is made from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`.

| Parameters ||
|---|---|
| `action` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The action to perform. |
| `arguments` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!: A bundle with additional arguments. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the action was performed. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If called outside of an AccessibilityService. |

### recycle

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun recycle(): Unit
```

**Deprecated:** *Object pooling has been discontinued. Calling this function now will have no effect.*

Would previously return an instance back to be reused.

### refresh

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun refresh(): Boolean
```

Refreshes this info with the latest state of the view it represents.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the refresh succeeded. `false` if the `https://developer.android.com/reference/kotlin/android/view/View.html#` represented by this node is no longer in the view tree (and thus this node is obsolete). |

### refreshWithExtraData

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun refreshWithExtraData(
    extraDataKey: String!, 
    args: Bundle!
): Boolean
```

Refreshes this info with the latest state of the view it represents, and request new data be added by the View.

| Parameters ||
|---|---|
| `extraDataKey` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The extra data requested. Data that must be requested with this mechanism is generally expensive to retrieve, so should only be requested when needed. See `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#EXTRA_DATA_RENDERING_INFO_KEY:kotlin.String`, `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#EXTRA_DATA_TEXT_CHARACTER_LOCATION_KEY:kotlin.String`, `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getAvailableExtraData()` and `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getExtraRenderingInfo()`. |
| `args` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!: A bundle of arguments for the request. These depend on the particular request. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the refresh succeeded. `false` if the `https://developer.android.com/reference/kotlin/android/view/View.html#` represented by this node is no longer in the view tree (and thus this node is obsolete). |

### removeAction

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeAction(action: AccessibilityNodeInfo.AccessibilityAction!): Boolean
```

Removes an action that can be performed on the node. If the action was not already added to the node, calling this method has no effect.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService.

| Parameters ||
|---|---|
| `action` | [AccessibilityNodeInfo.AccessibilityAction](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction)!: The action to be removed. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | The action removed from the list of actions. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If called from an AccessibilityService. |

### removeAction

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeAction(action: Int): Unit
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#removeAction(android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction)`*

Removes an action that can be performed on the node. If the action was not already added to the node, calling this method has no effect.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService.

| Parameters ||
|---|---|
| `action` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The action to be removed. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If called from an AccessibilityService. |

### removeChild

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeChild(child: View!): Boolean
```

Removes a child. If the child was not previously added to the node, calling this method has no effect.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService.

| Parameters ||
|---|---|
| `child` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!: The child. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the child was present |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If called from an AccessibilityService. |

### removeChild

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeChild(
    root: View!, 
    virtualDescendantId: Int
): Boolean
```

Removes a virtual child which is a descendant of the given `root`. If the child was not previously added to the node, calling this method has no effect.

| Parameters ||
|---|---|
| `root` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!: The root of the virtual subtree. |
| `virtualDescendantId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the virtual child. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the child was present |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#addChild(android.view.View,%20kotlin.Int)`

### removeLabeledBy

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeLabeledBy(label: View): Boolean
```

Removes a label. If the label was not previously added to the node, calling this method has no effect.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService.

| Parameters ||
|---|---|
| `label` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#): The node which serves as this node's label. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the label was present |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#addLabeledBy(android.view.View)`

### removeLabeledBy

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeLabeledBy(
    root: View, 
    virtualDescendantId: Int
): Boolean
```

Removes a label which is a virtual descendant of the given `root`. If `virtualDescendantId` is `https://developer.android.com/reference/kotlin/android/view/View.html#NO_ID:kotlin.Int` the root is set as the label. If the label was not previously added to the node, calling this method has no effect.

| Parameters ||
|---|---|
| `root` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#): The root of the virtual subtree. This value cannot be `null`. |
| `virtualDescendantId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the virtual node which serves as this node's label. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the label was present |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#addLabeledBy(android.view.View,%20kotlin.Int)`

### setAccessibilityDataSensitive

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setAccessibilityDataSensitive(accessibilityDataSensitive: Boolean): Unit
```

Sets whether this node's accessibility data is considered sensitive.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService.

| Parameters ||
|---|---|
| `accessibilityDataSensitive` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): True if the node's accessibility data is considered sensitive. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If called from an AccessibilityService. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/View.html#setAccessibilityDataSensitive(kotlin.Int)`

### setAccessibilityFocused

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setAccessibilityFocused(focused: Boolean): Unit
```

Sets whether this node is accessibility focused.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService.

The UI element updating this property should send an event of `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_ACCESSIBILITY_FOCUSED:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_ACCESSIBILITY_FOCUS_CLEARED:kotlin.Int` if its accessibility-focused state changes.

| Parameters ||
|---|---|
| `focused` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): True if the node is accessibility focused. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If called from an AccessibilityService. |

### setAvailableExtraData

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setAvailableExtraData(extraDataKeys: MutableList<String!>!): Unit
```

Set the extra data available for this node.

**Note:** When a `View` passes in a non-empty list, it promises that it will populate the node's extras with corresponding pieces of information in `https://developer.android.com/reference/kotlin/android/view/View.html#addExtraDataToAccessibilityNodeInfo(android.view.accessibility.AccessibilityNodeInfo,%20kotlin.String,%20android.os.Bundle)`.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService.

| Parameters ||
|---|---|
| `extraDataKeys` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!: A list of types of extra data that are available. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If called from an AccessibilityService. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getAvailableExtraData()`

### setBoundsInParent

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setBoundsInParent(bounds: Rect!): Unit
```

**Deprecated:** *Accessibility services should not care about these bounds.*

Sets the node bounds in the viewParent's coordinates. `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getParent()` does not represent the source's viewParent. Instead it represents the result of `https://developer.android.com/reference/kotlin/android/view/View.html#getParentForAccessibility()`, which returns the closest ancestor where `https://developer.android.com/reference/kotlin/android/view/View.html#isImportantForAccessibility()` is true. So this method is not reliable.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService.

| Parameters ||
|---|---|
| `bounds` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)!: The node bounds. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If called from an AccessibilityService. |

### setBoundsInScreen

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setBoundsInScreen(bounds: Rect!): Unit
```

Sets the node bounds in screen coordinates.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService.

| Parameters ||
|---|---|
| `bounds` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)!: The node bounds. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If called from an AccessibilityService. |

### setBoundsInWindow

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setBoundsInWindow(bounds: Rect): Unit
```

Sets the node bounds in window coordinates.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService.

| Parameters ||
|---|---|
| `bounds` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#): The node bounds. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If called from an AccessibilityService. |

### setCanOpenPopup

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setCanOpenPopup(opensPopup: Boolean): Unit
```

Sets if this node opens a popup or a dialog.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService.

| Parameters ||
|---|---|
| `opensPopup` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): If the the node opens a popup. |

### setCheckable

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setCheckable(checkable: Boolean): Unit
```

Sets whether this node is checkable.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService.

| Parameters ||
|---|---|
| `checkable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): True if the node is checkable. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If called from an AccessibilityService. |

### setChecked

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setChecked(checked: Boolean): Unit
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setChecked(kotlin.Int)` instead.*

Sets whether this node is checked. This is only meaningful when `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#isCheckable()` returns `true`.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService.

| Parameters ||
|---|---|
| `checked` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): True if the node is checked. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If called from an AccessibilityService. |

### setChecked

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setChecked(checked: Int): Unit
```

Sets the checked state of this node. This is only meaningful when `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#isCheckable()` returns `true`.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService.

| Parameters ||
|---|---|
| `checked` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The checked state. One of - `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#CHECKED_STATE_FALSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#CHECKED_STATE_TRUE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#CHECKED_STATE_PARTIAL:kotlin.Int` . Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#CHECKED_STATE_FALSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#CHECKED_STATE_TRUE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#CHECKED_STATE_PARTIAL:kotlin.Int` |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if checked is not one of `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#CHECKED_STATE_FALSE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#CHECKED_STATE_TRUE:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#CHECKED_STATE_PARTIAL:kotlin.Int`. |
| `java.lang.IllegalStateException` | If called from an AccessibilityService. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setCheckable(kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#isCheckable()`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getChecked()`

### setClassName

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setClassName(className: CharSequence!): Unit
```

Sets the class this node comes from.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService.

| Parameters ||
|---|---|
| `className` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: The class name. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If called from an AccessibilityService. |

### setClickable

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setClickable(clickable: Boolean): Unit
```

Sets whether this node is clickable.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService.

| Parameters ||
|---|---|
| `clickable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): True if the node is clickable. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If called from an AccessibilityService. |

### setCollectionInfo

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setCollectionInfo(collectionInfo: AccessibilityNodeInfo.CollectionInfo!): Unit
```

Sets the collection info if the node is a collection. A collection child is always a collection item.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService.

| Parameters ||
|---|---|
| `collectionInfo` | [AccessibilityNodeInfo.CollectionInfo](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.CollectionInfo)!: The collection info. |

### setCollectionItemInfo

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setCollectionItemInfo(collectionItemInfo: AccessibilityNodeInfo.CollectionItemInfo!): Unit
```

Sets the collection item info if the node is a collection item. A collection item is always a child of a collection.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService.

### setContainerTitle

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setContainerTitle(containerTitle: CharSequence?): Unit
```

Sets the container title for app-developer-defined container which can be any type of ViewGroup or layout. Container title will be used to group together related controls, similar to HTML fieldset. Or container title may identify a large piece of the UI that is visibly grouped together, such as a toolbar or a card, etc.

Container title helps to assist in navigation across containers and other groups. For example, a screen reader may use this to determine where to put accessibility focus.

Container title is different from pane title`https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setPaneTitle(kotlin.CharSequence)` which indicates that the node represents a window or activity.

Example: An app can set container titles on several non-modal menus, containing TextViews or ImageButtons that have content descriptions, text, etc. Screen readers can quickly switch accessibility focus among menus instead of child views. Other accessibility-services can easily find the menu.

| Parameters ||
|---|---|
| `containerTitle` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?: The container title that is associated with a ViewGroup/Layout on the screen. This value may be `null`. |

### setContentDescription

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setContentDescription(contentDescription: CharSequence!): Unit
```

Sets the content description of this node.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService.

| Parameters ||
|---|---|
| `contentDescription` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: The content description. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If called from an AccessibilityService. |

### setContentInvalid

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setContentInvalid(contentInvalid: Boolean): Unit
```

Sets if the content of this node is invalid. For example, a date is not well-formed.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService.

| Parameters ||
|---|---|
| `contentInvalid` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): If the node content is invalid. |

### setContextClickable

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setContextClickable(contextClickable: Boolean): Unit
```

Sets whether this node is context clickable.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService.

| Parameters ||
|---|---|
| `contextClickable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): True if the node is context clickable. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If called from an AccessibilityService. |

### setDismissable

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setDismissable(dismissable: Boolean): Unit
```

Sets if the node can be dismissed.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService.

| Parameters ||
|---|---|
| `dismissable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): If the node can be dismissed. |

### setDrawingOrder

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setDrawingOrder(drawingOrderInParent: Int): Unit
```

Set the drawing order of the view corresponding it this node.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService.

| Parameters ||
|---|---|
| `drawingOrderInParent` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If called from an AccessibilityService. |

### setEditable

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setEditable(editable: Boolean): Unit
```

Sets whether this node is editable.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService.

| Parameters ||
|---|---|
| `editable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): True if the node is editable. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If called from an AccessibilityService. |

### setEnabled

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setEnabled(enabled: Boolean): Unit
```

Sets whether this node is enabled.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService.

| Parameters ||
|---|---|
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): True if the node is enabled. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If called from an AccessibilityService. |

### setError

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setError(error: CharSequence!): Unit
```

Sets the error text of this node.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService.

| Parameters ||
|---|---|
| `error` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: The error text. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If called from an AccessibilityService. |

### setExpandedState

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setExpandedState(state: Int): Unit
```

Sets the expanded state of the node.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`.

| Parameters ||
|---|---|
| `state` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): new expanded state of this node. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#EXPANDED_STATE_UNDEFINED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#EXPANDED_STATE_COLLAPSED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#EXPANDED_STATE_PARTIAL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#EXPANDED_STATE_FULL:kotlin.Int` |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If state is not one of: - `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#EXPANDED_STATE_UNDEFINED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#EXPANDED_STATE_COLLAPSED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#EXPANDED_STATE_PARTIAL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#EXPANDED_STATE_FULL:kotlin.Int` |
| `java.lang.IllegalStateException` | If called from an AccessibilityService |

### setExtraRenderingInfo

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setExtraRenderingInfo(extraRenderingInfo: AccessibilityNodeInfo.ExtraRenderingInfo?): Unit
```

Sets the extra rendering info, `extraRenderingInfo, if the node is meant to be refreshed with extra data.
`

`` Note: Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService. ``
`
`

<br />

| Parameters ||
|---|---|
| `extraRenderingInfo` | [AccessibilityNodeInfo.ExtraRenderingInfo](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.ExtraRenderingInfo)?: The `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.ExtraRenderingInfo`, or `null` to remove a previously set value. |

### setFieldRequired

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setFieldRequired(required: Boolean): Unit
```

Sets whether `this` node represents a form field that requires input or selection.

**Note:** Cannot be called from an AccessibilityService. This class is made immutable before being delivered to an AccessibilityService.

| Parameters ||
|---|---|
| `required` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): `true` if input or selection of this node should be required, `false` otherwise. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If called from an AccessibilityService |

### setFocusable

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setFocusable(focusable: Boolean): Unit
```

Sets whether this node is focusable.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService.

To mark a node as explicitly focusable for a screen reader, consider using `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setScreenReaderFocusable(kotlin.Boolean)` instead.

| Parameters ||
|---|---|
| `focusable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): True if the node is focusable. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If called from an AccessibilityService. |

### setFocused

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setFocused(focused: Boolean): Unit
```

Sets whether this node is focused.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService.

| Parameters ||
|---|---|
| `focused` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): True if the node is focused. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If called from an AccessibilityService. |

### setGranularScrollingSupported

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setGranularScrollingSupported(granularScrollingSupported: Boolean): Unit
```

Sets if the node supports granular scrolling. This should be set to true if all scroll actions which could support `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_ARGUMENT_SCROLL_AMOUNT_FLOAT:kotlin.String` have done so.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService.

| Parameters ||
|---|---|
| `granularScrollingSupported` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): True if the node supports granular scrolling, false otherwise. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If called from an AccessibilityService. |

### setHeading

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setHeading(isHeading: Boolean): Unit
```

Sets whether the node represents a heading.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService.

| Parameters ||
|---|---|
| `isHeading` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): `true` if the node is a heading, `false` otherwise. |

### setHintText

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setHintText(hintText: CharSequence!): Unit
```

Sets the hint text of this node. Only applies to nodes where text can be entered.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService.

| Parameters ||
|---|---|
| `hintText` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: The hint text for this mode. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If called from an AccessibilityService. |

### setImportantForAccessibility

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setImportantForAccessibility(important: Boolean): Unit
```

Sets whether the node is considered important for accessibility.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService.

| Parameters ||
|---|---|
| `important` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): `true` if the node is considered important for accessibility, `false` otherwise |

### setInputType

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setInputType(inputType: Int): Unit
```

Sets the input type of the source as defined by `https://developer.android.com/reference/kotlin/android/text/InputType.html#`.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService.

| Parameters ||
|---|---|
| `inputType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The input type. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If called from an AccessibilityService. |

### setLabelFor

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setLabelFor(labeled: View!): Unit
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#addLabeledBy(android.view.View)` on the labeled node instead, since `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getLabeledByList()` and `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getLabeledBy()` on the labeled node are not automatically populated when this method is used.*

Sets the view for which the view represented by this info serves as a label for accessibility purposes.

| Parameters ||
|---|---|
| `labeled` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!: The view for which this info serves as a label. |

### setLabelFor

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setLabelFor(
    root: View!, 
    virtualDescendantId: Int
): Unit
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#addLabeledBy(android.view.View)` on the labeled node instead, since `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getLabeledByList()` and `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getLabeledBy()` on the labeled node are not automatically populated when this method is used.*

Sets the view for which the view represented by this info serves as a label for accessibility purposes. If `virtualDescendantId` is `https://developer.android.com/reference/kotlin/android/view/View.html#NO_ID:kotlin.Int` the root is set as the labeled.

A virtual descendant is an imaginary View that is reported as a part of the view hierarchy for accessibility purposes. This enables custom views that draw complex content to report themselves as a tree of virtual views, thus conveying their logical structure.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService.

| Parameters ||
|---|---|
| `root` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!: The root whose virtual descendant serves as a label. |
| `virtualDescendantId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the virtual descendant. |

### setLabeledBy

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setLabeledBy(label: View!): Unit
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#addLabeledBy(android.view.View)` or `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#removeLabeledBy(android.view.View)` instead.*

Sets the view which serves as the label of the view represented by this info for accessibility purposes.

| Parameters ||
|---|---|
| `label` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!: The view that labels this node's source. |

### setLabeledBy

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setLabeledBy(
    root: View!, 
    virtualDescendantId: Int
): Unit
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#addLabeledBy(android.view.View,%20kotlin.Int)` or `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#removeLabeledBy(android.view.View,%20kotlin.Int)` instead.*

Sets the view which serves as the label of the view represented by this info for accessibility purposes. If `virtualDescendantId` is `https://developer.android.com/reference/kotlin/android/view/View.html#NO_ID:kotlin.Int` the root is set as the label.

A virtual descendant is an imaginary View that is reported as a part of the view hierarchy for accessibility purposes. This enables custom views that draw complex content to report themselves as a tree of virtual views, thus conveying their logical structure.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService.

| Parameters ||
|---|---|
| `root` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!: The root whose virtual descendant labels this node's source. |
| `virtualDescendantId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the virtual descendant. |

### setLiveRegion

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setLiveRegion(mode: Int): Unit
```

Sets the node's live region mode.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService.

| Parameters ||
|---|---|
| `mode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The live region mode, or `https://developer.android.com/reference/kotlin/android/view/View.html#ACCESSIBILITY_LIVE_REGION_NONE:kotlin.Int` if the view is not a live region. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/View.html#setAccessibilityLiveRegion(kotlin.Int)`

### setLongClickable

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setLongClickable(longClickable: Boolean): Unit
```

Sets whether this node is long clickable.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService.

| Parameters ||
|---|---|
| `longClickable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): True if the node is long clickable. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If called from an AccessibilityService. |

### setMaxTextLength

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setMaxTextLength(max: Int): Unit
```

Sets the maximum text length, or -1 for no limit.

Typically used to indicate that an editable text field has a limit on the number of characters entered.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService.

| Parameters ||
|---|---|
| `max` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The maximum text length. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If called from an AccessibilityService. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getMaxTextLength()`

### setMinDurationBetweenContentChanges

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setMinDurationBetweenContentChanges(duration: Duration): Unit
```

Sets the minimum time duration between two content change events, which is used in throttling content change events in accessibility services.

Example: An app can set MinMillisBetweenContentChanges as 1 min for a view which sends content change events to accessibility services one event per second. Accessibility service will throttle those content change events and only handle one event per minute for that view.

Example UI elements that frequently update and may benefit from a duration are progress bars, timers, and stopwatches.

| Parameters ||
|---|---|
| `duration` | [Duration](https://developer.android.com/reference/kotlin/java/time/Duration.html#): the minimum duration between content change events. Negative duration would be treated as zero. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOW_CONTENT_CHANGED:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getContentChangeTypes()`

### setMovementGranularities

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setMovementGranularities(granularities: Int): Unit
```

Sets the movement granularities for traversing the text of this node.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService.

| Parameters ||
|---|---|
| `granularities` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The bit mask with granularities. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If called from an AccessibilityService. |

### setMultiLine

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setMultiLine(multiLine: Boolean): Unit
```

Sets if the node is a multi line editable text.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService.

| Parameters ||
|---|---|
| `multiLine` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): True if the node is multi line. |

### setPackageName

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setPackageName(packageName: CharSequence!): Unit
```

Sets the package this node comes from.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService.

| Parameters ||
|---|---|
| `packageName` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: The package name. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If called from an AccessibilityService. |

### setPaneTitle

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setPaneTitle(paneTitle: CharSequence?): Unit
```

If this node represents a visually distinct region of the screen that may update separately from the rest of the window, it is considered a pane. Set the pane title to indicate that the node is a pane, and to provide a title for it.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService.

| Parameters ||
|---|---|
| `paneTitle` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?: The title of the pane represented by this node. This value may be `null`. |

### setParent

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setParent(parent: View!): Unit
```

Sets the parent.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService.

| Parameters ||
|---|---|
| `parent` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!: The parent. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If called from an AccessibilityService. |

### setParent

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setParent(
    root: View!, 
    virtualDescendantId: Int
): Unit
```

Sets the parent to be a virtual descendant of the given `root`. If `virtualDescendantId` equals to `https://developer.android.com/reference/kotlin/android/view/View.html#NO_ID:kotlin.Int` the root is set as the parent.

A virtual descendant is an imaginary View that is reported as a part of the view hierarchy for accessibility purposes. This enables custom views that draw complex content to report them selves as a tree of virtual views, thus conveying their logical structure.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService.

| Parameters ||
|---|---|
| `root` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!: The root of the virtual subtree. |
| `virtualDescendantId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the virtual descendant. |

### setPassword

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setPassword(password: Boolean): Unit
```

Sets whether this node is a password.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService.

| Parameters ||
|---|---|
| `password` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): True if the node is a password. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If called from an AccessibilityService. |

### setQueryFromAppProcessEnabled

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setQueryFromAppProcessEnabled(
    view: View, 
    enabled: Boolean
): Unit
```

Connects this node to the View's root so that operations on this node can query the entire `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#` tree and perform accessibility actions on nodes.

Testing or debugging tools should create this `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#` node using `https://developer.android.com/reference/kotlin/android/view/View.html#createAccessibilityNodeInfo()` or `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeProvider` and call this method, then navigate and interact with the node tree by calling methods on the node. Calling this method more than once on the same node is a no-op. After calling this method, all nodes linked to this node (children, ancestors, etc.) are also queryable.

Here "query" refers to the following node operations:
- check properties of this node (example: `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#isScrollable()`)
- find and query children (example: `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getChild(kotlin.Int)`)
- find and query the parent (example: `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getParent()`)
- find focus (examples: `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#findFocus(kotlin.Int)`, `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#focusSearch(kotlin.Int)`)
- find and query other nodes (example: `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#findAccessibilityNodeInfosByText(kotlin.String)`, `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#findAccessibilityNodeInfosByViewId(kotlin.String)`)
- perform actions (example: `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#performAction(kotlin.Int)`)
- This is intended for short-lived inspections from testing or debugging tools in the app process, as operations on this node tree will only succeed as long as the associated view hierarchy remains attached to a window. `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#` objects can quickly become out of sync with their corresponding `https://developer.android.com/reference/kotlin/android/view/View.html#` objects; if you wish to inspect a changed or different view hierarchy then create a new node from any view in that hierarchy and call this method on that new node, instead of disabling \& re-enabling the connection on the previous node.

| Parameters ||
|---|---|
| `view` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#): The view that generated this node, or any view in the same view-root hierarchy. This value cannot be `null`. |
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Whether to enable (true) or disable (false) querying from the app process. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`, or if provided a `https://developer.android.com/reference/kotlin/android/view/View.html#` that is not attached to a window. |

### setRangeInfo

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setRangeInfo(rangeInfo: AccessibilityNodeInfo.RangeInfo!): Unit
```

Sets the range info if this node is a range.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService.

| Parameters ||
|---|---|
| `rangeInfo` | [AccessibilityNodeInfo.RangeInfo](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.RangeInfo)!: The range info. |

### setRequestInitialAccessibilityFocus

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setRequestInitialAccessibilityFocus(requestInitialAccessibilityFocus: Boolean): Unit
```

Sets whether the node has requested initial accessibility focus.

If the node `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#hasRequestInitialAccessibilityFocus()`, this node would be one of candidates to be accessibility focused when the window appears.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService.

| Parameters ||
|---|---|
| `requestInitialAccessibilityFocus` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): True if the node requests to receive initial accessibility focus. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If called from an AccessibilityService. |

### setScreenReaderFocusable

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setScreenReaderFocusable(screenReaderFocusable: Boolean): Unit
```

Sets whether the node should be considered a focusable unit by a screen reader.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService.

This can be used to [group related content.](https://developer.android.com/guide/topics/ui/accessibility/principles#content-groups)

| Parameters ||
|---|---|
| `screenReaderFocusable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): `true` if the node is a focusable unit for screen readers, `false` otherwise. |

### setScrollable

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setScrollable(scrollable: Boolean): Unit
```

Sets if the node is scrollable.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService.

| Parameters ||
|---|---|
| `scrollable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): True if the node is scrollable, false otherwise. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If called from an AccessibilityService. |

### setSelected

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setSelected(selected: Boolean): Unit
```

Sets whether this node is selected.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService.

| Parameters ||
|---|---|
| `selected` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): True if the node is selected. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If called from an AccessibilityService. |

### setSelection

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setSelection(selection: AccessibilityNodeInfo.Selection?): Unit
```

Sets the extended selection, which is a representation of selection that spans multiple nodes that exist within the subtree of the node defining selection.

**Note:** The start and end `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.SelectionPosition` of the provided `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.Selection` should be constructed with `this` node or a descendant of it.

**Note:** `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setFocusable(kotlin.Boolean)` and `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setFocused(kotlin.Boolean)` should both be called with `true` before setting the selection in order to make `this` node a candidate to contain a selection.

**Note:** Cannot be called from an AccessibilityService. This class is made immutable before being delivered to an AccessibilityService.

| Parameters ||
|---|---|
| `selection` | [AccessibilityNodeInfo.Selection](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.Selection)?: The extended selection within the node's subtree, or `null` if no selection exists. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If called from an AccessibilityService |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_SET_EXTENDED_SELECTION:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction`

### setShowingHintText

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setShowingHintText(showingHintText: Boolean): Unit
```

Sets whether the node's text represents a hint for the user to enter text. It should only be `true` if the node has editable text.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService.

| Parameters ||
|---|---|
| `showingHintText` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): `true` if the text in the node represents a hint to the user, `false` otherwise. |

### setSource

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setSource(source: View!): Unit
```

Sets the source.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService.

| Parameters ||
|---|---|
| `source` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!: The info source. |

### setSource

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setSource(
    root: View!, 
    virtualDescendantId: Int
): Unit
```

Sets the source to be a virtual descendant of the given `root`. If `virtualDescendantId` is `https://developer.android.com/reference/kotlin/android/view/View.html#NO_ID:kotlin.Int` the root is set as the source.

A virtual descendant is an imaginary View that is reported as a part of the view hierarchy for accessibility purposes. This enables custom views that draw complex content to report themselves as a tree of virtual views, thus conveying their logical structure.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService.

| Parameters ||
|---|---|
| `root` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!: The root of the virtual subtree. |
| `virtualDescendantId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the virtual descendant. |

### setStateDescription

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setStateDescription(stateDescription: CharSequence?): Unit
```

Sets the state description of this node.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService.

| Parameters ||
|---|---|
| `stateDescription` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?: the state description of this node. This value may be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If called from an AccessibilityService. |

### setStructuredDataInfo

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setStructuredDataInfo(info: AccessibilityNodeInfo.StructuredDataInfo?): Unit
```

Sets additional structured data properties of this node, such as for a mathematical expression.

| Parameters ||
|---|---|
| `info` | [AccessibilityNodeInfo.StructuredDataInfo](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.StructuredDataInfo)?: The `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.StructuredDataInfo` object (e.g., an instance of `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.MathInfo`) describing the node. This value may be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getStructuredDataInfo()`

### setSupplementalDescription

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setSupplementalDescription(supplementalDescription: CharSequence?): Unit
```

Sets the supplemental description of this node. A supplemental description provides brief supplemental information for this node, such as the purpose of the node when that purpose is not conveyed within its textual representation. For example, if a dropdown select has a purpose of setting font family, the supplemental description could be "font family". If this node has children, its supplemental description serves as additional information and is not intended to replace any existing information in the subtree. This is different from the `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setContentDescription(kotlin.CharSequence)` in that this description is purely supplemental while a content description may be used to replace a description for a node or its subtree that an assistive technology would otherwise compute based on other properties of the node and its descendants.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService.

| Parameters ||
|---|---|
| `supplementalDescription` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?: The supplemental description. This value may be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If called from an AccessibilityService. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getSupplementalDescription()`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setContentDescription(kotlin.CharSequence)`

### setText

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setText(text: CharSequence!): Unit
```

Sets the text of this node.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService.

| Parameters ||
|---|---|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: The text. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If called from an AccessibilityService. |

### setTextEntryKey

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTextEntryKey(isTextEntryKey: Boolean): Unit
```

Sets whether the node represents a text entry key that is part of a keyboard or keypad.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService.

| Parameters ||
|---|---|
| `isTextEntryKey` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): `true` if the node is a text entry key, `false` otherwise. |

### setTextSelectable

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTextSelectable(selectableText: Boolean): Unit
```

Sets if the node has selectable text.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService.

| Parameters ||
|---|---|
| `selectableText` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): True if the node has selectable text, false otherwise. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If called from an AccessibilityService. |

### setTextSelection

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTextSelection(
    start: Int, 
    end: Int
): Unit
```

Sets the text selection start and end.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService.

| Parameters ||
|---|---|
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The text selection start. |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The text selection end. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If called from an AccessibilityService. |

### setTooltipText

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTooltipText(tooltipText: CharSequence?): Unit
```

Sets the tooltip text of this node.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService.

| Parameters ||
|---|---|
| `tooltipText` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?: The tooltip text. This value may be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If called from an AccessibilityService. |

### setTouchDelegateInfo

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTouchDelegateInfo(delegatedInfo: AccessibilityNodeInfo.TouchDelegateInfo): Unit
```

Set touch delegate info if the represented view has a `https://developer.android.com/reference/kotlin/android/view/TouchDelegate.html#`.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService.

| Parameters ||
|---|---|
| `delegatedInfo` | [AccessibilityNodeInfo.TouchDelegateInfo](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.TouchDelegateInfo): `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.TouchDelegateInfo` returned from `https://developer.android.com/reference/kotlin/android/view/TouchDelegate.html#getTouchDelegateInfo()`. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If called from an AccessibilityService. |

### setTraversalAfter

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTraversalAfter(view: View!): Unit
```

Sets the view whose node is visited after this one in accessibility traversal. A screen-reader must visit the content of the other node before the content of this one.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService.

| Parameters ||
|---|---|
| `view` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!: The previous view. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getTraversalAfter()`

### setTraversalAfter

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTraversalAfter(
    root: View!, 
    virtualDescendantId: Int
): Unit
```

Sets the node after which this one is visited in accessibility traversal. A screen-reader must visit the content of the other node before the content of this one. If `virtualDescendantId` equals to `https://developer.android.com/reference/kotlin/android/view/View.html#NO_ID:kotlin.Int` the root is set as the predecessor.

A virtual descendant is an imaginary View that is reported as a part of the view hierarchy for accessibility purposes. This enables custom views that draw complex content to report them selves as a tree of virtual views, thus conveying their logical structure.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService.

| Parameters ||
|---|---|
| `root` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!: The root of the virtual subtree. |
| `virtualDescendantId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the virtual descendant. |

### setTraversalBefore

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTraversalBefore(view: View!): Unit
```

Sets the view before whose node this one should be visited during traversal. A screen-reader must visit the content of this node before the content of the one it precedes.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService.

| Parameters ||
|---|---|
| `view` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!: The view providing the preceding node. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getTraversalBefore()`

### setTraversalBefore

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTraversalBefore(
    root: View!, 
    virtualDescendantId: Int
): Unit
```

Sets the node before which this one is visited during traversal. A screen-reader must visit the content of this node before the content of the one it precedes. The successor is a virtual descendant of the given `root`. If `virtualDescendantId` equals to `https://developer.android.com/reference/kotlin/android/view/View.html#NO_ID:kotlin.Int` the root is set as the successor.

A virtual descendant is an imaginary View that is reported as a part of the view hierarchy for accessibility purposes. This enables custom views that draw complex content to report them selves as a tree of virtual views, thus conveying their logical structure.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService.

| Parameters ||
|---|---|
| `root` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!: The root of the virtual subtree. |
| `virtualDescendantId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of the virtual descendant. |

### setUniqueId

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setUniqueId(uniqueId: String?): Unit
```

Sets the unique id to act as a key to identify the node. If the node instance is replaced after refreshing the layout, calling this API to assign the same unique id to the new alike node can help accessibility service to identify it.

| Parameters ||
|---|---|
| `uniqueId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: The unique id that is associated with a visible node on the screen. This value may be `null`. |

### setViewIdResourceName

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setViewIdResourceName(viewIdResName: String!): Unit
```

Sets the fully qualified resource name of the source view's id.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService.

| Parameters ||
|---|---|
| `viewIdResName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The id resource name. |

### setVisibleToUser

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setVisibleToUser(visibleToUser: Boolean): Unit
```

Sets whether this node is visible to the user.

**Note:** Cannot be called from an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#`. This class is made immutable before being delivered to an AccessibilityService.

| Parameters ||
|---|---|
| `visibleToUser` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Whether the node is visible to the user. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If called from an AccessibilityService. |

### toString

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun writeToParcel(
    parcel: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

**Note:** After the instance is written to a parcel it is recycled. You must not touch the object after calling this function.

| Parameters ||
|---|---|
| `dest` | The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<AccessibilityNodeInfo!>
```
**See Also**

- `https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#`
