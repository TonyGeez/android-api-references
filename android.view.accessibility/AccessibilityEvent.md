# AccessibilityEvent

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AccessibilityEvent

Kotlin| [Java](../android/view/accessibility/AccessibilityEvent.md) 
| --- | --- |

```
class AccessibilityEvent : AccessibilityRecord, Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.view.accessibility.AccessibilityRecord](../android/view/accessibility/AccessibilityRecord.md) ||
| | ↳ | [android.view.accessibility.AccessibilityEvent](../android/view/accessibility/AccessibilityEvent.md) |

This class represents accessibility events that are sent by the system when something notable happens in the user interface. For example, when a [android.widget.Button](../android/widget/Button.md) is clicked, a [android.view.View](../android/view/View.md) is focused, etc.

An accessibility event is fired by an individual view which populates the event with data for its state and requests from its parent to send the event to interested parties. The parent can optionally modify or even block the event based on its broader understanding of the user interface's context.

The main purpose of an accessibility event is to communicate changes in the UI to an [android.accessibilityservice.AccessibilityService](../android/accessibilityservice/AccessibilityService.md). If needed, the service may then inspect the user interface by examining the View hierarchy through the event's [source](../android/view/accessibility/AccessibilityRecord.md)), as represented by a tree of [AccessibilityNodeInfo](../android/view/accessibility/AccessibilityNodeInfo.md) s (snapshot of a View state) which can be used for exploring the window content. Note that the privilege for accessing an event's source, thus the window content, has to be explicitly requested. For more details refer to [android.accessibilityservice.AccessibilityService](../android/accessibilityservice/AccessibilityService.md). If an accessibility service has not requested to retrieve the window content the event will not contain reference to its source.**Note:** for events of type [TYPE_NOTIFICATION_STATE_CHANGED](../android/view/accessibility/AccessibilityEvent.md) the source is never available, and Views that set [android.view.View#isAccessibilityDataSensitive()](../android/view/View.md))may not populate all event properties on events sent from higher up in the view hierarchy.

This class represents various semantically different accessibility event types. Each event type has an associated set of related properties. In other words, each event type is characterized via a subset of the properties exposed by this class. For each event type there is a corresponding constant defined in this class. Follows a specification of the event types and their associated properties:
|
| ### Developer Guides
|
| For more information about creating and processing AccessibilityEvents, read the [Accessibility](https://developer.android.com/guide/topics/ui/accessibility/index.html) developer guide.

**VIEW TYPES** 

**View clicked** - represents the event of clicking on a [android.view.View](../android/view/View.md) like [android.widget.Button](../android/widget/Button.md), [android.widget.CompoundButton](../android/widget/CompoundButton.md), etc. 
*Type:* [TYPE_VIEW_CLICKED](../android/view/accessibility/AccessibilityEvent.md) 
*Properties:* 

- [getEventType()](../android/view/accessibility/AccessibilityEvent.md))- The type of the event.
- [getSource()](../android/view/accessibility/AccessibilityRecord.md))- The source info (for registered clients).
- [getClassName()](../android/view/accessibility/AccessibilityRecord.md))- The class name of the source.
- [getPackageName()](../android/view/accessibility/AccessibilityEvent.md))- The package name of the source.
- [getEventTime()](../android/view/accessibility/AccessibilityEvent.md))- The event time.

<br />

**View long clicked** - represents the event of long clicking on a [android.view.View](../android/view/View.md) like [android.widget.Button](../android/widget/Button.md), [android.widget.CompoundButton](../android/widget/CompoundButton.md), etc 
*Type:* [TYPE_VIEW_LONG_CLICKED](../android/view/accessibility/AccessibilityEvent.md) 
*Properties:* 

- [getEventType()](../android/view/accessibility/AccessibilityEvent.md))- The type of the event.
- [getSource()](../android/view/accessibility/AccessibilityRecord.md))- The source info (for registered clients).
- [getClassName()](../android/view/accessibility/AccessibilityRecord.md))- The class name of the source.
- [getPackageName()](../android/view/accessibility/AccessibilityEvent.md))- The package name of the source.
- [getEventTime()](../android/view/accessibility/AccessibilityEvent.md))- The event time.

<br />

**View selected** - represents the event of selecting an item usually in the context of an [android.widget.AdapterView](../android/widget/AdapterView.md). 
*Type:* [TYPE_VIEW_SELECTED](../android/view/accessibility/AccessibilityEvent.md) 
*Properties:* 

- [getEventType()](../android/view/accessibility/AccessibilityEvent.md))- The type of the event.
- [getSource()](../android/view/accessibility/AccessibilityRecord.md))- The source info (for registered clients).
- [getClassName()](../android/view/accessibility/AccessibilityRecord.md))- The class name of the source.
- [getPackageName()](../android/view/accessibility/AccessibilityEvent.md))- The package name of the source.
- [getEventTime()](../android/view/accessibility/AccessibilityEvent.md))- The event time.

<br />

**View focused** - represents the event of focusing a [android.view.View](../android/view/View.md). 
*Type:* [TYPE_VIEW_FOCUSED](../android/view/accessibility/AccessibilityEvent.md) 
*Properties:* 

- [getEventType()](../android/view/accessibility/AccessibilityEvent.md))- The type of the event.
- [getSource()](../android/view/accessibility/AccessibilityRecord.md))- The source info (for registered clients).
- [getClassName()](../android/view/accessibility/AccessibilityRecord.md))- The class name of the source.
- [getPackageName()](../android/view/accessibility/AccessibilityEvent.md))- The package name of the source.
- [getEventTime()](../android/view/accessibility/AccessibilityEvent.md))- The event time.

<br />

**View text changed** - represents the event of changing the text of an [android.widget.EditText](../android/widget/EditText.md). 
*Type:* [TYPE_VIEW_TEXT_CHANGED](../android/view/accessibility/AccessibilityEvent.md) 
*Properties:* 

- [getEventType()](../android/view/accessibility/AccessibilityEvent.md))- The type of the event.
- [getSource()](../android/view/accessibility/AccessibilityRecord.md))- The source info (for registered clients).
- [getClassName()](../android/view/accessibility/AccessibilityRecord.md))- The class name of the source.
- [getPackageName()](../android/view/accessibility/AccessibilityEvent.md))- The package name of the source.
- [getEventTime()](../android/view/accessibility/AccessibilityEvent.md))- The event time.
- [getText()](../android/view/accessibility/AccessibilityRecord.md))- The new text of the source.
- [getBeforeText()](../android/view/accessibility/AccessibilityRecord.md))- The text of the source before the change.
- [getFromIndex()](../android/view/accessibility/AccessibilityRecord.md))- The text change start index.
- [getAddedCount()](../android/view/accessibility/AccessibilityRecord.md))- The number of added characters.
- [getRemovedCount()](../android/view/accessibility/AccessibilityRecord.md))- The number of removed characters.

<br />

**View text selection changed** - represents the event of changing the text selection of an [android.widget.EditText](../android/widget/EditText.md). 
*Type:* [TYPE_VIEW_TEXT_SELECTION_CHANGED](../android/view/accessibility/AccessibilityEvent.md) 
*Properties:* 

- [getEventType()](../android/view/accessibility/AccessibilityEvent.md))- The type of the event.
- [getSource()](../android/view/accessibility/AccessibilityRecord.md))- The source info (for registered clients).
- [getClassName()](../android/view/accessibility/AccessibilityRecord.md))- The class name of the source.
- [getPackageName()](../android/view/accessibility/AccessibilityEvent.md))- The package name of the source.
- [getEventTime()](../android/view/accessibility/AccessibilityEvent.md))- The event time.

<br />

**View text traversed at movement granularity** - represents the event of traversing the text of a view at a given granularity. For example, moving to the next word. 
*Type:* [TYPE_VIEW_TEXT_TRAVERSED_AT_MOVEMENT_GRANULARITY](../android/view/accessibility/AccessibilityEvent.md) 
*Properties:* 

- [getEventType()](../android/view/accessibility/AccessibilityEvent.md))- The type of the event.
- [getSource()](../android/view/accessibility/AccessibilityRecord.md))- The source info (for registered clients).
- [getClassName()](../android/view/accessibility/AccessibilityRecord.md))- The class name of the source.
- [getPackageName()](../android/view/accessibility/AccessibilityEvent.md))- The package name of the source.
- [getEventTime()](../android/view/accessibility/AccessibilityEvent.md))- The event time.
- [getMovementGranularity()](../android/view/accessibility/AccessibilityEvent.md))- Sets the granularity at which a view's text was traversed.
- [getText()](../android/view/accessibility/AccessibilityRecord.md))- The text of the source's sub-tree.
- [getFromIndex()](../android/view/accessibility/AccessibilityRecord.md))- The start the text that was skipped over in this movement. This is the starting point when moving forward through the text, but not when moving back.
- [getToIndex()](../android/view/accessibility/AccessibilityRecord.md))- The end of the text that was skipped over in this movement. This is the ending point when moving forward through the text, but not when moving back.
- [getAction()](../android/view/accessibility/AccessibilityEvent.md))- Gets traversal action which specifies the direction.

<br />

**View scrolled** - represents the event of scrolling a view. 
*Type:* [TYPE_VIEW_SCROLLED](../android/view/accessibility/AccessibilityEvent.md) 
*Properties:* 

- [getEventType()](../android/view/accessibility/AccessibilityEvent.md))- The type of the event.
- [getSource()](../android/view/accessibility/AccessibilityRecord.md))- The source info (for registered clients).
- [getClassName()](../android/view/accessibility/AccessibilityRecord.md))- The class name of the source.
- [getPackageName()](../android/view/accessibility/AccessibilityEvent.md))- The package name of the source.
- [getEventTime()](../android/view/accessibility/AccessibilityEvent.md))- The event time.
- [getScrollDeltaX()](../android/view/accessibility/AccessibilityRecord.md))- The difference in the horizontal position.
- [getScrollDeltaY()](../android/view/accessibility/AccessibilityRecord.md))- The difference in the vertical position.
- [getMaxScrollX()](../android/view/accessibility/AccessibilityRecord.md))()} - The max scroll offset of the source left edge
- [getMaxScrollY()](../android/view/accessibility/AccessibilityRecord.md))()} - The max scroll offset of the source top edge.

<br />

**TRANSITION TYPES** 

**Window state changed** - represents the event of a change to a section of the user interface that is visually distinct. Should be sent from either the root view of a window or from a view that is marked as a pane [android.view.View#setAccessibilityPaneTitle(CharSequence)](../android/view/View.md)). Note that changes to true windows are represented by [TYPE_WINDOWS_CHANGED](../android/view/accessibility/AccessibilityEvent.md). 
*Type:* [TYPE_WINDOW_STATE_CHANGED](../android/view/accessibility/AccessibilityEvent.md) 
*Properties:* 

- [getEventType()](../android/view/accessibility/AccessibilityEvent.md))- The type of the event.
- [getContentChangeTypes()](../android/view/accessibility/AccessibilityEvent.md))- The type of state changes.
- [getSource()](../android/view/accessibility/AccessibilityRecord.md))- The source info (for registered clients).
- [getClassName()](../android/view/accessibility/AccessibilityRecord.md))- The class name of the source.
- [getPackageName()](../android/view/accessibility/AccessibilityEvent.md))- The package name of the source.
- [getEventTime()](../android/view/accessibility/AccessibilityEvent.md))- The event time.
- [getText()](../android/view/accessibility/AccessibilityRecord.md))- The text of the source's sub-tree, including the pane titles.

<br />

**Window content changed** - represents the event of change in the content of a window. This change can be adding/removing view, changing a view size, etc. 

*Type:* [TYPE_WINDOW_CONTENT_CHANGED](../android/view/accessibility/AccessibilityEvent.md) 
*Properties:* 

- [getEventType()](../android/view/accessibility/AccessibilityEvent.md))- The type of the event.
- [getContentChangeTypes()](../android/view/accessibility/AccessibilityEvent.md))- The type of content changes.
- [getSource()](../android/view/accessibility/AccessibilityRecord.md))- The source info (for registered clients).
- [getClassName()](../android/view/accessibility/AccessibilityRecord.md))- The class name of the source.
- [getPackageName()](../android/view/accessibility/AccessibilityEvent.md))- The package name of the source.
- [getEventTime()](../android/view/accessibility/AccessibilityEvent.md))- The event time.

<br />

**Windows changed** - represents a change in the windows shown on the screen such as a window appeared, a window disappeared, a window size changed, a window layer changed, etc. These events should only come from the system, which is responsible for managing windows. The list of windows is available from [android.accessibilityservice.AccessibilityService#getWindows()](../android/accessibilityservice/AccessibilityService.md)). For regions of the user interface that are presented as windows but are controlled by an app's process, use [TYPE_WINDOW_STATE_CHANGED](../android/view/accessibility/AccessibilityEvent.md). 
*Type:* [TYPE_WINDOWS_CHANGED](../android/view/accessibility/AccessibilityEvent.md) 
*Properties:* 

- [getEventType()](../android/view/accessibility/AccessibilityEvent.md))- The type of the event.
- [getEventTime()](../android/view/accessibility/AccessibilityEvent.md))- The event time.
- [getWindowChanges()](../android/view/accessibility/AccessibilityEvent.md))
- The specific change to the source window

*Note:* You can retrieve the [AccessibilityWindowInfo](../android/view/accessibility/AccessibilityWindowInfo.md) for the window source of the event by looking through the list returned by [android.accessibilityservice.AccessibilityService#getWindows()](../android/accessibilityservice/AccessibilityService.md))for the window whose ID matches [getWindowId()](../android/view/accessibility/AccessibilityRecord.md)).

<br />

**NOTIFICATION TYPES** 

**Notification state changed** - represents the event showing a transient piece of information to the user. This information may be a [android.app.Notification](../android/app/Notification.md) or [android.widget.Toast](../android/widget/Toast.md). 
*Type:* [TYPE_NOTIFICATION_STATE_CHANGED](../android/view/accessibility/AccessibilityEvent.md) 
*Properties:* 

- [getEventType()](../android/view/accessibility/AccessibilityEvent.md))- The type of the event.
- [getClassName()](../android/view/accessibility/AccessibilityRecord.md))- The class name of the source.
- [getPackageName()](../android/view/accessibility/AccessibilityEvent.md))- The package name of the source.
- [getEventTime()](../android/view/accessibility/AccessibilityEvent.md))- The event time.
- [getParcelableData()](../android/view/accessibility/AccessibilityRecord.md))- The posted [android.app.Notification](../android/app/Notification.md), if applicable.
- [getText()](../android/view/accessibility/AccessibilityRecord.md))- Displayed text of the [android.widget.Toast](../android/widget/Toast.md), if applicable, or may contain text from the [android.app.Notification](../android/app/Notification.md), although [getParcelableData()](../android/view/accessibility/AccessibilityRecord.md))is a richer set of data for [android.app.Notification](../android/app/Notification.md).

<br />

**EXPLORATION TYPES** 

**View hover enter** - represents the event of beginning to hover over a [android.view.View](../android/view/View.md). The hover may be generated via exploring the screen by touch or via a pointing device. 
*Type:* [TYPE_VIEW_HOVER_ENTER](../android/view/accessibility/AccessibilityEvent.md) 
*Properties:* 

- [getEventType()](../android/view/accessibility/AccessibilityEvent.md))- The type of the event.
- [getSource()](../android/view/accessibility/AccessibilityRecord.md))- The source info (for registered clients).
- [getClassName()](../android/view/accessibility/AccessibilityRecord.md))- The class name of the source.
- [getPackageName()](../android/view/accessibility/AccessibilityEvent.md))- The package name of the source.
- [getEventTime()](../android/view/accessibility/AccessibilityEvent.md))- The event time.

<br />

**View hover exit** - represents the event of stopping to hover over a [android.view.View](../android/view/View.md). The hover may be generated via exploring the screen by touch or via a pointing device. 
*Type:* [TYPE_VIEW_HOVER_EXIT](../android/view/accessibility/AccessibilityEvent.md) 
*Properties:* 

- [getEventType()](../android/view/accessibility/AccessibilityEvent.md))- The type of the event.
- [getSource()](../android/view/accessibility/AccessibilityRecord.md))- The source info (for registered clients).
- [getClassName()](../android/view/accessibility/AccessibilityRecord.md))- The class name of the source.
- [getPackageName()](../android/view/accessibility/AccessibilityEvent.md))- The package name of the source.
- [getEventTime()](../android/view/accessibility/AccessibilityEvent.md))- The event time.

<br />

**View scrolled to** - represents the event of a target node brought on screen by ACTION_SCROLL_IN_DIRECTION.*Type:* [TYPE_VIEW_TARGETED_BY_SCROLL](../android/view/accessibility/AccessibilityEvent.md) 
*Properties:* 

- [getEventType()](../android/view/accessibility/AccessibilityEvent.md))- The type of the event.
- [getSource()](../android/view/accessibility/AccessibilityRecord.md))- The source info (for registered clients). This represents the node that is brought on screen as a result of the scroll.
- [getClassName()](../android/view/accessibility/AccessibilityRecord.md))- The class name of the source.
- [getPackageName()](../android/view/accessibility/AccessibilityEvent.md))- The package name of the source.
- [getEventTime()](../android/view/accessibility/AccessibilityEvent.md))- The event time.

<br />

**Touch interaction start** - represents the event of starting a touch interaction, which is the user starts touching the screen. 
*Type:* [TYPE_TOUCH_INTERACTION_START](../android/view/accessibility/AccessibilityEvent.md) 
*Properties:* 

- [getEventType()](../android/view/accessibility/AccessibilityEvent.md))- The type of the event.

*Note:* This event is fired only by the system and is not passed to the view tree to be populated. 

<br />

**Touch interaction end** - represents the event of ending a touch interaction, which is the user stops touching the screen. 
*Type:* [TYPE_TOUCH_INTERACTION_END](../android/view/accessibility/AccessibilityEvent.md) 
*Properties:* 

- [getEventType()](../android/view/accessibility/AccessibilityEvent.md))- The type of the event.

*Note:* This event is fired only by the system and is not passed to the view tree to be populated. 

<br />

**Touch exploration gesture start** - represents the event of starting a touch exploring gesture. 
*Type:* [TYPE_TOUCH_EXPLORATION_GESTURE_START](../android/view/accessibility/AccessibilityEvent.md) 
*Properties:* 

- [getEventType()](../android/view/accessibility/AccessibilityEvent.md))- The type of the event.

*Note:* This event is fired only by the system and is not passed to the view tree to be populated. 

<br />

**Touch exploration gesture end** - represents the event of ending a touch exploring gesture. 
*Type:* [TYPE_TOUCH_EXPLORATION_GESTURE_END](../android/view/accessibility/AccessibilityEvent.md) 
*Properties:* 

- [getEventType()](../android/view/accessibility/AccessibilityEvent.md))- The type of the event.

*Note:* This event is fired only by the system and is not passed to the view tree to be populated. 

<br />

**Touch gesture detection start** - represents the event of starting a user gesture detection. 
*Type:* [TYPE_GESTURE_DETECTION_START](../android/view/accessibility/AccessibilityEvent.md) 
*Properties:* 

- [getEventType()](../android/view/accessibility/AccessibilityEvent.md))- The type of the event.

*Note:* This event is fired only by the system and is not passed to the view tree to be populated. 

<br />

**Touch gesture detection end** - represents the event of ending a user gesture detection. 
*Type:* [TYPE_GESTURE_DETECTION_END](../android/view/accessibility/AccessibilityEvent.md) 
*Properties:* 

- [getEventType()](../android/view/accessibility/AccessibilityEvent.md))- The type of the event.

*Note:* This event is fired only by the system and is not passed to the view tree to be populated. 

<br />

**MISCELLANEOUS TYPES** 

**Announcement** - represents the event of an application requesting a screen reader to make an announcement. Because the event carries no semantic meaning, this event is appropriate only in exceptional situations where additional screen reader output is needed but other types of accessibility services do not need to be aware of the change. 
*Type:* [TYPE_ANNOUNCEMENT](../android/view/accessibility/AccessibilityEvent.md) 
*Properties:* 

- [getEventType()](../android/view/accessibility/AccessibilityEvent.md))- The type of the event.
- [getSource()](../android/view/accessibility/AccessibilityRecord.md))- The source info (for registered clients).
- [getClassName()](../android/view/accessibility/AccessibilityRecord.md))- The class name of the source.
- [getPackageName()](../android/view/accessibility/AccessibilityEvent.md))- The package name of the source.
- [getEventTime()](../android/view/accessibility/AccessibilityEvent.md))- The event time.
- [getText()](../android/view/accessibility/AccessibilityRecord.md))- The text of the announcement.

<br />

**speechStateChanged** *Type:* [TYPE_SPEECH_STATE_CHANGE](../android/view/accessibility/AccessibilityEvent.md) 
Represents a change in the speech state defined by the bit mask of the speech state change types. A change in the speech state occurs when an application wants to signal that it is either speaking or listening for human speech. This event helps avoid conflicts where two applications want to speak or one listens when another speaks. When sending this event, the sender should ensure that the accompanying state change types make sense. For example, the sender should not send [SPEECH_STATE_SPEAKING_START](../android/view/accessibility/AccessibilityEvent.md) and [SPEECH_STATE_SPEAKING_END](../android/view/accessibility/AccessibilityEvent.md) together.*Properties:* 

- [getSpeechStateChangeTypes()](../android/view/accessibility/AccessibilityEvent.md))- The type of state changes
- [getPackageName()](../android/view/accessibility/AccessibilityEvent.md))- The package name of the source.
- [getEventTime()](../android/view/accessibility/AccessibilityEvent.md))- The event time.

<br />

## Summary

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_CHANGE_TYPE_CHECKED](../android/view/accessibility/AccessibilityEvent.md) Change type for [TYPE_WINDOW_CONTENT_CHANGED](../android/view/accessibility/AccessibilityEvent.md) event: The source node changed its checked state, which is returned by [AccessibilityNodeInfo.getChecked()](../android/view/accessibility/AccessibilityNodeInfo.md)). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_CHANGE_TYPE_CONTENT_DESCRIPTION](../android/view/accessibility/AccessibilityEvent.md) Change type for [TYPE_WINDOW_CONTENT_CHANGED](../android/view/accessibility/AccessibilityEvent.md) event: The node's content description changed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_CHANGE_TYPE_CONTENT_INVALID](../android/view/accessibility/AccessibilityEvent.md) Change type for [TYPE_WINDOW_CONTENT_CHANGED](../android/view/accessibility/AccessibilityEvent.md) event: The source node changed its content validity returned by [AccessibilityNodeInfo.isContentInvalid](../android/view/accessibility/AccessibilityNodeInfo.md)). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_CHANGE_TYPE_DRAG_CANCELLED](../android/view/accessibility/AccessibilityEvent.md) Change type for [TYPE_WINDOW_CONTENT_CHANGED](../android/view/accessibility/AccessibilityEvent.md) event: A drag in with accessibility enabled has ended. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_CHANGE_TYPE_DRAG_DROPPED](../android/view/accessibility/AccessibilityEvent.md) Change type for [TYPE_WINDOW_CONTENT_CHANGED](../android/view/accessibility/AccessibilityEvent.md) event: A drag in with accessibility enabled has ended. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_CHANGE_TYPE_DRAG_STARTED](../android/view/accessibility/AccessibilityEvent.md) Change type for [TYPE_WINDOW_CONTENT_CHANGED](../android/view/accessibility/AccessibilityEvent.md) event: A drag has started while accessibility is enabled. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_CHANGE_TYPE_ENABLED](../android/view/accessibility/AccessibilityEvent.md) Change type for [TYPE_WINDOW_CONTENT_CHANGED](../android/view/accessibility/AccessibilityEvent.md) event: The source node changed its ability to interact returned by [AccessibilityNodeInfo.isEnabled](../android/view/accessibility/AccessibilityNodeInfo.md)). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_CHANGE_TYPE_ERROR](../android/view/accessibility/AccessibilityEvent.md) Change type for [TYPE_WINDOW_CONTENT_CHANGED](../android/view/accessibility/AccessibilityEvent.md) event: The source node changed its erroneous content's error message returned by [AccessibilityNodeInfo.getError](../android/view/accessibility/AccessibilityNodeInfo.md)). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_CHANGE_TYPE_EXPANDED](../android/view/accessibility/AccessibilityEvent.md) Change type for [TYPE_WINDOW_CONTENT_CHANGED](../android/view/accessibility/AccessibilityEvent.md) event: The source node changed its expanded state which is returned by [AccessibilityNodeInfo.getExpandedState()](../android/view/accessibility/AccessibilityNodeInfo.md)). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_CHANGE_TYPE_PANE_APPEARED](../android/view/accessibility/AccessibilityEvent.md) Change type for [TYPE_WINDOW_STATE_CHANGED](../android/view/accessibility/AccessibilityEvent.md) event: The node has a pane title, and either just appeared or just was assigned a title when it had none before. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_CHANGE_TYPE_PANE_DISAPPEARED](../android/view/accessibility/AccessibilityEvent.md) Change type for [TYPE_WINDOW_STATE_CHANGED](../android/view/accessibility/AccessibilityEvent.md) event: Can mean one of two slightly different things. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_CHANGE_TYPE_PANE_TITLE](../android/view/accessibility/AccessibilityEvent.md) Change type for [TYPE_WINDOW_STATE_CHANGED](../android/view/accessibility/AccessibilityEvent.md) event: The node's pane title changed. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_CHANGE_TYPE_SORT_DIRECTION](../android/view/accessibility/AccessibilityEvent.md) Change type for [TYPE_WINDOW_CONTENT_CHANGED](../android/view/accessibility/AccessibilityEvent.md) event: The source node's collection item info changed its sort direction state for the data corresponding to this collection item, which is returned by [AccessibilityNodeInfo.CollectionItemInfo.getSortDirection()](../android/view/accessibility/AccessibilityNodeInfo.CollectionItemInfo.md)). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_CHANGE_TYPE_STATE_DESCRIPTION](../android/view/accessibility/AccessibilityEvent.md) Change type for [TYPE_WINDOW_CONTENT_CHANGED](../android/view/accessibility/AccessibilityEvent.md) event: state description of the node as returned by [AccessibilityNodeInfo.getStateDescription](../android/view/accessibility/AccessibilityNodeInfo.md))changed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_CHANGE_TYPE_SUBTREE](../android/view/accessibility/AccessibilityEvent.md) Change type for [TYPE_WINDOW_CONTENT_CHANGED](../android/view/accessibility/AccessibilityEvent.md) event: One or more content changes occurred in the the subtree rooted at the source node, or the subtree's structure changed when a node was added or removed. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_CHANGE_TYPE_SUPPLEMENTAL_DESCRIPTION](../android/view/accessibility/AccessibilityEvent.md) Change type for [TYPE_WINDOW_CONTENT_CHANGED](../android/view/accessibility/AccessibilityEvent.md) event: The source node changed its supplemental description, which is returned by [AccessibilityNodeInfo.getSupplementalDescription()](../android/view/accessibility/AccessibilityNodeInfo.md)). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_CHANGE_TYPE_TEXT](../android/view/accessibility/AccessibilityEvent.md) Change type for [TYPE_WINDOW_CONTENT_CHANGED](../android/view/accessibility/AccessibilityEvent.md) event: The node's text changed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_CHANGE_TYPE_UNDEFINED](../android/view/accessibility/AccessibilityEvent.md) Change type for [TYPE_WINDOW_CONTENT_CHANGED](../android/view/accessibility/AccessibilityEvent.md) event: The type of change is not defined. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INVALID_POSITION](../android/view/accessibility/AccessibilityEvent.md) Invalid selection/focus position. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MAX_TEXT_LENGTH](../android/view/accessibility/AccessibilityEvent.md) Maximum length of the text fields. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SPEECH_STATE_LISTENING_END](../android/view/accessibility/AccessibilityEvent.md) Change type for [TYPE_SPEECH_STATE_CHANGE](../android/view/accessibility/AccessibilityEvent.md) event: another service is no longer listening to the microphone. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SPEECH_STATE_LISTENING_START](../android/view/accessibility/AccessibilityEvent.md) Change type for [TYPE_SPEECH_STATE_CHANGE](../android/view/accessibility/AccessibilityEvent.md) event: another service is listening to the microphone. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SPEECH_STATE_SPEAKING_END](../android/view/accessibility/AccessibilityEvent.md) Change type for [TYPE_SPEECH_STATE_CHANGE](../android/view/accessibility/AccessibilityEvent.md) event: another service is no longer speaking. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SPEECH_STATE_SPEAKING_START](../android/view/accessibility/AccessibilityEvent.md) Change type for [TYPE_SPEECH_STATE_CHANGE](../android/view/accessibility/AccessibilityEvent.md) event: another service is speaking. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPES_ALL_MASK](../android/view/accessibility/AccessibilityEvent.md) Mask for [AccessibilityEvent](../android/view/accessibility/AccessibilityEvent.md) all types. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_ANNOUNCEMENT](../android/view/accessibility/AccessibilityEvent.md) Represents the event of an application making an announcement. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_ASSIST_READING_CONTEXT](../android/view/accessibility/AccessibilityEvent.md) Represents the event of the assistant currently reading the users screen context. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_GESTURE_DETECTION_END](../android/view/accessibility/AccessibilityEvent.md) Represents the event of ending gesture detection. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_GESTURE_DETECTION_START](../android/view/accessibility/AccessibilityEvent.md) Represents the event of beginning gesture detection. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_NOTIFICATION_STATE_CHANGED](../android/view/accessibility/AccessibilityEvent.md) Represents the event showing a [android.app.Notification](../android/app/Notification.md). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_SPEECH_STATE_CHANGE](../android/view/accessibility/AccessibilityEvent.md) Represents a change in the speech state defined by the speech state change types. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TOUCH_EXPLORATION_GESTURE_END](../android/view/accessibility/AccessibilityEvent.md) Represents the event of ending a touch exploration gesture. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TOUCH_EXPLORATION_GESTURE_START](../android/view/accessibility/AccessibilityEvent.md) Represents the event of starting a touch exploration gesture. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TOUCH_INTERACTION_END](../android/view/accessibility/AccessibilityEvent.md) Represents the event of the user ending to touch the screen. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TOUCH_INTERACTION_START](../android/view/accessibility/AccessibilityEvent.md) Represents the event of the user starting to touch the screen. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_VIEW_ACCESSIBILITY_FOCUSED](../android/view/accessibility/AccessibilityEvent.md) Represents the event of gaining accessibility focus. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_VIEW_ACCESSIBILITY_FOCUS_CLEARED](../android/view/accessibility/AccessibilityEvent.md) Represents the event of clearing accessibility focus. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_VIEW_CLICKED](../android/view/accessibility/AccessibilityEvent.md) Represents the event of clicking on a [android.view.View](../android/view/View.md) like [android.widget.Button](../android/widget/Button.md), [android.widget.CompoundButton](../android/widget/CompoundButton.md), etc. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_VIEW_CONTEXT_CLICKED](../android/view/accessibility/AccessibilityEvent.md) Represents the event of a context click on a [android.view.View](../android/view/View.md). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_VIEW_FOCUSED](../android/view/accessibility/AccessibilityEvent.md) Represents the event of setting input focus of a [android.view.View](../android/view/View.md). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_VIEW_HOVER_ENTER](../android/view/accessibility/AccessibilityEvent.md) Represents the event of a hover enter over a [android.view.View](../android/view/View.md). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_VIEW_HOVER_EXIT](../android/view/accessibility/AccessibilityEvent.md) Represents the event of a hover exit over a [android.view.View](../android/view/View.md). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_VIEW_LONG_CLICKED](../android/view/accessibility/AccessibilityEvent.md) Represents the event of long clicking on a [android.view.View](../android/view/View.md) like [android.widget.Button](../android/widget/Button.md), [android.widget.CompoundButton](../android/widget/CompoundButton.md), etc. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_VIEW_SCROLLED](../android/view/accessibility/AccessibilityEvent.md) Represents the event of scrolling a view. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_VIEW_SELECTED](../android/view/accessibility/AccessibilityEvent.md) Represents the event of selecting an item usually in the context of an [android.widget.AdapterView](../android/widget/AdapterView.md). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_VIEW_TARGETED_BY_SCROLL](../android/view/accessibility/AccessibilityEvent.md) Represents the event of a scroll having completed and brought the target node on screen. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_VIEW_TEXT_CHANGED](../android/view/accessibility/AccessibilityEvent.md) Represents the event of changing the text of an [android.widget.EditText](../android/widget/EditText.md). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_VIEW_TEXT_SELECTION_CHANGED](../android/view/accessibility/AccessibilityEvent.md) Represents the event of changing the selection in an [android.widget.EditText](../android/widget/EditText.md). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_VIEW_TEXT_TRAVERSED_AT_MOVEMENT_GRANULARITY](../android/view/accessibility/AccessibilityEvent.md) Represents the event of traversing the text of a view at a given movement granularity. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_WINDOWS_CHANGED](../android/view/accessibility/AccessibilityEvent.md) Represents the event change in the system windows shown on the screen. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_WINDOW_CONTENT_CHANGED](../android/view/accessibility/AccessibilityEvent.md) Represents the event of changing the content of a window and more specifically the sub-tree rooted at the event's source. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_WINDOW_STATE_CHANGED](../android/view/accessibility/AccessibilityEvent.md) Represents the event of a change to a visually distinct section of the user interface. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WINDOWS_CHANGE_ACCESSIBILITY_FOCUSED](../android/view/accessibility/AccessibilityEvent.md) Change type for [TYPE_WINDOWS_CHANGED](../android/view/accessibility/AccessibilityEvent.md) event: The window's [AccessibilityWindowInfo.isAccessibilityFocused()](../android/view/accessibility/AccessibilityWindowInfo.md))changed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WINDOWS_CHANGE_ACTIVE](../android/view/accessibility/AccessibilityEvent.md) Change type for [TYPE_WINDOWS_CHANGED](../android/view/accessibility/AccessibilityEvent.md) event: The window's [AccessibilityWindowInfo.isActive()](../android/view/accessibility/AccessibilityWindowInfo.md))changed. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WINDOWS_CHANGE_ADDED](../android/view/accessibility/AccessibilityEvent.md) Change type for [TYPE_WINDOWS_CHANGED](../android/view/accessibility/AccessibilityEvent.md) event: The window was added. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WINDOWS_CHANGE_BOUNDS](../android/view/accessibility/AccessibilityEvent.md) Change type for [TYPE_WINDOWS_CHANGED](../android/view/accessibility/AccessibilityEvent.md) event: The window's bounds changed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WINDOWS_CHANGE_CHILDREN](../android/view/accessibility/AccessibilityEvent.md) Change type for [TYPE_WINDOWS_CHANGED](../android/view/accessibility/AccessibilityEvent.md) event: The window's children changed. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WINDOWS_CHANGE_FOCUSED](../android/view/accessibility/AccessibilityEvent.md) Change type for [TYPE_WINDOWS_CHANGED](../android/view/accessibility/AccessibilityEvent.md) event: The window's [AccessibilityWindowInfo.isFocused()](../android/view/accessibility/AccessibilityWindowInfo.md))changed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WINDOWS_CHANGE_LAYER](../android/view/accessibility/AccessibilityEvent.md) Change type for [TYPE_WINDOWS_CHANGED](../android/view/accessibility/AccessibilityEvent.md) event: The window's layer changed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WINDOWS_CHANGE_PARENT](../android/view/accessibility/AccessibilityEvent.md) Change type for [TYPE_WINDOWS_CHANGED](../android/view/accessibility/AccessibilityEvent.md) event: The window's parent changed. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WINDOWS_CHANGE_PIP](../android/view/accessibility/AccessibilityEvent.md) Change type for [TYPE_WINDOWS_CHANGED](../android/view/accessibility/AccessibilityEvent.md) event: The window either entered or exited picture-in-picture mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WINDOWS_CHANGE_REMOVED](../android/view/accessibility/AccessibilityEvent.md) Change type for [TYPE_WINDOWS_CHANGED](../android/view/accessibility/AccessibilityEvent.md) event: A window was removed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WINDOWS_CHANGE_TITLE](../android/view/accessibility/AccessibilityEvent.md) Change type for [TYPE_WINDOWS_CHANGED](../android/view/accessibility/AccessibilityEvent.md) event: The window's title changed. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AccessibilityEvent](../android/view/accessibility/AccessibilityEvent.md))`()` Creates a new [AccessibilityEvent](../android/view/accessibility/AccessibilityEvent.md). |
| [AccessibilityEvent](../android/view/accessibility/AccessibilityEvent.md))`(`event:` ` [AccessibilityEvent](../android/view/accessibility/AccessibilityEvent.md)`)` Copy constructor. |
| [AccessibilityEvent](../android/view/accessibility/AccessibilityEvent.md))`(`eventType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a new [AccessibilityEvent](../android/view/accessibility/AccessibilityEvent.md) with the given`eventType`. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [appendRecord](../android/view/accessibility/AccessibilityEvent.md))`(`record:` ` [AccessibilityRecord](../android/view/accessibility/AccessibilityRecord.md)!`)` Appends an [AccessibilityRecord](../android/view/accessibility/AccessibilityRecord.md) to the end of event records. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/view/accessibility/AccessibilityEvent.md))`()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [eventTypeToString](../android/view/accessibility/AccessibilityEvent.md))`(`eventType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the string representation of an event type. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAction](../android/view/accessibility/AccessibilityEvent.md))`()` Gets the performed action that triggered this event. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getContentChangeTypes](../android/view/accessibility/AccessibilityEvent.md))`()` Gets the bit mask of change types signaled by a [TYPE_WINDOW_CONTENT_CHANGED](../android/view/accessibility/AccessibilityEvent.md) event or [TYPE_WINDOW_STATE_CHANGED](../android/view/accessibility/AccessibilityEvent.md). |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getEventTime](../android/view/accessibility/AccessibilityEvent.md))`()` Gets the time in which this event was sent. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getEventType](../android/view/accessibility/AccessibilityEvent.md))`()` Gets the event type. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMovementGranularity](../android/view/accessibility/AccessibilityEvent.md))`()` Gets the movement granularity that was traversed. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [getPackageName](../android/view/accessibility/AccessibilityEvent.md))`()` Gets the package name of the source. |
| --- | --- |
| [AccessibilityRecord](../android/view/accessibility/AccessibilityRecord.md)! | [getRecord](../android/view/accessibility/AccessibilityEvent.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Gets the record at a given index. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRecordCount](../android/view/accessibility/AccessibilityEvent.md))`()` Gets the number of records contained in the event. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSpeechStateChangeTypes](../android/view/accessibility/AccessibilityEvent.md))`()` Gets the bit mask of the speech state signaled by a [TYPE_SPEECH_STATE_CHANGE](../android/view/accessibility/AccessibilityEvent.md) event. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getWindowChanges](../android/view/accessibility/AccessibilityEvent.md))`()` Get the bit mask of change types signaled by a [TYPE_WINDOWS_CHANGED](../android/view/accessibility/AccessibilityEvent.md) event. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [initFromParcel](../android/view/accessibility/AccessibilityEvent.md))`(`parcel:` ` [Parcel](../android/os/Parcel.md)!`)` Creates a new instance from a [Parcel](../android/os/Parcel.md). |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAccessibilityDataSensitive](../android/view/accessibility/AccessibilityEvent.md))`()` Whether the event should only be delivered to an [android.accessibilityservice.AccessibilityService](../android/accessibilityservice/AccessibilityService.md) with the [android.accessibilityservice.AccessibilityServiceInfo#isAccessibilityTool](../android/accessibilityservice/AccessibilityServiceInfo.md))property set to true. |
| --- | --- |
| static [AccessibilityEvent](../android/view/accessibility/AccessibilityEvent.md)! | [obtain](../android/view/accessibility/AccessibilityEvent.md))`()` Instantiates a new AccessibilityEvent instance. |
| static [AccessibilityEvent](../android/view/accessibility/AccessibilityEvent.md)! | [obtain](../android/view/accessibility/AccessibilityEvent.md))`(`event:` ` [AccessibilityEvent](../android/view/accessibility/AccessibilityEvent.md)!`)` Instantiates a new AccessibilityEvent instance. |
| static [AccessibilityEvent](../android/view/accessibility/AccessibilityEvent.md)! | [obtain](../android/view/accessibility/AccessibilityEvent.md))`(`eventType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Instantiates a new AccessibilityEvent instance with its type property set. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [recycle](../android/view/accessibility/AccessibilityEvent.md))`()` Previously would recycle an instance back to be reused. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAccessibilityDataSensitive](../android/view/accessibility/AccessibilityEvent.md))`(`accessibilityDataSensitive:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether the event should only be delivered to an [android.accessibilityservice.AccessibilityService](../android/accessibilityservice/AccessibilityService.md) with the [android.accessibilityservice.AccessibilityServiceInfo#isAccessibilityTool](../android/accessibilityservice/AccessibilityServiceInfo.md))property set to true. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAction](../android/view/accessibility/AccessibilityEvent.md))`(`action:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the performed action that triggered this event. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setContentChangeTypes](../android/view/accessibility/AccessibilityEvent.md))`(`changeTypes:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the bit mask of node tree changes signaled by an [TYPE_WINDOW_CONTENT_CHANGED](../android/view/accessibility/AccessibilityEvent.md) event. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEventTime](../android/view/accessibility/AccessibilityEvent.md))`(`eventTime:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the time in which this event was sent. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEventType](../android/view/accessibility/AccessibilityEvent.md))`(`eventType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the event type. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMovementGranularity](../android/view/accessibility/AccessibilityEvent.md))`(`granularity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the movement granularity that was traversed. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPackageName](../android/view/accessibility/AccessibilityEvent.md))`(`packageName:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Sets the package name of the source. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSpeechStateChangeTypes](../android/view/accessibility/AccessibilityEvent.md))`(`state:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the bit mask of the speech state change types signaled by a [TYPE_SPEECH_STATE_CHANGE](../android/view/accessibility/AccessibilityEvent.md) event. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/view/accessibility/AccessibilityEvent.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/view/accessibility/AccessibilityEvent.md))`(`parcel:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Inherited functions ||
|---|---|
| From class [AccessibilityRecord](../android/view/accessibility/AccessibilityRecord.md) |---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAddedCount](../android/view/accessibility/AccessibilityRecord.md))`()` <br /> Gets the number of added characters. <br /> | | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getBeforeText](../android/view/accessibility/AccessibilityRecord.md))`()` <br /> Gets the text before a change. <br /> | | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getClassName](../android/view/accessibility/AccessibilityRecord.md))`()` <br /> Gets the class name of the source. <br /> | | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getContentDescription](../android/view/accessibility/AccessibilityRecord.md))`()` <br /> Gets the description of the source. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCurrentItemIndex](../android/view/accessibility/AccessibilityRecord.md))`()` <br /> Gets the index of the source in the list of items the can be visited. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDisplayId](../android/view/accessibility/AccessibilityRecord.md))`()` <br /> Gets the id of the display from which the event comes from. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getFromIndex](../android/view/accessibility/AccessibilityRecord.md))`()` <br /> Gets the index of the first character of the changed sequence, or the beginning of a text selection or the index of the first visible item when scrolling. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getItemCount](../android/view/accessibility/AccessibilityRecord.md))`()` <br /> Gets the number of items that can be visited. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxScrollX](../android/view/accessibility/AccessibilityRecord.md))`()` <br /> Gets the max scroll offset of the source left edge in pixels. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxScrollY](../android/view/accessibility/AccessibilityRecord.md))`()` <br /> Gets the max scroll offset of the source top edge in pixels. <br /> | | [Parcelable](../android/os/Parcelable.md)? | [getParcelableData](../android/view/accessibility/AccessibilityRecord.md))`()` <br /> Gets the [Parcelable](../android/os/Parcelable.md) data. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRemovedCount](../android/view/accessibility/AccessibilityRecord.md))`()` <br /> Gets the number of removed characters. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getScrollDeltaX](../android/view/accessibility/AccessibilityRecord.md))`()` <br /> Gets the difference in pixels between the horizontal position before the scroll and the current horizontal position <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getScrollDeltaY](../android/view/accessibility/AccessibilityRecord.md))`()` <br /> Gets the difference in pixels between the vertical position before the scroll and the current vertical position <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getScrollX](../android/view/accessibility/AccessibilityRecord.md))`()` <br /> Gets the scroll offset of the source left edge in pixels. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getScrollY](../android/view/accessibility/AccessibilityRecord.md))`()` <br /> Gets the scroll offset of the source top edge in pixels. <br /> | | [AccessibilityNodeInfo](../android/view/accessibility/AccessibilityNodeInfo.md)? | [getSource](../android/view/accessibility/AccessibilityRecord.md))`()` <br /> Gets the [AccessibilityNodeInfo](../android/view/accessibility/AccessibilityNodeInfo.md) of the event source. **Note:** It is a client responsibility to recycle the received info by calling [AccessibilityNodeInfo#recycle()](../android/view/accessibility/AccessibilityNodeInfo.md))to avoid creating of multiple instances. <br /> | | [AccessibilityNodeInfo](../android/view/accessibility/AccessibilityNodeInfo.md)? | [getSource](../android/view/accessibility/AccessibilityRecord.md))`(`prefetchingStrategy:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Gets the [AccessibilityNodeInfo](../android/view/accessibility/AccessibilityNodeInfo.md) of the event source. <br /> | | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!> | [getText](../android/view/accessibility/AccessibilityRecord.md))`()` <br /> Gets the text of the event. The index in the list represents the priority of the text. Specifically, the lower the index the higher the priority. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getToIndex](../android/view/accessibility/AccessibilityRecord.md))`()` <br /> Gets the index of text selection end or the index of the last visible item when scrolling. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getWindowId](../android/view/accessibility/AccessibilityRecord.md))`()` <br /> Gets the id of the window from which the event comes from. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isChecked](../android/view/accessibility/AccessibilityRecord.md))`()` <br /> Gets if the source is checked. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEnabled](../android/view/accessibility/AccessibilityRecord.md))`()` <br /> Gets if the source is enabled. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isFullScreen](../android/view/accessibility/AccessibilityRecord.md))`()` <br /> Gets if the source is taking the entire screen. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPassword](../android/view/accessibility/AccessibilityRecord.md))`()` <br /> Gets if the source is a password field. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isScrollable](../android/view/accessibility/AccessibilityRecord.md))`()` <br /> Gets if the source is scrollable. <br /> | | [AccessibilityRecord](../android/view/accessibility/AccessibilityRecord.md) | [obtain](../android/view/accessibility/AccessibilityRecord.md))`(`record:` ` [AccessibilityRecord](../android/view/accessibility/AccessibilityRecord.md)`)` <br /> Instantiates a new record initialized with data from the given record. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAddedCount](../android/view/accessibility/AccessibilityRecord.md))`(`addedCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the number of added characters. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBeforeText](../android/view/accessibility/AccessibilityRecord.md))`(`beforeText:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?`)` <br /> Sets the text before a change. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setChecked](../android/view/accessibility/AccessibilityRecord.md))`(`isChecked:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Sets if the source is checked. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setClassName](../android/view/accessibility/AccessibilityRecord.md))`(`className:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?`)` <br /> Sets the class name of the source. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setContentDescription](../android/view/accessibility/AccessibilityRecord.md))`(`contentDescription:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?`)` <br /> Sets the description of the source. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCurrentItemIndex](../android/view/accessibility/AccessibilityRecord.md))`(`currentItemIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the index of the source in the list of items that can be visited. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEnabled](../android/view/accessibility/AccessibilityRecord.md))`(`isEnabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Sets if the source is enabled. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFromIndex](../android/view/accessibility/AccessibilityRecord.md))`(`fromIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the index of the first character of the changed sequence or the beginning of a text selection or the index of the first visible item when scrolling. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFullScreen](../android/view/accessibility/AccessibilityRecord.md))`(`isFullScreen:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Sets if the source is taking the entire screen. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setItemCount](../android/view/accessibility/AccessibilityRecord.md))`(`itemCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the number of items that can be visited. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMaxScrollX](../android/view/accessibility/AccessibilityRecord.md))`(`maxScrollX:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the max scroll offset of the source left edge in pixels. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMaxScrollY](../android/view/accessibility/AccessibilityRecord.md))`(`maxScrollY:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the max scroll offset of the source top edge in pixels. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setParcelableData](../android/view/accessibility/AccessibilityRecord.md))`(`parcelableData:` ` [Parcelable](../android/os/Parcelable.md)?`)` <br /> Sets the [Parcelable](../android/os/Parcelable.md) data of the event. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPassword](../android/view/accessibility/AccessibilityRecord.md))`(`isPassword:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Sets if the source is a password field. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRemovedCount](../android/view/accessibility/AccessibilityRecord.md))`(`removedCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the number of removed characters. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setScrollDeltaX](../android/view/accessibility/AccessibilityRecord.md))`(`scrollDeltaX:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the difference in pixels between the horizontal position before the scroll and the current horizontal position <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setScrollDeltaY](../android/view/accessibility/AccessibilityRecord.md))`(`scrollDeltaY:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the difference in pixels between the vertical position before the scroll and the current vertical position <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setScrollX](../android/view/accessibility/AccessibilityRecord.md))`(`scrollX:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the scroll offset of the source left edge in pixels. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setScrollY](../android/view/accessibility/AccessibilityRecord.md))`(`scrollY:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the scroll offset of the source top edge in pixels. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setScrollable](../android/view/accessibility/AccessibilityRecord.md))`(`scrollable:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Sets if the source is scrollable. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSource](../android/view/accessibility/AccessibilityRecord.md))`(`source:` ` [View](../android/view/View.md)?`)` <br /> Sets the event source. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSource](../android/view/accessibility/AccessibilityRecord.md))`(`root:` ` [View](../android/view/View.md)?`, `virtualDescendantId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the source to be a virtual descendant of the given`root`. If`virtualDescendantId`equals to [View.NO_ID](../android/view/View.md) the root is set as the source. A virtual descendant is an imaginary View that is reported as a part of the view hierarchy for accessibility purposes. This enables custom views that draw complex content to report them selves as a tree of virtual views, thus conveying their logical structure. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setToIndex](../android/view/accessibility/AccessibilityRecord.md))`(`toIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the index of text selection end or the index of the last visible item when scrolling. <br /> | ||

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [AccessibilityEvent](../android/view/accessibility/AccessibilityEvent.md)!\> | [CREATOR](../android/view/accessibility/AccessibilityEvent.md) <br /> |

## Constants

### CONTENT_CHANGE_TYPE_CHECKED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTENT_CHANGE_TYPE_CHECKED: Int
```

Change type for [TYPE_WINDOW_CONTENT_CHANGED](../android/view/accessibility/AccessibilityEvent.md) event: The source node changed its checked state, which is returned by [AccessibilityNodeInfo.getChecked()](../android/view/accessibility/AccessibilityNodeInfo.md)). The view changing its checked state should call [AccessibilityNodeInfo.setChecked(int)](../android/view/accessibility/AccessibilityNodeInfo.md))and then send this event. 

 Value: 8192

**See Also**

- [android.view.accessibility.AccessibilityNodeInfo#getChecked()](../android/view/accessibility/AccessibilityNodeInfo.md))
- [android.view.accessibility.AccessibilityNodeInfo#setChecked(int)](../android/view/accessibility/AccessibilityNodeInfo.md)) 

### CONTENT_CHANGE_TYPE_CONTENT_DESCRIPTION

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTENT_CHANGE_TYPE_CONTENT_DESCRIPTION: Int
```

Change type for [TYPE_WINDOW_CONTENT_CHANGED](../android/view/accessibility/AccessibilityEvent.md) event: The node's content description changed. 

 Value: 4

### CONTENT_CHANGE_TYPE_CONTENT_INVALID

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTENT_CHANGE_TYPE_CONTENT_INVALID: Int
```

Change type for [TYPE_WINDOW_CONTENT_CHANGED](../android/view/accessibility/AccessibilityEvent.md) event: The source node changed its content validity returned by [AccessibilityNodeInfo.isContentInvalid](../android/view/accessibility/AccessibilityNodeInfo.md)). The view changing content validity should call [AccessibilityNodeInfo.setContentInvalid](../android/view/accessibility/AccessibilityNodeInfo.md))and then send this event. 

 Value: 1024

**See Also**

- [android.view.accessibility.AccessibilityNodeInfo#isContentInvalid](../android/view/accessibility/AccessibilityNodeInfo.md))
- [android.view.accessibility.AccessibilityNodeInfo#setContentInvalid](../android/view/accessibility/AccessibilityNodeInfo.md)) 

### CONTENT_CHANGE_TYPE_DRAG_CANCELLED

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTENT_CHANGE_TYPE_DRAG_CANCELLED: Int
```

Change type for [TYPE_WINDOW_CONTENT_CHANGED](../android/view/accessibility/AccessibilityEvent.md) event: A drag in with accessibility enabled has ended. This means the content has been unsuccessfully dropped, the user has canceled the action via an AccessibilityAction, or no drop has been detected within a timeout and the drag was automatically cancelled. This is sent from the source that initiated the drag. 

 Value: 512

**See Also**

- [android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction#ACTION_DRAG_CANCEL](../android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction.md) 

### CONTENT_CHANGE_TYPE_DRAG_DROPPED

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTENT_CHANGE_TYPE_DRAG_DROPPED: Int
```

Change type for [TYPE_WINDOW_CONTENT_CHANGED](../android/view/accessibility/AccessibilityEvent.md) event: A drag in with accessibility enabled has ended. This means the content has been successfully dropped. This is sent from the target that accepted the dragged content. 

 Value: 256

**See Also**

- [android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction#ACTION_DRAG_DROP](../android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction.md) 

### CONTENT_CHANGE_TYPE_DRAG_STARTED

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTENT_CHANGE_TYPE_DRAG_STARTED: Int
```

Change type for [TYPE_WINDOW_CONTENT_CHANGED](../android/view/accessibility/AccessibilityEvent.md) event: A drag has started while accessibility is enabled. This is either via an AccessibilityAction, or via touch events. This is sent from the source that initiated the drag. 

 Value: 128

**See Also**

- [android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction#ACTION_DRAG_START](../android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction.md) 

### CONTENT_CHANGE_TYPE_ENABLED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTENT_CHANGE_TYPE_ENABLED: Int
```

Change type for [TYPE_WINDOW_CONTENT_CHANGED](../android/view/accessibility/AccessibilityEvent.md) event: The source node changed its ability to interact returned by [AccessibilityNodeInfo.isEnabled](../android/view/accessibility/AccessibilityNodeInfo.md)). The view changing content's ability to interact should call [AccessibilityNodeInfo.setEnabled](../android/view/accessibility/AccessibilityNodeInfo.md))and then send this event. 

 Value: 4096

**See Also**

- [android.view.accessibility.AccessibilityNodeInfo#isEnabled](../android/view/accessibility/AccessibilityNodeInfo.md))
- [android.view.accessibility.AccessibilityNodeInfo#setEnabled](../android/view/accessibility/AccessibilityNodeInfo.md)) 

### CONTENT_CHANGE_TYPE_ERROR

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTENT_CHANGE_TYPE_ERROR: Int
```

Change type for [TYPE_WINDOW_CONTENT_CHANGED](../android/view/accessibility/AccessibilityEvent.md) event: The source node changed its erroneous content's error message returned by [AccessibilityNodeInfo.getError](../android/view/accessibility/AccessibilityNodeInfo.md)). The view changing erroneous content's error message should call [AccessibilityNodeInfo.setError](../android/view/accessibility/AccessibilityNodeInfo.md))and then send this event. 

 Value: 2048

**See Also**

- [android.view.accessibility.AccessibilityNodeInfo#getError](../android/view/accessibility/AccessibilityNodeInfo.md))
- [android.view.accessibility.AccessibilityNodeInfo#setError](../android/view/accessibility/AccessibilityNodeInfo.md)) 

### CONTENT_CHANGE_TYPE_EXPANDED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTENT_CHANGE_TYPE_EXPANDED: Int
```

Change type for [TYPE_WINDOW_CONTENT_CHANGED](../android/view/accessibility/AccessibilityEvent.md) event: The source node changed its expanded state which is returned by [AccessibilityNodeInfo.getExpandedState()](../android/view/accessibility/AccessibilityNodeInfo.md)). The view changing the node's expanded state should call [android.view.accessibility.AccessibilityNodeInfo#setExpandedState(int)](../android/view/accessibility/AccessibilityNodeInfo.md))and then send this event. 

 Value: 16384

**See Also**

- [android.view.accessibility.AccessibilityNodeInfo#getExpandedState()](../android/view/accessibility/AccessibilityNodeInfo.md))
- [android.view.accessibility.AccessibilityNodeInfo#setExpandedState(int)](../android/view/accessibility/AccessibilityNodeInfo.md)) 

### CONTENT_CHANGE_TYPE_PANE_APPEARED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTENT_CHANGE_TYPE_PANE_APPEARED: Int
```

Change type for [TYPE_WINDOW_STATE_CHANGED](../android/view/accessibility/AccessibilityEvent.md) event: The node has a pane title, and either just appeared or just was assigned a title when it had none before. 

 Value: 16

**See Also**

- [android.view.View#setAccessibilityPaneTitle(CharSequence)](../android/view/View.md)) 

### CONTENT_CHANGE_TYPE_PANE_DISAPPEARED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTENT_CHANGE_TYPE_PANE_DISAPPEARED: Int
```

Change type for [TYPE_WINDOW_STATE_CHANGED](../android/view/accessibility/AccessibilityEvent.md) event: Can mean one of two slightly different things. The primary meaning is that the node has a pane title, and was removed from the node hierarchy. It will also be sent if the pane title is set to`null`after it contained a title. No source will be returned if the node is no longer on the screen. To make the change more clear for the user, the first entry in [getText()](../android/view/accessibility/AccessibilityRecord.md))will return the value that would have been returned by`getSource().getPaneTitle()`. 

 Value: 32

**See Also**

- [android.view.View#setAccessibilityPaneTitle(CharSequence)](../android/view/View.md)) 

### CONTENT_CHANGE_TYPE_PANE_TITLE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTENT_CHANGE_TYPE_PANE_TITLE: Int
```

Change type for [TYPE_WINDOW_STATE_CHANGED](../android/view/accessibility/AccessibilityEvent.md) event: The node's pane title changed.

If this makes the pane appear, [CONTENT_CHANGE_TYPE_PANE_APPEARED](../android/view/accessibility/AccessibilityEvent.md) is sent instead. If this makes the pane disappear, [CONTENT_CHANGE_TYPE_PANE_DISAPPEARED](../android/view/accessibility/AccessibilityEvent.md) is sent. 

 Value: 8

**See Also**

- [android.view.View#setAccessibilityPaneTitle(CharSequence)](../android/view/View.md)) 

### CONTENT_CHANGE_TYPE_SORT_DIRECTION

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTENT_CHANGE_TYPE_SORT_DIRECTION: Int
```

Change type for [TYPE_WINDOW_CONTENT_CHANGED](../android/view/accessibility/AccessibilityEvent.md) event: The source node's collection item info changed its sort direction state for the data corresponding to this collection item, which is returned by [AccessibilityNodeInfo.CollectionItemInfo.getSortDirection()](../android/view/accessibility/AccessibilityNodeInfo.CollectionItemInfo.md)). The view changing its collection item info's sort direction should set a [AccessibilityNodeInfo.CollectionItemInfo](../android/view/accessibility/AccessibilityNodeInfo.CollectionItemInfo.md) created with [AccessibilityNodeInfo.CollectionItemInfo.Builder.setSortDirection(int)](../android/view/accessibility/AccessibilityNodeInfo.CollectionItemInfo.Builder.md))and then send this event. 

 Value: 65536

**See Also**

- [android.view.accessibility.AccessibilityNodeInfo.CollectionItemInfo#getSortDirection()](../android/view/accessibility/AccessibilityNodeInfo.CollectionItemInfo.md))
- [android.view.accessibility.AccessibilityNodeInfo.CollectionItemInfo.Builder#setSortDirection(int)](../android/view/accessibility/AccessibilityNodeInfo.CollectionItemInfo.Builder.md)) 

### CONTENT_CHANGE_TYPE_STATE_DESCRIPTION

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTENT_CHANGE_TYPE_STATE_DESCRIPTION: Int
```

Change type for [TYPE_WINDOW_CONTENT_CHANGED](../android/view/accessibility/AccessibilityEvent.md) event: state description of the node as returned by [AccessibilityNodeInfo.getStateDescription](../android/view/accessibility/AccessibilityNodeInfo.md))changed. If part of the state description changes, the changed part can be put into event text. For example, if state description changed from "on, wifi signal full" to "on, wifi three bars", "wifi three bars" can be put into the event text. 

 Value: 64

**See Also**

- [android.view.View#setStateDescription(CharSequence)](../android/view/View.md)) 

### CONTENT_CHANGE_TYPE_SUBTREE

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTENT_CHANGE_TYPE_SUBTREE: Int
```

Change type for [TYPE_WINDOW_CONTENT_CHANGED](../android/view/accessibility/AccessibilityEvent.md) event: One or more content changes occurred in the the subtree rooted at the source node, or the subtree's structure changed when a node was added or removed. 

 Value: 1

### CONTENT_CHANGE_TYPE_SUPPLEMENTAL_DESCRIPTION

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTENT_CHANGE_TYPE_SUPPLEMENTAL_DESCRIPTION: Int
```

Change type for [TYPE_WINDOW_CONTENT_CHANGED](../android/view/accessibility/AccessibilityEvent.md) event: The source node changed its supplemental description, which is returned by [AccessibilityNodeInfo.getSupplementalDescription()](../android/view/accessibility/AccessibilityNodeInfo.md)). The view changing its supplemental description should call [AccessibilityNodeInfo.setSupplementalDescription(CharSequence)](../android/view/accessibility/AccessibilityNodeInfo.md))and then send this event. 

 Value: 32768

**See Also**

- [android.view.accessibility.AccessibilityNodeInfo#getSupplementalDescription()](../android/view/accessibility/AccessibilityNodeInfo.md))
- [android.view.accessibility.AccessibilityNodeInfo#setSupplementalDescription(CharSequence)](../android/view/accessibility/AccessibilityNodeInfo.md)) 

### CONTENT_CHANGE_TYPE_TEXT

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTENT_CHANGE_TYPE_TEXT: Int
```

Change type for [TYPE_WINDOW_CONTENT_CHANGED](../android/view/accessibility/AccessibilityEvent.md) event: The node's text changed. 

 Value: 2

**See Also**

- [android.view.accessibility.AccessibilityNodeInfo#setText(CharSequence)](../android/view/accessibility/AccessibilityNodeInfo.md)) 

### CONTENT_CHANGE_TYPE_UNDEFINED

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTENT_CHANGE_TYPE_UNDEFINED: Int
```

Change type for [TYPE_WINDOW_CONTENT_CHANGED](../android/view/accessibility/AccessibilityEvent.md) event: The type of change is not defined. 

 Value: 0

### INVALID_POSITION

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INVALID_POSITION: Int
```

Invalid selection/focus position. 

 Value: -1

**See Also**

- [#getCurrentItemIndex()](../android/view/accessibility/AccessibilityRecord.md)) 

### MAX_TEXT_LENGTH

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MAX_TEXT_LENGTH: Int
```

**Deprecated:** *Deprecated in Java.*

Maximum length of the text fields. 

 Value: 500

**See Also**

- [#getBeforeText()](../android/view/accessibility/AccessibilityRecord.md))
- [#getText()](../android/view/accessibility/AccessibilityRecord.md)) 

### SPEECH_STATE_LISTENING_END

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SPEECH_STATE_LISTENING_END: Int
```

Change type for [TYPE_SPEECH_STATE_CHANGE](../android/view/accessibility/AccessibilityEvent.md) event: another service is no longer listening to the microphone. 

 Value: 8

### SPEECH_STATE_LISTENING_START

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SPEECH_STATE_LISTENING_START: Int
```

Change type for [TYPE_SPEECH_STATE_CHANGE](../android/view/accessibility/AccessibilityEvent.md) event: another service is listening to the microphone. 

 Value: 4

### SPEECH_STATE_SPEAKING_END

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SPEECH_STATE_SPEAKING_END: Int
```

Change type for [TYPE_SPEECH_STATE_CHANGE](../android/view/accessibility/AccessibilityEvent.md) event: another service is no longer speaking. 

 Value: 2

### SPEECH_STATE_SPEAKING_START

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SPEECH_STATE_SPEAKING_START: Int
```

Change type for [TYPE_SPEECH_STATE_CHANGE](../android/view/accessibility/AccessibilityEvent.md) event: another service is speaking. 

 Value: 1

### TYPES_ALL_MASK

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPES_ALL_MASK: Int
```

Mask for [AccessibilityEvent](../android/view/accessibility/AccessibilityEvent.md) all types. 

 Value: -1

**See Also**

- [#TYPE_VIEW_CLICKED](../android/view/accessibility/AccessibilityEvent.md)
- [#TYPE_VIEW_LONG_CLICKED](../android/view/accessibility/AccessibilityEvent.md)
- [#TYPE_VIEW_SELECTED](../android/view/accessibility/AccessibilityEvent.md)
- [#TYPE_VIEW_FOCUSED](../android/view/accessibility/AccessibilityEvent.md)
- [#TYPE_VIEW_TEXT_CHANGED](../android/view/accessibility/AccessibilityEvent.md)
- [#TYPE_WINDOW_STATE_CHANGED](../android/view/accessibility/AccessibilityEvent.md)
- [#TYPE_NOTIFICATION_STATE_CHANGED](../android/view/accessibility/AccessibilityEvent.md)
- [#TYPE_VIEW_HOVER_ENTER](../android/view/accessibility/AccessibilityEvent.md)
- [#TYPE_VIEW_HOVER_EXIT](../android/view/accessibility/AccessibilityEvent.md)
- [#TYPE_TOUCH_EXPLORATION_GESTURE_START](../android/view/accessibility/AccessibilityEvent.md)
- [#TYPE_TOUCH_EXPLORATION_GESTURE_END](../android/view/accessibility/AccessibilityEvent.md)
- [#TYPE_WINDOW_CONTENT_CHANGED](../android/view/accessibility/AccessibilityEvent.md)
- [#TYPE_VIEW_SCROLLED](../android/view/accessibility/AccessibilityEvent.md)
- [#TYPE_VIEW_TEXT_SELECTION_CHANGED](../android/view/accessibility/AccessibilityEvent.md)
- [#TYPE_ANNOUNCEMENT](../android/view/accessibility/AccessibilityEvent.md)
- [#TYPE_VIEW_ACCESSIBILITY_FOCUSED](../android/view/accessibility/AccessibilityEvent.md)
- [#TYPE_VIEW_ACCESSIBILITY_FOCUS_CLEARED](../android/view/accessibility/AccessibilityEvent.md)
- [#TYPE_VIEW_TEXT_TRAVERSED_AT_MOVEMENT_GRANULARITY](../android/view/accessibility/AccessibilityEvent.md)
- [#TYPE_GESTURE_DETECTION_START](../android/view/accessibility/AccessibilityEvent.md)
- [#TYPE_GESTURE_DETECTION_END](../android/view/accessibility/AccessibilityEvent.md)
- [#TYPE_TOUCH_INTERACTION_START](../android/view/accessibility/AccessibilityEvent.md)
- [#TYPE_TOUCH_INTERACTION_END](../android/view/accessibility/AccessibilityEvent.md)
- [#TYPE_WINDOWS_CHANGED](../android/view/accessibility/AccessibilityEvent.md)
- [#TYPE_VIEW_CONTEXT_CLICKED](../android/view/accessibility/AccessibilityEvent.md)
- [#TYPE_ASSIST_READING_CONTEXT](../android/view/accessibility/AccessibilityEvent.md)
- [#TYPE_SPEECH_STATE_CHANGE](../android/view/accessibility/AccessibilityEvent.md)
- [#TYPE_VIEW_TARGETED_BY_SCROLL](../android/view/accessibility/AccessibilityEvent.md) 

### TYPE_ANNOUNCEMENT

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_ANNOUNCEMENT: Int
```

**Deprecated:** *Use one of the semantic alternative methods described in the documentation of [View.announceForAccessibility(CharSequence)](../android/view/View.md))instead of using this event, as accessibility services may choose to ignore dispatch of this event type.*

Represents the event of an application making an announcement. 

 Value: 16384

### TYPE_ASSIST_READING_CONTEXT

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_ASSIST_READING_CONTEXT: Int
```

Represents the event of the assistant currently reading the users screen context. 

 Value: 16777216

### TYPE_GESTURE_DETECTION_END

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_GESTURE_DETECTION_END: Int
```

Represents the event of ending gesture detection. 

 Value: 524288

### TYPE_GESTURE_DETECTION_START

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_GESTURE_DETECTION_START: Int
```

Represents the event of beginning gesture detection. 

 Value: 262144

### TYPE_NOTIFICATION_STATE_CHANGED

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_NOTIFICATION_STATE_CHANGED: Int
```

Represents the event showing a [android.app.Notification](../android/app/Notification.md). 

 Value: 64

### TYPE_SPEECH_STATE_CHANGE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_SPEECH_STATE_CHANGE: Int
```

Represents a change in the speech state defined by the speech state change types. A change in the speech state occurs when an application wants to signal that it is either speaking or listening for human speech. This event helps avoid conflicts where two applications want to speak or one listens when another speaks. When sending this event, the sender should ensure that the accompanying state change types make sense. For example, the sender should not send [SPEECH_STATE_SPEAKING_START](../android/view/accessibility/AccessibilityEvent.md) and [SPEECH_STATE_SPEAKING_END](../android/view/accessibility/AccessibilityEvent.md) together. 

 Value: 33554432

**See Also**

- [#SPEECH_STATE_SPEAKING_START](../android/view/accessibility/AccessibilityEvent.md)
- [#SPEECH_STATE_SPEAKING_END](../android/view/accessibility/AccessibilityEvent.md)
- [#SPEECH_STATE_LISTENING_START](../android/view/accessibility/AccessibilityEvent.md)
- [#SPEECH_STATE_LISTENING_END](../android/view/accessibility/AccessibilityEvent.md)
- [#getSpeechStateChangeTypes](../android/view/accessibility/AccessibilityEvent.md))
- [#setSpeechStateChangeTypes](../android/view/accessibility/AccessibilityEvent.md)) 

### TYPE_TOUCH_EXPLORATION_GESTURE_END

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_TOUCH_EXPLORATION_GESTURE_END: Int
```

Represents the event of ending a touch exploration gesture. 

 Value: 1024

### TYPE_TOUCH_EXPLORATION_GESTURE_START

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_TOUCH_EXPLORATION_GESTURE_START: Int
```

Represents the event of starting a touch exploration gesture. 

 Value: 512

### TYPE_TOUCH_INTERACTION_END

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_TOUCH_INTERACTION_END: Int
```

Represents the event of the user ending to touch the screen. 

 Value: 2097152

### TYPE_TOUCH_INTERACTION_START

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_TOUCH_INTERACTION_START: Int
```

Represents the event of the user starting to touch the screen. 

 Value: 1048576

### TYPE_VIEW_ACCESSIBILITY_FOCUSED

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_VIEW_ACCESSIBILITY_FOCUSED: Int
```

Represents the event of gaining accessibility focus. 

 Value: 32768

**See Also**

- [android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction#ACTION_ACCESSIBILITY_FOCUS](../android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction.md) 

### TYPE_VIEW_ACCESSIBILITY_FOCUS_CLEARED

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_VIEW_ACCESSIBILITY_FOCUS_CLEARED: Int
```

Represents the event of clearing accessibility focus. 

 Value: 65536

**See Also**

- [android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction#ACTION_ACCESSIBILITY_FOCUS](../android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction.md) 

### TYPE_VIEW_CLICKED

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_VIEW_CLICKED: Int
```

Represents the event of clicking on a [android.view.View](../android/view/View.md) like [android.widget.Button](../android/widget/Button.md), [android.widget.CompoundButton](../android/widget/CompoundButton.md), etc.

See [AccessibilityNodeInfo.AccessibilityAction.ACTION_CLICK](../android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction.md) for more details. 

 Value: 1

### TYPE_VIEW_CONTEXT_CLICKED

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_VIEW_CONTEXT_CLICKED: Int
```

Represents the event of a context click on a [android.view.View](../android/view/View.md).

See [AccessibilityNodeInfo.AccessibilityAction.ACTION_CONTEXT_CLICK](../android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction.md) for more details. 

 Value: 8388608

### TYPE_VIEW_FOCUSED

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_VIEW_FOCUSED: Int
```

Represents the event of setting input focus of a [android.view.View](../android/view/View.md). 

 Value: 8

**See Also**

- [android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction#ACTION_ACCESSIBILITY_FOCUS](../android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction.md) 

### TYPE_VIEW_HOVER_ENTER

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_VIEW_HOVER_ENTER: Int
```

Represents the event of a hover enter over a [android.view.View](../android/view/View.md). 

 Value: 128

### TYPE_VIEW_HOVER_EXIT

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_VIEW_HOVER_EXIT: Int
```

Represents the event of a hover exit over a [android.view.View](../android/view/View.md). 

 Value: 256

### TYPE_VIEW_LONG_CLICKED

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_VIEW_LONG_CLICKED: Int
```

Represents the event of long clicking on a [android.view.View](../android/view/View.md) like [android.widget.Button](../android/widget/Button.md), [android.widget.CompoundButton](../android/widget/CompoundButton.md), etc.

See [AccessibilityNodeInfo.AccessibilityAction.ACTION_LONG_CLICK](../android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction.md) for more details. 

 Value: 2

### TYPE_VIEW_SCROLLED

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_VIEW_SCROLLED: Int
```

Represents the event of scrolling a view. This event type is generally not sent directly. In the View system, this is sent in [android.view.View#onScrollChanged(int, int, int, int)](../android/view/View.md))

In addition to the source and package name, the event should populate scroll-specific properties like [setScrollDeltaX(int)](../android/view/accessibility/AccessibilityRecord.md)), [setScrollDeltaY(int)](../android/view/accessibility/AccessibilityRecord.md)), [setMaxScrollX(int)](../android/view/accessibility/AccessibilityRecord.md)), and [setMaxScrollY(int)](../android/view/accessibility/AccessibilityRecord.md)).

Services are encouraged to rely on the source to query UI state over AccessibilityEvents properties. For example, to check after a scroll if the bottom of the scrolling UI element has been reached, check if the source node is scrollable and has the [AccessibilityNodeInfo.AccessibilityAction.ACTION_SCROLL_BACKWARD](../android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction.md) action but not the [AccessibilityNodeInfo.AccessibilityAction.ACTION_SCROLL_FORWARD](../android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction.md) action. For scrolling to a target, use [TYPE_VIEW_TARGETED_BY_SCROLL](../android/view/accessibility/AccessibilityEvent.md). 

 Value: 4096

### TYPE_VIEW_SELECTED

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_VIEW_SELECTED: Int
```

Represents the event of selecting an item usually in the context of an [android.widget.AdapterView](../android/widget/AdapterView.md). 

 Value: 4

**See Also**

- [android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction#ACTION_SELECT](../android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction.md) 

### TYPE_VIEW_TARGETED_BY_SCROLL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_VIEW_TARGETED_BY_SCROLL: Int
```

Represents the event of a scroll having completed and brought the target node on screen. 

 Value: 67108864

### TYPE_VIEW_TEXT_CHANGED

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_VIEW_TEXT_CHANGED: Int
```

Represents the event of changing the text of an [android.widget.EditText](../android/widget/EditText.md). 

 Value: 16

**See Also**

- [android.view.accessibility.AccessibilityNodeInfo#setText(CharSequence)](../android/view/accessibility/AccessibilityNodeInfo.md)) 

### TYPE_VIEW_TEXT_SELECTION_CHANGED

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_VIEW_TEXT_SELECTION_CHANGED: Int
```

Represents the event of changing the selection in an [android.widget.EditText](../android/widget/EditText.md). 

 Value: 8192

### TYPE_VIEW_TEXT_TRAVERSED_AT_MOVEMENT_GRANULARITY

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_VIEW_TEXT_TRAVERSED_AT_MOVEMENT_GRANULARITY: Int
```

Represents the event of traversing the text of a view at a given movement granularity. 

 Value: 131072

### TYPE_WINDOWS_CHANGED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_WINDOWS_CHANGED: Int
```

Represents the event change in the system windows shown on the screen. This event type should only be dispatched by the system. 

 Value: 4194304

### TYPE_WINDOW_CONTENT_CHANGED

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_WINDOW_CONTENT_CHANGED: Int
```

Represents the event of changing the content of a window and more specifically the sub-tree rooted at the event's source. 

 Value: 2048

### TYPE_WINDOW_STATE_CHANGED

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_WINDOW_STATE_CHANGED: Int
```

Represents the event of a change to a visually distinct section of the user interface.

These events should only be dispatched from [android.view.View](../android/view/View.md) s that have accessibility pane titles, and replaces [TYPE_WINDOW_CONTENT_CHANGED](../android/view/accessibility/AccessibilityEvent.md) for those sources. Details about the change are available from [getContentChangeTypes()](../android/view/accessibility/AccessibilityEvent.md)).

Do not use this to get an accessibility service to make non-pane announcements. Instead, follow the practices described in [View.announceForAccessibility(CharSequence)](../android/view/View.md)).**Note:**this does not suggest calling announceForAccessibility(), but using the suggestions listed in its documentation. 

 Value: 32

### WINDOWS_CHANGE_ACCESSIBILITY_FOCUSED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WINDOWS_CHANGE_ACCESSIBILITY_FOCUSED: Int
```

Change type for [TYPE_WINDOWS_CHANGED](../android/view/accessibility/AccessibilityEvent.md) event: The window's [AccessibilityWindowInfo.isAccessibilityFocused()](../android/view/accessibility/AccessibilityWindowInfo.md))changed. 

 Value: 128

### WINDOWS_CHANGE_ACTIVE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WINDOWS_CHANGE_ACTIVE: Int
```

Change type for [TYPE_WINDOWS_CHANGED](../android/view/accessibility/AccessibilityEvent.md) event: The window's [AccessibilityWindowInfo.isActive()](../android/view/accessibility/AccessibilityWindowInfo.md))changed. 

 Value: 32

### WINDOWS_CHANGE_ADDED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WINDOWS_CHANGE_ADDED: Int
```

Change type for [TYPE_WINDOWS_CHANGED](../android/view/accessibility/AccessibilityEvent.md) event: The window was added. 

 Value: 1

### WINDOWS_CHANGE_BOUNDS

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WINDOWS_CHANGE_BOUNDS: Int
```

Change type for [TYPE_WINDOWS_CHANGED](../android/view/accessibility/AccessibilityEvent.md) event: The window's bounds changed.

Starting in [R](../android/os/Build.VERSION_CODES.md), this event implies the window's region changed. It's also possible that region changed but bounds doesn't. 

 Value: 8

### WINDOWS_CHANGE_CHILDREN

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WINDOWS_CHANGE_CHILDREN: Int
```

Change type for [TYPE_WINDOWS_CHANGED](../android/view/accessibility/AccessibilityEvent.md) event: The window's children changed. 

 Value: 512

### WINDOWS_CHANGE_FOCUSED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WINDOWS_CHANGE_FOCUSED: Int
```

Change type for [TYPE_WINDOWS_CHANGED](../android/view/accessibility/AccessibilityEvent.md) event: The window's [AccessibilityWindowInfo.isFocused()](../android/view/accessibility/AccessibilityWindowInfo.md))changed. 

 Value: 64

### WINDOWS_CHANGE_LAYER

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WINDOWS_CHANGE_LAYER: Int
```

Change type for [TYPE_WINDOWS_CHANGED](../android/view/accessibility/AccessibilityEvent.md) event: The window's layer changed. 

 Value: 16

### WINDOWS_CHANGE_PARENT

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WINDOWS_CHANGE_PARENT: Int
```

Change type for [TYPE_WINDOWS_CHANGED](../android/view/accessibility/AccessibilityEvent.md) event: The window's parent changed. 

 Value: 256

### WINDOWS_CHANGE_PIP

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WINDOWS_CHANGE_PIP: Int
```

Change type for [TYPE_WINDOWS_CHANGED](../android/view/accessibility/AccessibilityEvent.md) event: The window either entered or exited picture-in-picture mode. 

 Value: 1024

### WINDOWS_CHANGE_REMOVED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WINDOWS_CHANGE_REMOVED: Int
```

Change type for [TYPE_WINDOWS_CHANGED](../android/view/accessibility/AccessibilityEvent.md) event: A window was removed. 

 Value: 2

### WINDOWS_CHANGE_TITLE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WINDOWS_CHANGE_TITLE: Int
```

Change type for [TYPE_WINDOWS_CHANGED](../android/view/accessibility/AccessibilityEvent.md) event: The window's title changed. 

 Value: 4

## Public constructors

### AccessibilityEvent

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AccessibilityEvent()
```

Creates a new [AccessibilityEvent](../android/view/accessibility/AccessibilityEvent.md). 

### AccessibilityEvent

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AccessibilityEvent(event: AccessibilityEvent)
```

Copy constructor. Creates a new [AccessibilityEvent](../android/view/accessibility/AccessibilityEvent.md), and this instance is initialized from the given`event`.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `event` | [AccessibilityEvent](../android/view/accessibility/AccessibilityEvent.md):The other event. This value cannot be`null`. |

### AccessibilityEvent

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AccessibilityEvent(eventType: Int)
```

Creates a new [AccessibilityEvent](../android/view/accessibility/AccessibilityEvent.md) with the given`eventType`.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------|
| `eventType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The event type. |

## Public methods

### appendRecord

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun appendRecord(record: AccessibilityRecord!): Unit
```

Appends an [AccessibilityRecord](../android/view/accessibility/AccessibilityRecord.md) to the end of event records.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `record` | [AccessibilityRecord](../android/view/accessibility/AccessibilityRecord.md)!:The record to append. |

| Exceptions ||
|-----------------------------------|-----------------------------------------|
| `java.lang.IllegalStateException` | If called from an AccessibilityService. |

### describeContents

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of [writeToParcel(android.os.Parcel,int)](../android/os/Parcelable.md)), the return value of this method must include the [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) bit.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### eventTypeToString

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun eventTypeToString(eventType: Int): String!
```

Returns the string representation of an event type. For example, [TYPE_VIEW_CLICKED](../android/view/accessibility/AccessibilityEvent.md) is represented by the string TYPE_VIEW_CLICKED.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------|
| `eventType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The event type |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The string representation. |

### getAction

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAction(): Int
```

Gets the performed action that triggered this event.

| Return ||
|----------------------------------------------------------------------------|-------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The action. |

### getContentChangeTypes

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getContentChangeTypes(): Int
```

Gets the bit mask of change types signaled by a [TYPE_WINDOW_CONTENT_CHANGED](../android/view/accessibility/AccessibilityEvent.md) event or [TYPE_WINDOW_STATE_CHANGED](../android/view/accessibility/AccessibilityEvent.md). A single event may represent multiple change types.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The bit mask of change types. One or more of: - [CONTENT_CHANGE_TYPE_CONTENT_DESCRIPTION](../android/view/accessibility/AccessibilityEvent.md) - [CONTENT_CHANGE_TYPE_STATE_DESCRIPTION](../android/view/accessibility/AccessibilityEvent.md) - [CONTENT_CHANGE_TYPE_SUBTREE](../android/view/accessibility/AccessibilityEvent.md) - [CONTENT_CHANGE_TYPE_TEXT](../android/view/accessibility/AccessibilityEvent.md) - [CONTENT_CHANGE_TYPE_PANE_TITLE](../android/view/accessibility/AccessibilityEvent.md) - [CONTENT_CHANGE_TYPE_UNDEFINED](../android/view/accessibility/AccessibilityEvent.md) - [CONTENT_CHANGE_TYPE_PANE_APPEARED](../android/view/accessibility/AccessibilityEvent.md) - [CONTENT_CHANGE_TYPE_PANE_DISAPPEARED](../android/view/accessibility/AccessibilityEvent.md) - [CONTENT_CHANGE_TYPE_DRAG_STARTED](../android/view/accessibility/AccessibilityEvent.md) - [CONTENT_CHANGE_TYPE_DRAG_DROPPED](../android/view/accessibility/AccessibilityEvent.md) - [CONTENT_CHANGE_TYPE_DRAG_CANCELLED](../android/view/accessibility/AccessibilityEvent.md) - [CONTENT_CHANGE_TYPE_CONTENT_INVALID](../android/view/accessibility/AccessibilityEvent.md) - [CONTENT_CHANGE_TYPE_ERROR](../android/view/accessibility/AccessibilityEvent.md) - [CONTENT_CHANGE_TYPE_ENABLED](../android/view/accessibility/AccessibilityEvent.md) Value is either`0`or a combination of [android.view.accessibility.AccessibilityEvent#CONTENT_CHANGE_TYPE_UNDEFINED](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#CONTENT_CHANGE_TYPE_SUBTREE](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#CONTENT_CHANGE_TYPE_TEXT](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#CONTENT_CHANGE_TYPE_CONTENT_DESCRIPTION](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#CONTENT_CHANGE_TYPE_STATE_DESCRIPTION](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#CONTENT_CHANGE_TYPE_PANE_TITLE](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#CONTENT_CHANGE_TYPE_PANE_APPEARED](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#CONTENT_CHANGE_TYPE_PANE_DISAPPEARED](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#CONTENT_CHANGE_TYPE_DRAG_STARTED](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#CONTENT_CHANGE_TYPE_DRAG_DROPPED](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#CONTENT_CHANGE_TYPE_DRAG_CANCELLED](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#CONTENT_CHANGE_TYPE_CONTENT_INVALID](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#CONTENT_CHANGE_TYPE_ERROR](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#CONTENT_CHANGE_TYPE_ENABLED](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#CONTENT_CHANGE_TYPE_CHECKED](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#CONTENT_CHANGE_TYPE_EXPANDED](../android/view/accessibility/AccessibilityEvent.md), and [android.view.accessibility.AccessibilityEvent#CONTENT_CHANGE_TYPE_SUPPLEMENTAL_DESCRIPTION](../android/view/accessibility/AccessibilityEvent.md) |

### getEventTime

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getEventTime(): Long
```

Gets the time in which this event was sent.

| Return ||
|------------------------------------------------------------------------------|-----------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The event time. |

### getEventType

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getEventType(): Int
```

Gets the event type.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The event type. Value is either`0`or a combination of [android.view.accessibility.AccessibilityEvent#TYPE_VIEW_CLICKED](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#TYPE_VIEW_LONG_CLICKED](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#TYPE_VIEW_SELECTED](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#TYPE_VIEW_FOCUSED](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#TYPE_VIEW_TEXT_CHANGED](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#TYPE_WINDOW_STATE_CHANGED](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#TYPE_NOTIFICATION_STATE_CHANGED](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#TYPE_VIEW_HOVER_ENTER](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#TYPE_VIEW_HOVER_EXIT](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#TYPE_TOUCH_EXPLORATION_GESTURE_START](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#TYPE_TOUCH_EXPLORATION_GESTURE_END](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#TYPE_WINDOW_CONTENT_CHANGED](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#TYPE_VIEW_SCROLLED](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#TYPE_VIEW_TEXT_SELECTION_CHANGED](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#TYPE_ANNOUNCEMENT](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#TYPE_VIEW_ACCESSIBILITY_FOCUSED](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#TYPE_VIEW_ACCESSIBILITY_FOCUS_CLEARED](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#TYPE_VIEW_TEXT_TRAVERSED_AT_MOVEMENT_GRANULARITY](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#TYPE_GESTURE_DETECTION_START](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#TYPE_GESTURE_DETECTION_END](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#TYPE_TOUCH_INTERACTION_START](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#TYPE_TOUCH_INTERACTION_END](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#TYPE_WINDOWS_CHANGED](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#TYPE_VIEW_CONTEXT_CLICKED](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#TYPE_ASSIST_READING_CONTEXT](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#TYPE_SPEECH_STATE_CHANGE](../android/view/accessibility/AccessibilityEvent.md), and [android.view.accessibility.AccessibilityEvent#TYPE_VIEW_TARGETED_BY_SCROLL](../android/view/accessibility/AccessibilityEvent.md) |

### getMovementGranularity

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMovementGranularity(): Int
```

Gets the movement granularity that was traversed.

| Return ||
|----------------------------------------------------------------------------|------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The granularity. |

### getPackageName

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPackageName(): CharSequence!
```

Gets the package name of the source.

| Return ||
|------------------------------------------------------------------------------------------------|-------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | The package name. |

### getRecord

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRecord(index: Int): AccessibilityRecord!
```

Gets the record at a given index.

| Parameters ||
|---------|---------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index. |

| Return ||
|-----------------------------------------------------------------------------------------------------------------------|------------------------------------|
| [AccessibilityRecord](../android/view/accessibility/AccessibilityRecord.md)! | The record at the specified index. |

### getRecordCount

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRecordCount(): Int
```

Gets the number of records contained in the event.

| Return ||
|----------------------------------------------------------------------------|------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The number of records. |

### getSpeechStateChangeTypes

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSpeechStateChangeTypes(): Int
```

Gets the bit mask of the speech state signaled by a [TYPE_SPEECH_STATE_CHANGE](../android/view/accessibility/AccessibilityEvent.md) event.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The bit mask of speech change types. |

**See Also**

- [#SPEECH_STATE_SPEAKING_START](../android/view/accessibility/AccessibilityEvent.md)
- [#SPEECH_STATE_SPEAKING_END](../android/view/accessibility/AccessibilityEvent.md)
- [#SPEECH_STATE_LISTENING_START](../android/view/accessibility/AccessibilityEvent.md)
- [#SPEECH_STATE_LISTENING_END](../android/view/accessibility/AccessibilityEvent.md) 

### getWindowChanges

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getWindowChanges(): Int
```

Get the bit mask of change types signaled by a [TYPE_WINDOWS_CHANGED](../android/view/accessibility/AccessibilityEvent.md) event. A single event may represent multiple change types.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The bit mask of change types. Value is either`0`or a combination of [android.view.accessibility.AccessibilityEvent#WINDOWS_CHANGE_ADDED](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#WINDOWS_CHANGE_REMOVED](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#WINDOWS_CHANGE_TITLE](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#WINDOWS_CHANGE_BOUNDS](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#WINDOWS_CHANGE_LAYER](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#WINDOWS_CHANGE_ACTIVE](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#WINDOWS_CHANGE_FOCUSED](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#WINDOWS_CHANGE_ACCESSIBILITY_FOCUSED](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#WINDOWS_CHANGE_PARENT](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#WINDOWS_CHANGE_CHILDREN](../android/view/accessibility/AccessibilityEvent.md), and [android.view.accessibility.AccessibilityEvent#WINDOWS_CHANGE_PIP](../android/view/accessibility/AccessibilityEvent.md) |

**See Also**

- [#WINDOWS_CHANGE_ADDED](../android/view/accessibility/AccessibilityEvent.md)
- [#WINDOWS_CHANGE_REMOVED](../android/view/accessibility/AccessibilityEvent.md)
- [#WINDOWS_CHANGE_TITLE](../android/view/accessibility/AccessibilityEvent.md)
- [#WINDOWS_CHANGE_BOUNDS](../android/view/accessibility/AccessibilityEvent.md)
- [#WINDOWS_CHANGE_LAYER](../android/view/accessibility/AccessibilityEvent.md)
- [#WINDOWS_CHANGE_ACTIVE](../android/view/accessibility/AccessibilityEvent.md)
- [#WINDOWS_CHANGE_FOCUSED](../android/view/accessibility/AccessibilityEvent.md)
- [#WINDOWS_CHANGE_ACCESSIBILITY_FOCUSED](../android/view/accessibility/AccessibilityEvent.md)
- [#WINDOWS_CHANGE_PARENT](../android/view/accessibility/AccessibilityEvent.md)
- [#WINDOWS_CHANGE_CHILDREN](../android/view/accessibility/AccessibilityEvent.md)
- [#WINDOWS_CHANGE_PIP](../android/view/accessibility/AccessibilityEvent.md) 

### initFromParcel

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun initFromParcel(parcel: Parcel!): Unit
```

Creates a new instance from a [Parcel](../android/os/Parcel.md).

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parcel` | [Parcel](../android/os/Parcel.md)!:A parcel containing the state of a [AccessibilityEvent](../android/view/accessibility/AccessibilityEvent.md). |

### isAccessibilityDataSensitive

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isAccessibilityDataSensitive(): Boolean
```

Whether the event should only be delivered to an [android.accessibilityservice.AccessibilityService](../android/accessibilityservice/AccessibilityService.md) with the [android.accessibilityservice.AccessibilityServiceInfo#isAccessibilityTool](../android/accessibilityservice/AccessibilityServiceInfo.md))property set to true.

Initial value matches the [android.view.View#isAccessibilityDataSensitive](../android/view/View.md))property from the event's source node, if present, or false by default.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the event should be delivered only to isAccessibilityTool services, false otherwise. |

**See Also**

- [#setAccessibilityDataSensitive](../android/view/accessibility/AccessibilityEvent.md)) 

### obtain

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun obtain(): AccessibilityEvent!
```

**Deprecated:** *Object pooling has been discontinued. Create a new instance using the constructor [AccessibilityEvent()](../android/view/accessibility/AccessibilityEvent.md))instead.*

Instantiates a new AccessibilityEvent instance.

| Return ||
|----------------------------------------------------------------------------------------------------------------------|--------------|
| [AccessibilityEvent](../android/view/accessibility/AccessibilityEvent.md)! | An instance. |

### obtain

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun obtain(event: AccessibilityEvent!): AccessibilityEvent!
```

**Deprecated:** *Object pooling has been discontinued. Create a new instance using the constructor [AccessibilityEvent()](../android/view/accessibility/AccessibilityEvent.md))instead.*

Instantiates a new AccessibilityEvent instance. The returned instance is initialized from the given`event`.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------|
| `event` | [AccessibilityEvent](../android/view/accessibility/AccessibilityEvent.md)!:The other event. |

| Return ||
|----------------------------------------------------------------------------------------------------------------------|--------------|
| [AccessibilityEvent](../android/view/accessibility/AccessibilityEvent.md)! | An instance. |

### obtain

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun obtain(eventType: Int): AccessibilityEvent!
```

**Deprecated:** *Object pooling has been discontinued. Create a new instance using the constructor [AccessibilityEvent()](../android/view/accessibility/AccessibilityEvent.md))instead.*

Instantiates a new AccessibilityEvent instance with its type property set.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------|
| `eventType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The event type. |

| Return ||
|----------------------------------------------------------------------------------------------------------------------|--------------|
| [AccessibilityEvent](../android/view/accessibility/AccessibilityEvent.md)! | An instance. |

### recycle

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun recycle(): Unit
```

**Deprecated:** *Object pooling has been discontinued. Calling this function now will have no effect.*

Previously would recycle an instance back to be reused. 

### setAccessibilityDataSensitive

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setAccessibilityDataSensitive(accessibilityDataSensitive: Boolean): Unit
```

Sets whether the event should only be delivered to an [android.accessibilityservice.AccessibilityService](../android/accessibilityservice/AccessibilityService.md) with the [android.accessibilityservice.AccessibilityServiceInfo#isAccessibilityTool](../android/accessibilityservice/AccessibilityServiceInfo.md))property set to true.

This will be set automatically based on the event's source (if present). If creating and sending an event directly through [AccessibilityManager](../android/view/accessibility/AccessibilityManager.md)(where an event may have no source) then this method must be called explicitly if you want non-default behavior.

| Parameters ||
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `accessibilityDataSensitive` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):True if the event should be delivered only to isAccessibilityTool services, false otherwise. |

| Exceptions ||
|-----------------------------------|-----------------------------------------|
| `java.lang.IllegalStateException` | If called from an AccessibilityService. |

### setAction

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setAction(action: Int): Unit
```

Sets the performed action that triggered this event.

Valid actions are defined in [AccessibilityNodeInfo](../android/view/accessibility/AccessibilityNodeInfo.md):

- [AccessibilityNodeInfo.ACTION_ACCESSIBILITY_FOCUS](../android/view/accessibility/AccessibilityNodeInfo.md)
- [AccessibilityNodeInfo.ACTION_CLEAR_ACCESSIBILITY_FOCUS](../android/view/accessibility/AccessibilityNodeInfo.md)
- [AccessibilityNodeInfo.ACTION_CLEAR_FOCUS](../android/view/accessibility/AccessibilityNodeInfo.md)
- [AccessibilityNodeInfo.ACTION_CLEAR_SELECTION](../android/view/accessibility/AccessibilityNodeInfo.md)
- [AccessibilityNodeInfo.ACTION_CLICK](../android/view/accessibility/AccessibilityNodeInfo.md)
- [AccessibilityNodeInfo.ACTION_LONG_CLICK](../android/view/accessibility/AccessibilityNodeInfo.md)
- [AccessibilityNodeInfo.ACTION_NEXT_AT_MOVEMENT_GRANULARITY](../android/view/accessibility/AccessibilityNodeInfo.md)
- [AccessibilityNodeInfo.ACTION_PREVIOUS_AT_MOVEMENT_GRANULARITY](../android/view/accessibility/AccessibilityNodeInfo.md)
- [AccessibilityNodeInfo.ACTION_NEXT_HTML_ELEMENT](../android/view/accessibility/AccessibilityNodeInfo.md)
- [AccessibilityNodeInfo.ACTION_PREVIOUS_HTML_ELEMENT](../android/view/accessibility/AccessibilityNodeInfo.md)
- [AccessibilityNodeInfo.ACTION_SCROLL_FORWARD](../android/view/accessibility/AccessibilityNodeInfo.md)
- [AccessibilityNodeInfo.ACTION_SCROLL_BACKWARD](../android/view/accessibility/AccessibilityNodeInfo.md)
- [AccessibilityNodeInfo.ACTION_COPY](../android/view/accessibility/AccessibilityNodeInfo.md)
- [AccessibilityNodeInfo.ACTION_PASTE](../android/view/accessibility/AccessibilityNodeInfo.md)
- [AccessibilityNodeInfo.ACTION_CUT](../android/view/accessibility/AccessibilityNodeInfo.md)
- [AccessibilityNodeInfo.ACTION_SET_SELECTION](../android/view/accessibility/AccessibilityNodeInfo.md)
- [AccessibilityNodeInfo.ACTION_EXPAND](../android/view/accessibility/AccessibilityNodeInfo.md)
- [AccessibilityNodeInfo.ACTION_COLLAPSE](../android/view/accessibility/AccessibilityNodeInfo.md)
- [AccessibilityNodeInfo.ACTION_DISMISS](../android/view/accessibility/AccessibilityNodeInfo.md)
- [AccessibilityNodeInfo.ACTION_SET_TEXT](../android/view/accessibility/AccessibilityNodeInfo.md)
- etc.

| Parameters ||
|----------|----------------------------------------------------------------------------------------|
| `action` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The action. |

| Exceptions ||
|-----------------------------------|-----------------------------------------|
| `java.lang.IllegalStateException` | If called from an AccessibilityService. |

**See Also**

- [android.view.accessibility.AccessibilityNodeInfo#performAction(int)](../android/view/accessibility/AccessibilityNodeInfo.md)) 

### setContentChangeTypes

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setContentChangeTypes(changeTypes: Int): Unit
```

Sets the bit mask of node tree changes signaled by an [TYPE_WINDOW_CONTENT_CHANGED](../android/view/accessibility/AccessibilityEvent.md) event.

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `changeTypes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The bit mask of change types. Value is either`0`or a combination of [android.view.accessibility.AccessibilityEvent#CONTENT_CHANGE_TYPE_UNDEFINED](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#CONTENT_CHANGE_TYPE_SUBTREE](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#CONTENT_CHANGE_TYPE_TEXT](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#CONTENT_CHANGE_TYPE_CONTENT_DESCRIPTION](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#CONTENT_CHANGE_TYPE_STATE_DESCRIPTION](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#CONTENT_CHANGE_TYPE_PANE_TITLE](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#CONTENT_CHANGE_TYPE_PANE_APPEARED](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#CONTENT_CHANGE_TYPE_PANE_DISAPPEARED](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#CONTENT_CHANGE_TYPE_DRAG_STARTED](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#CONTENT_CHANGE_TYPE_DRAG_DROPPED](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#CONTENT_CHANGE_TYPE_DRAG_CANCELLED](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#CONTENT_CHANGE_TYPE_CONTENT_INVALID](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#CONTENT_CHANGE_TYPE_ERROR](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#CONTENT_CHANGE_TYPE_ENABLED](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#CONTENT_CHANGE_TYPE_CHECKED](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#CONTENT_CHANGE_TYPE_EXPANDED](../android/view/accessibility/AccessibilityEvent.md), and [android.view.accessibility.AccessibilityEvent#CONTENT_CHANGE_TYPE_SUPPLEMENTAL_DESCRIPTION](../android/view/accessibility/AccessibilityEvent.md) |

| Exceptions ||
|-----------------------------------|-----------------------------------------|
| `java.lang.IllegalStateException` | If called from an AccessibilityService. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getContentChangeTypes()> 

### setEventTime

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setEventTime(eventTime: Long): Unit
```

Sets the time in which this event was sent.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------|
| `eventTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The event time. |

| Exceptions ||
|-----------------------------------|-----------------------------------------|
| `java.lang.IllegalStateException` | If called from an AccessibilityService. |

### setEventType

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setEventType(eventType: Int): Unit
```

Sets the event type.**Note: An event must represent a single event type.**

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `eventType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The event type. Value is either`0`or a combination of [android.view.accessibility.AccessibilityEvent#TYPE_VIEW_CLICKED](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#TYPE_VIEW_LONG_CLICKED](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#TYPE_VIEW_SELECTED](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#TYPE_VIEW_FOCUSED](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#TYPE_VIEW_TEXT_CHANGED](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#TYPE_WINDOW_STATE_CHANGED](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#TYPE_NOTIFICATION_STATE_CHANGED](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#TYPE_VIEW_HOVER_ENTER](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#TYPE_VIEW_HOVER_EXIT](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#TYPE_TOUCH_EXPLORATION_GESTURE_START](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#TYPE_TOUCH_EXPLORATION_GESTURE_END](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#TYPE_WINDOW_CONTENT_CHANGED](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#TYPE_VIEW_SCROLLED](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#TYPE_VIEW_TEXT_SELECTION_CHANGED](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#TYPE_ANNOUNCEMENT](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#TYPE_VIEW_ACCESSIBILITY_FOCUSED](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#TYPE_VIEW_ACCESSIBILITY_FOCUS_CLEARED](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#TYPE_VIEW_TEXT_TRAVERSED_AT_MOVEMENT_GRANULARITY](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#TYPE_GESTURE_DETECTION_START](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#TYPE_GESTURE_DETECTION_END](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#TYPE_TOUCH_INTERACTION_START](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#TYPE_TOUCH_INTERACTION_END](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#TYPE_WINDOWS_CHANGED](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#TYPE_VIEW_CONTEXT_CLICKED](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#TYPE_ASSIST_READING_CONTEXT](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#TYPE_SPEECH_STATE_CHANGE](../android/view/accessibility/AccessibilityEvent.md), and [android.view.accessibility.AccessibilityEvent#TYPE_VIEW_TARGETED_BY_SCROLL](../android/view/accessibility/AccessibilityEvent.md) |

| Exceptions ||
|-----------------------------------|-----------------------------------------|
| `java.lang.IllegalStateException` | If called from an AccessibilityService. |

### setMovementGranularity

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setMovementGranularity(granularity: Int): Unit
```

Sets the movement granularity that was traversed.

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------|
| `granularity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The granularity. |

| Exceptions ||
|-----------------------------------|-----------------------------------------|
| `java.lang.IllegalStateException` | If called from an AccessibilityService. |

### setPackageName

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setPackageName(packageName: CharSequence!): Unit
```

Sets the package name of the source.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------|
| `packageName` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:The package name. |

| Exceptions ||
|-----------------------------------|-----------------------------------------|
| `java.lang.IllegalStateException` | If called from an AccessibilityService. |

### setSpeechStateChangeTypes

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setSpeechStateChangeTypes(state: Int): Unit
```

Sets the bit mask of the speech state change types signaled by a [TYPE_SPEECH_STATE_CHANGE](../android/view/accessibility/AccessibilityEvent.md) event. The sender is responsible for ensuring that the state change types make sense. For example, the sender should not send [SPEECH_STATE_SPEAKING_START](../android/view/accessibility/AccessibilityEvent.md) and [SPEECH_STATE_SPEAKING_END](../android/view/accessibility/AccessibilityEvent.md) together.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `state` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is either`0`or a combination of [android.view.accessibility.AccessibilityEvent#SPEECH_STATE_SPEAKING_START](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#SPEECH_STATE_SPEAKING_END](../android/view/accessibility/AccessibilityEvent.md), [android.view.accessibility.AccessibilityEvent#SPEECH_STATE_LISTENING_START](../android/view/accessibility/AccessibilityEvent.md), and [android.view.accessibility.AccessibilityEvent#SPEECH_STATE_LISTENING_END](../android/view/accessibility/AccessibilityEvent.md) |

**See Also**

- [#SPEECH_STATE_SPEAKING_START](../android/view/accessibility/AccessibilityEvent.md)
- [#SPEECH_STATE_SPEAKING_END](../android/view/accessibility/AccessibilityEvent.md)
- [#SPEECH_STATE_LISTENING_START](../android/view/accessibility/AccessibilityEvent.md)
- [#SPEECH_STATE_LISTENING_END](../android/view/accessibility/AccessibilityEvent.md) 

### toString

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    parcel: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<AccessibilityEvent!>
```  
**See Also**

- [android.os.Parcelable.Creator](../android/os/Parcelable.Creator.md)
