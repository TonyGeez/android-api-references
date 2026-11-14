# AccessibilityEvent

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AccessibilityEvent

Kotlin| [Java](https://developer.android.com/reference/android/view/accessibility/AccessibilityEvent "View this page in Java") 
| --- | --- |

```
class AccessibilityEvent : AccessibilityRecord, Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.view.accessibility.AccessibilityRecord](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord) ||
| | ↳ | [android.view.accessibility.AccessibilityEvent](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#) |

This class represents accessibility events that are sent by the system when something notable happens in the user interface. For example, when a [android.widget.Button](https://developer.android.com/reference/kotlin/android/widget/Button.html#) is clicked, a [android.view.View](https://developer.android.com/reference/kotlin/android/view/View.html#) is focused, etc.

An accessibility event is fired by an individual view which populates the event with data for its state and requests from its parent to send the event to interested parties. The parent can optionally modify or even block the event based on its broader understanding of the user interface's context.

The main purpose of an accessibility event is to communicate changes in the UI to an [android.accessibilityservice.AccessibilityService](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#). If needed, the service may then inspect the user interface by examining the View hierarchy through the event's [source](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getSource()), as represented by a tree of [AccessibilityNodeInfo](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo) s (snapshot of a View state) which can be used for exploring the window content. Note that the privilege for accessing an event's source, thus the window content, has to be explicitly requested. For more details refer to [android.accessibilityservice.AccessibilityService](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#). If an accessibility service has not requested to retrieve the window content the event will not contain reference to its source.**Note:** for events of type [TYPE_NOTIFICATION_STATE_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_NOTIFICATION_STATE_CHANGED:kotlin.Int) the source is never available, and Views that set [android.view.View#isAccessibilityDataSensitive()](https://developer.android.com/reference/kotlin/android/view/View.html#isAccessibilityDataSensitive())may not populate all event properties on events sent from higher up in the view hierarchy.

This class represents various semantically different accessibility event types. Each event type has an associated set of related properties. In other words, each event type is characterized via a subset of the properties exposed by this class. For each event type there is a corresponding constant defined in this class. Follows a specification of the event types and their associated properties:
|
| ### Developer Guides
|
| For more information about creating and processing AccessibilityEvents, read the [Accessibility](https://developer.android.com/guide/topics/ui/accessibility/index.html) developer guide.

**VIEW TYPES** 

**View clicked** - represents the event of clicking on a [android.view.View](https://developer.android.com/reference/kotlin/android/view/View.html#) like [android.widget.Button](https://developer.android.com/reference/kotlin/android/widget/Button.html#), [android.widget.CompoundButton](https://developer.android.com/reference/kotlin/android/widget/CompoundButton.html#), etc. 
*Type:* [TYPE_VIEW_CLICKED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_CLICKED:kotlin.Int) 
*Properties:* 

- [getEventType()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getEventType())- The type of the event.
- [getSource()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getSource())- The source info (for registered clients).
- [getClassName()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getClassName())- The class name of the source.
- [getPackageName()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getPackageName())- The package name of the source.
- [getEventTime()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getEventTime())- The event time.

<br />

**View long clicked** - represents the event of long clicking on a [android.view.View](https://developer.android.com/reference/kotlin/android/view/View.html#) like [android.widget.Button](https://developer.android.com/reference/kotlin/android/widget/Button.html#), [android.widget.CompoundButton](https://developer.android.com/reference/kotlin/android/widget/CompoundButton.html#), etc 
*Type:* [TYPE_VIEW_LONG_CLICKED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_LONG_CLICKED:kotlin.Int) 
*Properties:* 

- [getEventType()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getEventType())- The type of the event.
- [getSource()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getSource())- The source info (for registered clients).
- [getClassName()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getClassName())- The class name of the source.
- [getPackageName()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getPackageName())- The package name of the source.
- [getEventTime()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getEventTime())- The event time.

<br />

**View selected** - represents the event of selecting an item usually in the context of an [android.widget.AdapterView](https://developer.android.com/reference/kotlin/android/widget/AdapterView.html#). 
*Type:* [TYPE_VIEW_SELECTED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_SELECTED:kotlin.Int) 
*Properties:* 

- [getEventType()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getEventType())- The type of the event.
- [getSource()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getSource())- The source info (for registered clients).
- [getClassName()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getClassName())- The class name of the source.
- [getPackageName()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getPackageName())- The package name of the source.
- [getEventTime()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getEventTime())- The event time.

<br />

**View focused** - represents the event of focusing a [android.view.View](https://developer.android.com/reference/kotlin/android/view/View.html#). 
*Type:* [TYPE_VIEW_FOCUSED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_FOCUSED:kotlin.Int) 
*Properties:* 

- [getEventType()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getEventType())- The type of the event.
- [getSource()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getSource())- The source info (for registered clients).
- [getClassName()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getClassName())- The class name of the source.
- [getPackageName()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getPackageName())- The package name of the source.
- [getEventTime()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getEventTime())- The event time.

<br />

**View text changed** - represents the event of changing the text of an [android.widget.EditText](https://developer.android.com/reference/kotlin/android/widget/EditText.html#). 
*Type:* [TYPE_VIEW_TEXT_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_TEXT_CHANGED:kotlin.Int) 
*Properties:* 

- [getEventType()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getEventType())- The type of the event.
- [getSource()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getSource())- The source info (for registered clients).
- [getClassName()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getClassName())- The class name of the source.
- [getPackageName()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getPackageName())- The package name of the source.
- [getEventTime()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getEventTime())- The event time.
- [getText()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getText())- The new text of the source.
- [getBeforeText()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getBeforeText())- The text of the source before the change.
- [getFromIndex()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getFromIndex())- The text change start index.
- [getAddedCount()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getAddedCount())- The number of added characters.
- [getRemovedCount()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getRemovedCount())- The number of removed characters.

<br />

**View text selection changed** - represents the event of changing the text selection of an [android.widget.EditText](https://developer.android.com/reference/kotlin/android/widget/EditText.html#). 
*Type:* [TYPE_VIEW_TEXT_SELECTION_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_TEXT_SELECTION_CHANGED:kotlin.Int) 
*Properties:* 

- [getEventType()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getEventType())- The type of the event.
- [getSource()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getSource())- The source info (for registered clients).
- [getClassName()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getClassName())- The class name of the source.
- [getPackageName()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getPackageName())- The package name of the source.
- [getEventTime()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getEventTime())- The event time.

<br />

**View text traversed at movement granularity** - represents the event of traversing the text of a view at a given granularity. For example, moving to the next word. 
*Type:* [TYPE_VIEW_TEXT_TRAVERSED_AT_MOVEMENT_GRANULARITY](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_TEXT_TRAVERSED_AT_MOVEMENT_GRANULARITY:kotlin.Int) 
*Properties:* 

- [getEventType()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getEventType())- The type of the event.
- [getSource()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getSource())- The source info (for registered clients).
- [getClassName()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getClassName())- The class name of the source.
- [getPackageName()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getPackageName())- The package name of the source.
- [getEventTime()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getEventTime())- The event time.
- [getMovementGranularity()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getMovementGranularity())- Sets the granularity at which a view's text was traversed.
- [getText()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getText())- The text of the source's sub-tree.
- [getFromIndex()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getFromIndex())- The start the text that was skipped over in this movement. This is the starting point when moving forward through the text, but not when moving back.
- [getToIndex()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getToIndex())- The end of the text that was skipped over in this movement. This is the ending point when moving forward through the text, but not when moving back.
- [getAction()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getAction())- Gets traversal action which specifies the direction.

<br />

**View scrolled** - represents the event of scrolling a view. 
*Type:* [TYPE_VIEW_SCROLLED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_SCROLLED:kotlin.Int) 
*Properties:* 

- [getEventType()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getEventType())- The type of the event.
- [getSource()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getSource())- The source info (for registered clients).
- [getClassName()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getClassName())- The class name of the source.
- [getPackageName()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getPackageName())- The package name of the source.
- [getEventTime()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getEventTime())- The event time.
- [getScrollDeltaX()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getScrollDeltaX())- The difference in the horizontal position.
- [getScrollDeltaY()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getScrollDeltaY())- The difference in the vertical position.
- [getMaxScrollX()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getMaxScrollX())()} - The max scroll offset of the source left edge
- [getMaxScrollY()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getMaxScrollY())()} - The max scroll offset of the source top edge.

<br />

**TRANSITION TYPES** 

**Window state changed** - represents the event of a change to a section of the user interface that is visually distinct. Should be sent from either the root view of a window or from a view that is marked as a pane [android.view.View#setAccessibilityPaneTitle(CharSequence)](https://developer.android.com/reference/kotlin/android/view/View.html#setAccessibilityPaneTitle(kotlin.CharSequence)). Note that changes to true windows are represented by [TYPE_WINDOWS_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOWS_CHANGED:kotlin.Int). 
*Type:* [TYPE_WINDOW_STATE_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOW_STATE_CHANGED:kotlin.Int) 
*Properties:* 

- [getEventType()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getEventType())- The type of the event.
- [getContentChangeTypes()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getContentChangeTypes())- The type of state changes.
- [getSource()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getSource())- The source info (for registered clients).
- [getClassName()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getClassName())- The class name of the source.
- [getPackageName()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getPackageName())- The package name of the source.
- [getEventTime()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getEventTime())- The event time.
- [getText()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getText())- The text of the source's sub-tree, including the pane titles.

<br />

**Window content changed** - represents the event of change in the content of a window. This change can be adding/removing view, changing a view size, etc. 

*Type:* [TYPE_WINDOW_CONTENT_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOW_CONTENT_CHANGED:kotlin.Int) 
*Properties:* 

- [getEventType()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getEventType())- The type of the event.
- [getContentChangeTypes()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getContentChangeTypes())- The type of content changes.
- [getSource()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getSource())- The source info (for registered clients).
- [getClassName()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getClassName())- The class name of the source.
- [getPackageName()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getPackageName())- The package name of the source.
- [getEventTime()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getEventTime())- The event time.

<br />

**Windows changed** - represents a change in the windows shown on the screen such as a window appeared, a window disappeared, a window size changed, a window layer changed, etc. These events should only come from the system, which is responsible for managing windows. The list of windows is available from [android.accessibilityservice.AccessibilityService#getWindows()](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#getWindows()). For regions of the user interface that are presented as windows but are controlled by an app's process, use [TYPE_WINDOW_STATE_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOW_STATE_CHANGED:kotlin.Int). 
*Type:* [TYPE_WINDOWS_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOWS_CHANGED:kotlin.Int) 
*Properties:* 

- [getEventType()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getEventType())- The type of the event.
- [getEventTime()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getEventTime())- The event time.
- [getWindowChanges()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getWindowChanges())
- The specific change to the source window

*Note:* You can retrieve the [AccessibilityWindowInfo](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo) for the window source of the event by looking through the list returned by [android.accessibilityservice.AccessibilityService#getWindows()](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#getWindows())for the window whose ID matches [getWindowId()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getWindowId()).

<br />

**NOTIFICATION TYPES** 

**Notification state changed** - represents the event showing a transient piece of information to the user. This information may be a [android.app.Notification](https://developer.android.com/reference/kotlin/android/app/Notification.html#) or [android.widget.Toast](https://developer.android.com/reference/kotlin/android/widget/Toast.html#). 
*Type:* [TYPE_NOTIFICATION_STATE_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_NOTIFICATION_STATE_CHANGED:kotlin.Int) 
*Properties:* 

- [getEventType()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getEventType())- The type of the event.
- [getClassName()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getClassName())- The class name of the source.
- [getPackageName()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getPackageName())- The package name of the source.
- [getEventTime()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getEventTime())- The event time.
- [getParcelableData()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getParcelableData())- The posted [android.app.Notification](https://developer.android.com/reference/kotlin/android/app/Notification.html#), if applicable.
- [getText()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getText())- Displayed text of the [android.widget.Toast](https://developer.android.com/reference/kotlin/android/widget/Toast.html#), if applicable, or may contain text from the [android.app.Notification](https://developer.android.com/reference/kotlin/android/app/Notification.html#), although [getParcelableData()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getParcelableData())is a richer set of data for [android.app.Notification](https://developer.android.com/reference/kotlin/android/app/Notification.html#).

<br />

**EXPLORATION TYPES** 

**View hover enter** - represents the event of beginning to hover over a [android.view.View](https://developer.android.com/reference/kotlin/android/view/View.html#). The hover may be generated via exploring the screen by touch or via a pointing device. 
*Type:* [TYPE_VIEW_HOVER_ENTER](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_HOVER_ENTER:kotlin.Int) 
*Properties:* 

- [getEventType()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getEventType())- The type of the event.
- [getSource()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getSource())- The source info (for registered clients).
- [getClassName()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getClassName())- The class name of the source.
- [getPackageName()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getPackageName())- The package name of the source.
- [getEventTime()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getEventTime())- The event time.

<br />

**View hover exit** - represents the event of stopping to hover over a [android.view.View](https://developer.android.com/reference/kotlin/android/view/View.html#). The hover may be generated via exploring the screen by touch or via a pointing device. 
*Type:* [TYPE_VIEW_HOVER_EXIT](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_HOVER_EXIT:kotlin.Int) 
*Properties:* 

- [getEventType()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getEventType())- The type of the event.
- [getSource()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getSource())- The source info (for registered clients).
- [getClassName()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getClassName())- The class name of the source.
- [getPackageName()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getPackageName())- The package name of the source.
- [getEventTime()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getEventTime())- The event time.

<br />

**View scrolled to** - represents the event of a target node brought on screen by ACTION_SCROLL_IN_DIRECTION.*Type:* [TYPE_VIEW_TARGETED_BY_SCROLL](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_TARGETED_BY_SCROLL:kotlin.Int) 
*Properties:* 

- [getEventType()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getEventType())- The type of the event.
- [getSource()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getSource())- The source info (for registered clients). This represents the node that is brought on screen as a result of the scroll.
- [getClassName()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getClassName())- The class name of the source.
- [getPackageName()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getPackageName())- The package name of the source.
- [getEventTime()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getEventTime())- The event time.

<br />

**Touch interaction start** - represents the event of starting a touch interaction, which is the user starts touching the screen. 
*Type:* [TYPE_TOUCH_INTERACTION_START](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_TOUCH_INTERACTION_START:kotlin.Int) 
*Properties:* 

- [getEventType()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getEventType())- The type of the event.

*Note:* This event is fired only by the system and is not passed to the view tree to be populated. 

<br />

**Touch interaction end** - represents the event of ending a touch interaction, which is the user stops touching the screen. 
*Type:* [TYPE_TOUCH_INTERACTION_END](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_TOUCH_INTERACTION_END:kotlin.Int) 
*Properties:* 

- [getEventType()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getEventType())- The type of the event.

*Note:* This event is fired only by the system and is not passed to the view tree to be populated. 

<br />

**Touch exploration gesture start** - represents the event of starting a touch exploring gesture. 
*Type:* [TYPE_TOUCH_EXPLORATION_GESTURE_START](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_TOUCH_EXPLORATION_GESTURE_START:kotlin.Int) 
*Properties:* 

- [getEventType()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getEventType())- The type of the event.

*Note:* This event is fired only by the system and is not passed to the view tree to be populated. 

<br />

**Touch exploration gesture end** - represents the event of ending a touch exploring gesture. 
*Type:* [TYPE_TOUCH_EXPLORATION_GESTURE_END](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_TOUCH_EXPLORATION_GESTURE_END:kotlin.Int) 
*Properties:* 

- [getEventType()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getEventType())- The type of the event.

*Note:* This event is fired only by the system and is not passed to the view tree to be populated. 

<br />

**Touch gesture detection start** - represents the event of starting a user gesture detection. 
*Type:* [TYPE_GESTURE_DETECTION_START](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_GESTURE_DETECTION_START:kotlin.Int) 
*Properties:* 

- [getEventType()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getEventType())- The type of the event.

*Note:* This event is fired only by the system and is not passed to the view tree to be populated. 

<br />

**Touch gesture detection end** - represents the event of ending a user gesture detection. 
*Type:* [TYPE_GESTURE_DETECTION_END](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_GESTURE_DETECTION_END:kotlin.Int) 
*Properties:* 

- [getEventType()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getEventType())- The type of the event.

*Note:* This event is fired only by the system and is not passed to the view tree to be populated. 

<br />

**MISCELLANEOUS TYPES** 

**Announcement** - represents the event of an application requesting a screen reader to make an announcement. Because the event carries no semantic meaning, this event is appropriate only in exceptional situations where additional screen reader output is needed but other types of accessibility services do not need to be aware of the change. 
*Type:* [TYPE_ANNOUNCEMENT](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_ANNOUNCEMENT:kotlin.Int) 
*Properties:* 

- [getEventType()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getEventType())- The type of the event.
- [getSource()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getSource())- The source info (for registered clients).
- [getClassName()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getClassName())- The class name of the source.
- [getPackageName()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getPackageName())- The package name of the source.
- [getEventTime()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getEventTime())- The event time.
- [getText()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getText())- The text of the announcement.

<br />

**speechStateChanged** *Type:* [TYPE_SPEECH_STATE_CHANGE](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_SPEECH_STATE_CHANGE:kotlin.Int) 
Represents a change in the speech state defined by the bit mask of the speech state change types. A change in the speech state occurs when an application wants to signal that it is either speaking or listening for human speech. This event helps avoid conflicts where two applications want to speak or one listens when another speaks. When sending this event, the sender should ensure that the accompanying state change types make sense. For example, the sender should not send [SPEECH_STATE_SPEAKING_START](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#SPEECH_STATE_SPEAKING_START:kotlin.Int) and [SPEECH_STATE_SPEAKING_END](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#SPEECH_STATE_SPEAKING_END:kotlin.Int) together.*Properties:* 

- [getSpeechStateChangeTypes()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getSpeechStateChangeTypes())- The type of state changes
- [getPackageName()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getPackageName())- The package name of the source.
- [getEventTime()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getEventTime())- The event time.

<br />

## Summary

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_CHANGE_TYPE_CHECKED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_CHECKED:kotlin.Int) Change type for [TYPE_WINDOW_CONTENT_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOW_CONTENT_CHANGED:kotlin.Int) event: The source node changed its checked state, which is returned by [AccessibilityNodeInfo.getChecked()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getChecked()). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_CHANGE_TYPE_CONTENT_DESCRIPTION](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_CONTENT_DESCRIPTION:kotlin.Int) Change type for [TYPE_WINDOW_CONTENT_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOW_CONTENT_CHANGED:kotlin.Int) event: The node's content description changed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_CHANGE_TYPE_CONTENT_INVALID](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_CONTENT_INVALID:kotlin.Int) Change type for [TYPE_WINDOW_CONTENT_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOW_CONTENT_CHANGED:kotlin.Int) event: The source node changed its content validity returned by [AccessibilityNodeInfo.isContentInvalid](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#isContentInvalid()). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_CHANGE_TYPE_DRAG_CANCELLED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_DRAG_CANCELLED:kotlin.Int) Change type for [TYPE_WINDOW_CONTENT_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOW_CONTENT_CHANGED:kotlin.Int) event: A drag in with accessibility enabled has ended. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_CHANGE_TYPE_DRAG_DROPPED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_DRAG_DROPPED:kotlin.Int) Change type for [TYPE_WINDOW_CONTENT_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOW_CONTENT_CHANGED:kotlin.Int) event: A drag in with accessibility enabled has ended. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_CHANGE_TYPE_DRAG_STARTED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_DRAG_STARTED:kotlin.Int) Change type for [TYPE_WINDOW_CONTENT_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOW_CONTENT_CHANGED:kotlin.Int) event: A drag has started while accessibility is enabled. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_CHANGE_TYPE_ENABLED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_ENABLED:kotlin.Int) Change type for [TYPE_WINDOW_CONTENT_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOW_CONTENT_CHANGED:kotlin.Int) event: The source node changed its ability to interact returned by [AccessibilityNodeInfo.isEnabled](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#isEnabled()). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_CHANGE_TYPE_ERROR](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_ERROR:kotlin.Int) Change type for [TYPE_WINDOW_CONTENT_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOW_CONTENT_CHANGED:kotlin.Int) event: The source node changed its erroneous content's error message returned by [AccessibilityNodeInfo.getError](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getError()). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_CHANGE_TYPE_EXPANDED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_EXPANDED:kotlin.Int) Change type for [TYPE_WINDOW_CONTENT_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOW_CONTENT_CHANGED:kotlin.Int) event: The source node changed its expanded state which is returned by [AccessibilityNodeInfo.getExpandedState()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getExpandedState()). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_CHANGE_TYPE_PANE_APPEARED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_PANE_APPEARED:kotlin.Int) Change type for [TYPE_WINDOW_STATE_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOW_STATE_CHANGED:kotlin.Int) event: The node has a pane title, and either just appeared or just was assigned a title when it had none before. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_CHANGE_TYPE_PANE_DISAPPEARED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_PANE_DISAPPEARED:kotlin.Int) Change type for [TYPE_WINDOW_STATE_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOW_STATE_CHANGED:kotlin.Int) event: Can mean one of two slightly different things. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_CHANGE_TYPE_PANE_TITLE](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_PANE_TITLE:kotlin.Int) Change type for [TYPE_WINDOW_STATE_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOW_STATE_CHANGED:kotlin.Int) event: The node's pane title changed. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_CHANGE_TYPE_SORT_DIRECTION](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_SORT_DIRECTION:kotlin.Int) Change type for [TYPE_WINDOW_CONTENT_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOW_CONTENT_CHANGED:kotlin.Int) event: The source node's collection item info changed its sort direction state for the data corresponding to this collection item, which is returned by [AccessibilityNodeInfo.CollectionItemInfo.getSortDirection()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.CollectionItemInfo#getSortDirection()). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_CHANGE_TYPE_STATE_DESCRIPTION](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_STATE_DESCRIPTION:kotlin.Int) Change type for [TYPE_WINDOW_CONTENT_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOW_CONTENT_CHANGED:kotlin.Int) event: state description of the node as returned by [AccessibilityNodeInfo.getStateDescription](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getStateDescription())changed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_CHANGE_TYPE_SUBTREE](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_SUBTREE:kotlin.Int) Change type for [TYPE_WINDOW_CONTENT_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOW_CONTENT_CHANGED:kotlin.Int) event: One or more content changes occurred in the the subtree rooted at the source node, or the subtree's structure changed when a node was added or removed. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_CHANGE_TYPE_SUPPLEMENTAL_DESCRIPTION](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_SUPPLEMENTAL_DESCRIPTION:kotlin.Int) Change type for [TYPE_WINDOW_CONTENT_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOW_CONTENT_CHANGED:kotlin.Int) event: The source node changed its supplemental description, which is returned by [AccessibilityNodeInfo.getSupplementalDescription()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getSupplementalDescription()). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_CHANGE_TYPE_TEXT](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_TEXT:kotlin.Int) Change type for [TYPE_WINDOW_CONTENT_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOW_CONTENT_CHANGED:kotlin.Int) event: The node's text changed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_CHANGE_TYPE_UNDEFINED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_UNDEFINED:kotlin.Int) Change type for [TYPE_WINDOW_CONTENT_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOW_CONTENT_CHANGED:kotlin.Int) event: The type of change is not defined. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INVALID_POSITION](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#INVALID_POSITION:kotlin.Int) Invalid selection/focus position. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MAX_TEXT_LENGTH](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#MAX_TEXT_LENGTH:kotlin.Int) Maximum length of the text fields. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SPEECH_STATE_LISTENING_END](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#SPEECH_STATE_LISTENING_END:kotlin.Int) Change type for [TYPE_SPEECH_STATE_CHANGE](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_SPEECH_STATE_CHANGE:kotlin.Int) event: another service is no longer listening to the microphone. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SPEECH_STATE_LISTENING_START](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#SPEECH_STATE_LISTENING_START:kotlin.Int) Change type for [TYPE_SPEECH_STATE_CHANGE](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_SPEECH_STATE_CHANGE:kotlin.Int) event: another service is listening to the microphone. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SPEECH_STATE_SPEAKING_END](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#SPEECH_STATE_SPEAKING_END:kotlin.Int) Change type for [TYPE_SPEECH_STATE_CHANGE](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_SPEECH_STATE_CHANGE:kotlin.Int) event: another service is no longer speaking. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SPEECH_STATE_SPEAKING_START](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#SPEECH_STATE_SPEAKING_START:kotlin.Int) Change type for [TYPE_SPEECH_STATE_CHANGE](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_SPEECH_STATE_CHANGE:kotlin.Int) event: another service is speaking. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPES_ALL_MASK](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPES_ALL_MASK:kotlin.Int) Mask for [AccessibilityEvent](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#) all types. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_ANNOUNCEMENT](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_ANNOUNCEMENT:kotlin.Int) Represents the event of an application making an announcement. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_ASSIST_READING_CONTEXT](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_ASSIST_READING_CONTEXT:kotlin.Int) Represents the event of the assistant currently reading the users screen context. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_GESTURE_DETECTION_END](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_GESTURE_DETECTION_END:kotlin.Int) Represents the event of ending gesture detection. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_GESTURE_DETECTION_START](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_GESTURE_DETECTION_START:kotlin.Int) Represents the event of beginning gesture detection. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_NOTIFICATION_STATE_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_NOTIFICATION_STATE_CHANGED:kotlin.Int) Represents the event showing a [android.app.Notification](https://developer.android.com/reference/kotlin/android/app/Notification.html#). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_SPEECH_STATE_CHANGE](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_SPEECH_STATE_CHANGE:kotlin.Int) Represents a change in the speech state defined by the speech state change types. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TOUCH_EXPLORATION_GESTURE_END](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_TOUCH_EXPLORATION_GESTURE_END:kotlin.Int) Represents the event of ending a touch exploration gesture. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TOUCH_EXPLORATION_GESTURE_START](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_TOUCH_EXPLORATION_GESTURE_START:kotlin.Int) Represents the event of starting a touch exploration gesture. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TOUCH_INTERACTION_END](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_TOUCH_INTERACTION_END:kotlin.Int) Represents the event of the user ending to touch the screen. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TOUCH_INTERACTION_START](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_TOUCH_INTERACTION_START:kotlin.Int) Represents the event of the user starting to touch the screen. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_VIEW_ACCESSIBILITY_FOCUSED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_ACCESSIBILITY_FOCUSED:kotlin.Int) Represents the event of gaining accessibility focus. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_VIEW_ACCESSIBILITY_FOCUS_CLEARED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_ACCESSIBILITY_FOCUS_CLEARED:kotlin.Int) Represents the event of clearing accessibility focus. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_VIEW_CLICKED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_CLICKED:kotlin.Int) Represents the event of clicking on a [android.view.View](https://developer.android.com/reference/kotlin/android/view/View.html#) like [android.widget.Button](https://developer.android.com/reference/kotlin/android/widget/Button.html#), [android.widget.CompoundButton](https://developer.android.com/reference/kotlin/android/widget/CompoundButton.html#), etc. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_VIEW_CONTEXT_CLICKED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_CONTEXT_CLICKED:kotlin.Int) Represents the event of a context click on a [android.view.View](https://developer.android.com/reference/kotlin/android/view/View.html#). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_VIEW_FOCUSED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_FOCUSED:kotlin.Int) Represents the event of setting input focus of a [android.view.View](https://developer.android.com/reference/kotlin/android/view/View.html#). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_VIEW_HOVER_ENTER](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_HOVER_ENTER:kotlin.Int) Represents the event of a hover enter over a [android.view.View](https://developer.android.com/reference/kotlin/android/view/View.html#). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_VIEW_HOVER_EXIT](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_HOVER_EXIT:kotlin.Int) Represents the event of a hover exit over a [android.view.View](https://developer.android.com/reference/kotlin/android/view/View.html#). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_VIEW_LONG_CLICKED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_LONG_CLICKED:kotlin.Int) Represents the event of long clicking on a [android.view.View](https://developer.android.com/reference/kotlin/android/view/View.html#) like [android.widget.Button](https://developer.android.com/reference/kotlin/android/widget/Button.html#), [android.widget.CompoundButton](https://developer.android.com/reference/kotlin/android/widget/CompoundButton.html#), etc. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_VIEW_SCROLLED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_SCROLLED:kotlin.Int) Represents the event of scrolling a view. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_VIEW_SELECTED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_SELECTED:kotlin.Int) Represents the event of selecting an item usually in the context of an [android.widget.AdapterView](https://developer.android.com/reference/kotlin/android/widget/AdapterView.html#). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_VIEW_TARGETED_BY_SCROLL](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_TARGETED_BY_SCROLL:kotlin.Int) Represents the event of a scroll having completed and brought the target node on screen. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_VIEW_TEXT_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_TEXT_CHANGED:kotlin.Int) Represents the event of changing the text of an [android.widget.EditText](https://developer.android.com/reference/kotlin/android/widget/EditText.html#). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_VIEW_TEXT_SELECTION_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_TEXT_SELECTION_CHANGED:kotlin.Int) Represents the event of changing the selection in an [android.widget.EditText](https://developer.android.com/reference/kotlin/android/widget/EditText.html#). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_VIEW_TEXT_TRAVERSED_AT_MOVEMENT_GRANULARITY](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_TEXT_TRAVERSED_AT_MOVEMENT_GRANULARITY:kotlin.Int) Represents the event of traversing the text of a view at a given movement granularity. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_WINDOWS_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOWS_CHANGED:kotlin.Int) Represents the event change in the system windows shown on the screen. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_WINDOW_CONTENT_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOW_CONTENT_CHANGED:kotlin.Int) Represents the event of changing the content of a window and more specifically the sub-tree rooted at the event's source. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_WINDOW_STATE_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOW_STATE_CHANGED:kotlin.Int) Represents the event of a change to a visually distinct section of the user interface. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WINDOWS_CHANGE_ACCESSIBILITY_FOCUSED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#WINDOWS_CHANGE_ACCESSIBILITY_FOCUSED:kotlin.Int) Change type for [TYPE_WINDOWS_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOWS_CHANGED:kotlin.Int) event: The window's [AccessibilityWindowInfo.isAccessibilityFocused()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#isAccessibilityFocused())changed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WINDOWS_CHANGE_ACTIVE](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#WINDOWS_CHANGE_ACTIVE:kotlin.Int) Change type for [TYPE_WINDOWS_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOWS_CHANGED:kotlin.Int) event: The window's [AccessibilityWindowInfo.isActive()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#isActive())changed. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WINDOWS_CHANGE_ADDED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#WINDOWS_CHANGE_ADDED:kotlin.Int) Change type for [TYPE_WINDOWS_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOWS_CHANGED:kotlin.Int) event: The window was added. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WINDOWS_CHANGE_BOUNDS](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#WINDOWS_CHANGE_BOUNDS:kotlin.Int) Change type for [TYPE_WINDOWS_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOWS_CHANGED:kotlin.Int) event: The window's bounds changed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WINDOWS_CHANGE_CHILDREN](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#WINDOWS_CHANGE_CHILDREN:kotlin.Int) Change type for [TYPE_WINDOWS_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOWS_CHANGED:kotlin.Int) event: The window's children changed. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WINDOWS_CHANGE_FOCUSED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#WINDOWS_CHANGE_FOCUSED:kotlin.Int) Change type for [TYPE_WINDOWS_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOWS_CHANGED:kotlin.Int) event: The window's [AccessibilityWindowInfo.isFocused()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#isFocused())changed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WINDOWS_CHANGE_LAYER](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#WINDOWS_CHANGE_LAYER:kotlin.Int) Change type for [TYPE_WINDOWS_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOWS_CHANGED:kotlin.Int) event: The window's layer changed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WINDOWS_CHANGE_PARENT](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#WINDOWS_CHANGE_PARENT:kotlin.Int) Change type for [TYPE_WINDOWS_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOWS_CHANGED:kotlin.Int) event: The window's parent changed. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WINDOWS_CHANGE_PIP](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#WINDOWS_CHANGE_PIP:kotlin.Int) Change type for [TYPE_WINDOWS_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOWS_CHANGED:kotlin.Int) event: The window either entered or exited picture-in-picture mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WINDOWS_CHANGE_REMOVED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#WINDOWS_CHANGE_REMOVED:kotlin.Int) Change type for [TYPE_WINDOWS_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOWS_CHANGED:kotlin.Int) event: A window was removed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WINDOWS_CHANGE_TITLE](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#WINDOWS_CHANGE_TITLE:kotlin.Int) Change type for [TYPE_WINDOWS_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOWS_CHANGED:kotlin.Int) event: The window's title changed. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AccessibilityEvent](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#AccessibilityEvent())`()` Creates a new [AccessibilityEvent](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#). |
| [AccessibilityEvent](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#AccessibilityEvent(android.view.accessibility.AccessibilityEvent))`(`event:` ` [AccessibilityEvent](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#)`)` Copy constructor. |
| [AccessibilityEvent](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#AccessibilityEvent(kotlin.Int))`(`eventType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a new [AccessibilityEvent](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#) with the given`eventType`. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [appendRecord](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#appendRecord(android.view.accessibility.AccessibilityRecord))`(`record:` ` [AccessibilityRecord](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord)!`)` Appends an [AccessibilityRecord](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord) to the end of event records. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#describeContents())`()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [eventTypeToString](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#eventTypeToString(kotlin.Int))`(`eventType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the string representation of an event type. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAction](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getAction())`()` Gets the performed action that triggered this event. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getContentChangeTypes](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getContentChangeTypes())`()` Gets the bit mask of change types signaled by a [TYPE_WINDOW_CONTENT_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOW_CONTENT_CHANGED:kotlin.Int) event or [TYPE_WINDOW_STATE_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOW_STATE_CHANGED:kotlin.Int). |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getEventTime](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getEventTime())`()` Gets the time in which this event was sent. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getEventType](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getEventType())`()` Gets the event type. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMovementGranularity](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getMovementGranularity())`()` Gets the movement granularity that was traversed. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [getPackageName](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getPackageName())`()` Gets the package name of the source. |
| --- | --- |
| [AccessibilityRecord](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord)! | [getRecord](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getRecord(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Gets the record at a given index. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRecordCount](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getRecordCount())`()` Gets the number of records contained in the event. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSpeechStateChangeTypes](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getSpeechStateChangeTypes())`()` Gets the bit mask of the speech state signaled by a [TYPE_SPEECH_STATE_CHANGE](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_SPEECH_STATE_CHANGE:kotlin.Int) event. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getWindowChanges](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getWindowChanges())`()` Get the bit mask of change types signaled by a [TYPE_WINDOWS_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOWS_CHANGED:kotlin.Int) event. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [initFromParcel](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#initFromParcel(android.os.Parcel))`(`parcel:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)!`)` Creates a new instance from a [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#). |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAccessibilityDataSensitive](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#isAccessibilityDataSensitive())`()` Whether the event should only be delivered to an [android.accessibilityservice.AccessibilityService](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#) with the [android.accessibilityservice.AccessibilityServiceInfo#isAccessibilityTool](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo.html#isAccessibilityTool())property set to true. |
| --- | --- |
| static [AccessibilityEvent](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#)! | [obtain](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#obtain())`()` Instantiates a new AccessibilityEvent instance. |
| static [AccessibilityEvent](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#)! | [obtain](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#obtain(android.view.accessibility.AccessibilityEvent))`(`event:` ` [AccessibilityEvent](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#)!`)` Instantiates a new AccessibilityEvent instance. |
| static [AccessibilityEvent](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#)! | [obtain](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#obtain(kotlin.Int))`(`eventType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Instantiates a new AccessibilityEvent instance with its type property set. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [recycle](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#recycle())`()` Previously would recycle an instance back to be reused. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAccessibilityDataSensitive](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#setAccessibilityDataSensitive(kotlin.Boolean))`(`accessibilityDataSensitive:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether the event should only be delivered to an [android.accessibilityservice.AccessibilityService](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#) with the [android.accessibilityservice.AccessibilityServiceInfo#isAccessibilityTool](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo.html#isAccessibilityTool())property set to true. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAction](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#setAction(kotlin.Int))`(`action:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the performed action that triggered this event. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setContentChangeTypes](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#setContentChangeTypes(kotlin.Int))`(`changeTypes:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the bit mask of node tree changes signaled by an [TYPE_WINDOW_CONTENT_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOW_CONTENT_CHANGED:kotlin.Int) event. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEventTime](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#setEventTime(kotlin.Long))`(`eventTime:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the time in which this event was sent. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEventType](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#setEventType(kotlin.Int))`(`eventType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the event type. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMovementGranularity](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#setMovementGranularity(kotlin.Int))`(`granularity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the movement granularity that was traversed. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPackageName](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#setPackageName(kotlin.CharSequence))`(`packageName:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Sets the package name of the source. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSpeechStateChangeTypes](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#setSpeechStateChangeTypes(kotlin.Int))`(`state:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the bit mask of the speech state change types signaled by a [TYPE_SPEECH_STATE_CHANGE](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_SPEECH_STATE_CHANGE:kotlin.Int) event. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`parcel:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Inherited functions ||
|---|---|
| From class [AccessibilityRecord](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord) |---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAddedCount](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getAddedCount())`()` <br /> Gets the number of added characters. <br /> | | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getBeforeText](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getBeforeText())`()` <br /> Gets the text before a change. <br /> | | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getClassName](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getClassName())`()` <br /> Gets the class name of the source. <br /> | | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getContentDescription](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getContentDescription())`()` <br /> Gets the description of the source. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCurrentItemIndex](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getCurrentItemIndex())`()` <br /> Gets the index of the source in the list of items the can be visited. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDisplayId](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getDisplayId())`()` <br /> Gets the id of the display from which the event comes from. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getFromIndex](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getFromIndex())`()` <br /> Gets the index of the first character of the changed sequence, or the beginning of a text selection or the index of the first visible item when scrolling. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getItemCount](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getItemCount())`()` <br /> Gets the number of items that can be visited. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxScrollX](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getMaxScrollX())`()` <br /> Gets the max scroll offset of the source left edge in pixels. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxScrollY](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getMaxScrollY())`()` <br /> Gets the max scroll offset of the source top edge in pixels. <br /> | | [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#)? | [getParcelableData](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getParcelableData())`()` <br /> Gets the [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) data. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRemovedCount](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getRemovedCount())`()` <br /> Gets the number of removed characters. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getScrollDeltaX](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getScrollDeltaX())`()` <br /> Gets the difference in pixels between the horizontal position before the scroll and the current horizontal position <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getScrollDeltaY](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getScrollDeltaY())`()` <br /> Gets the difference in pixels between the vertical position before the scroll and the current vertical position <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getScrollX](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getScrollX())`()` <br /> Gets the scroll offset of the source left edge in pixels. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getScrollY](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getScrollY())`()` <br /> Gets the scroll offset of the source top edge in pixels. <br /> | | [AccessibilityNodeInfo](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo)? | [getSource](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getSource())`()` <br /> Gets the [AccessibilityNodeInfo](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo) of the event source. **Note:** It is a client responsibility to recycle the received info by calling [AccessibilityNodeInfo#recycle()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#recycle())to avoid creating of multiple instances. <br /> | | [AccessibilityNodeInfo](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo)? | [getSource](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getSource(kotlin.Int))`(`prefetchingStrategy:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Gets the [AccessibilityNodeInfo](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo) of the event source. <br /> | | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!> | [getText](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getText())`()` <br /> Gets the text of the event. The index in the list represents the priority of the text. Specifically, the lower the index the higher the priority. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getToIndex](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getToIndex())`()` <br /> Gets the index of text selection end or the index of the last visible item when scrolling. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getWindowId](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getWindowId())`()` <br /> Gets the id of the window from which the event comes from. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isChecked](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#isChecked())`()` <br /> Gets if the source is checked. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEnabled](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#isEnabled())`()` <br /> Gets if the source is enabled. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isFullScreen](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#isFullScreen())`()` <br /> Gets if the source is taking the entire screen. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPassword](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#isPassword())`()` <br /> Gets if the source is a password field. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isScrollable](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#isScrollable())`()` <br /> Gets if the source is scrollable. <br /> | | [AccessibilityRecord](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord) | [obtain](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#obtain(android.view.accessibility.AccessibilityRecord))`(`record:` ` [AccessibilityRecord](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord)`)` <br /> Instantiates a new record initialized with data from the given record. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAddedCount](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#setAddedCount(kotlin.Int))`(`addedCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the number of added characters. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBeforeText](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#setBeforeText(kotlin.CharSequence))`(`beforeText:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?`)` <br /> Sets the text before a change. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setChecked](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#setChecked(kotlin.Boolean))`(`isChecked:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Sets if the source is checked. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setClassName](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#setClassName(kotlin.CharSequence))`(`className:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?`)` <br /> Sets the class name of the source. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setContentDescription](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#setContentDescription(kotlin.CharSequence))`(`contentDescription:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?`)` <br /> Sets the description of the source. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCurrentItemIndex](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#setCurrentItemIndex(kotlin.Int))`(`currentItemIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the index of the source in the list of items that can be visited. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEnabled](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#setEnabled(kotlin.Boolean))`(`isEnabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Sets if the source is enabled. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFromIndex](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#setFromIndex(kotlin.Int))`(`fromIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the index of the first character of the changed sequence or the beginning of a text selection or the index of the first visible item when scrolling. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFullScreen](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#setFullScreen(kotlin.Boolean))`(`isFullScreen:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Sets if the source is taking the entire screen. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setItemCount](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#setItemCount(kotlin.Int))`(`itemCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the number of items that can be visited. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMaxScrollX](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#setMaxScrollX(kotlin.Int))`(`maxScrollX:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the max scroll offset of the source left edge in pixels. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMaxScrollY](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#setMaxScrollY(kotlin.Int))`(`maxScrollY:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the max scroll offset of the source top edge in pixels. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setParcelableData](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#setParcelableData(android.os.Parcelable))`(`parcelableData:` ` [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#)?`)` <br /> Sets the [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) data of the event. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPassword](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#setPassword(kotlin.Boolean))`(`isPassword:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Sets if the source is a password field. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRemovedCount](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#setRemovedCount(kotlin.Int))`(`removedCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the number of removed characters. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setScrollDeltaX](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#setScrollDeltaX(kotlin.Int))`(`scrollDeltaX:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the difference in pixels between the horizontal position before the scroll and the current horizontal position <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setScrollDeltaY](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#setScrollDeltaY(kotlin.Int))`(`scrollDeltaY:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the difference in pixels between the vertical position before the scroll and the current vertical position <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setScrollX](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#setScrollX(kotlin.Int))`(`scrollX:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the scroll offset of the source left edge in pixels. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setScrollY](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#setScrollY(kotlin.Int))`(`scrollY:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the scroll offset of the source top edge in pixels. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setScrollable](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#setScrollable(kotlin.Boolean))`(`scrollable:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Sets if the source is scrollable. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSource](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#setSource(android.view.View))`(`source:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)?`)` <br /> Sets the event source. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSource](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#setSource(android.view.View,%20kotlin.Int))`(`root:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)?`, `virtualDescendantId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the source to be a virtual descendant of the given`root`. If`virtualDescendantId`equals to [View.NO_ID](https://developer.android.com/reference/kotlin/android/view/View.html#NO_ID:kotlin.Int) the root is set as the source. A virtual descendant is an imaginary View that is reported as a part of the view hierarchy for accessibility purposes. This enables custom views that draw complex content to report them selves as a tree of virtual views, thus conveying their logical structure. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setToIndex](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#setToIndex(kotlin.Int))`(`toIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the index of text selection end or the index of the last visible item when scrolling. <br /> | ||

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [AccessibilityEvent](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### CONTENT_CHANGE_TYPE_CHECKED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTENT_CHANGE_TYPE_CHECKED: Int
```

Change type for [TYPE_WINDOW_CONTENT_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOW_CONTENT_CHANGED:kotlin.Int) event: The source node changed its checked state, which is returned by [AccessibilityNodeInfo.getChecked()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getChecked()). The view changing its checked state should call [AccessibilityNodeInfo.setChecked(int)](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setChecked(kotlin.Int))and then send this event. 

 Value: 8192

**See Also**

- [android.view.accessibility.AccessibilityNodeInfo#getChecked()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getChecked())
- [android.view.accessibility.AccessibilityNodeInfo#setChecked(int)](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setChecked(kotlin.Int)) 

### CONTENT_CHANGE_TYPE_CONTENT_DESCRIPTION

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTENT_CHANGE_TYPE_CONTENT_DESCRIPTION: Int
```

Change type for [TYPE_WINDOW_CONTENT_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOW_CONTENT_CHANGED:kotlin.Int) event: The node's content description changed. 

 Value: 4

### CONTENT_CHANGE_TYPE_CONTENT_INVALID

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTENT_CHANGE_TYPE_CONTENT_INVALID: Int
```

Change type for [TYPE_WINDOW_CONTENT_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOW_CONTENT_CHANGED:kotlin.Int) event: The source node changed its content validity returned by [AccessibilityNodeInfo.isContentInvalid](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#isContentInvalid()). The view changing content validity should call [AccessibilityNodeInfo.setContentInvalid](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setContentInvalid(kotlin.Boolean))and then send this event. 

 Value: 1024

**See Also**

- [android.view.accessibility.AccessibilityNodeInfo#isContentInvalid](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#isContentInvalid())
- [android.view.accessibility.AccessibilityNodeInfo#setContentInvalid](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setContentInvalid(kotlin.Boolean)) 

### CONTENT_CHANGE_TYPE_DRAG_CANCELLED

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTENT_CHANGE_TYPE_DRAG_CANCELLED: Int
```

Change type for [TYPE_WINDOW_CONTENT_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOW_CONTENT_CHANGED:kotlin.Int) event: A drag in with accessibility enabled has ended. This means the content has been unsuccessfully dropped, the user has canceled the action via an AccessibilityAction, or no drop has been detected within a timeout and the drag was automatically cancelled. This is sent from the source that initiated the drag. 

 Value: 512

**See Also**

- [android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction#ACTION_DRAG_CANCEL](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_DRAG_CANCEL:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction) 

### CONTENT_CHANGE_TYPE_DRAG_DROPPED

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTENT_CHANGE_TYPE_DRAG_DROPPED: Int
```

Change type for [TYPE_WINDOW_CONTENT_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOW_CONTENT_CHANGED:kotlin.Int) event: A drag in with accessibility enabled has ended. This means the content has been successfully dropped. This is sent from the target that accepted the dragged content. 

 Value: 256

**See Also**

- [android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction#ACTION_DRAG_DROP](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_DRAG_DROP:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction) 

### CONTENT_CHANGE_TYPE_DRAG_STARTED

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTENT_CHANGE_TYPE_DRAG_STARTED: Int
```

Change type for [TYPE_WINDOW_CONTENT_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOW_CONTENT_CHANGED:kotlin.Int) event: A drag has started while accessibility is enabled. This is either via an AccessibilityAction, or via touch events. This is sent from the source that initiated the drag. 

 Value: 128

**See Also**

- [android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction#ACTION_DRAG_START](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_DRAG_START:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction) 

### CONTENT_CHANGE_TYPE_ENABLED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTENT_CHANGE_TYPE_ENABLED: Int
```

Change type for [TYPE_WINDOW_CONTENT_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOW_CONTENT_CHANGED:kotlin.Int) event: The source node changed its ability to interact returned by [AccessibilityNodeInfo.isEnabled](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#isEnabled()). The view changing content's ability to interact should call [AccessibilityNodeInfo.setEnabled](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setEnabled(kotlin.Boolean))and then send this event. 

 Value: 4096

**See Also**

- [android.view.accessibility.AccessibilityNodeInfo#isEnabled](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#isEnabled())
- [android.view.accessibility.AccessibilityNodeInfo#setEnabled](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setEnabled(kotlin.Boolean)) 

### CONTENT_CHANGE_TYPE_ERROR

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTENT_CHANGE_TYPE_ERROR: Int
```

Change type for [TYPE_WINDOW_CONTENT_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOW_CONTENT_CHANGED:kotlin.Int) event: The source node changed its erroneous content's error message returned by [AccessibilityNodeInfo.getError](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getError()). The view changing erroneous content's error message should call [AccessibilityNodeInfo.setError](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setError(kotlin.CharSequence))and then send this event. 

 Value: 2048

**See Also**

- [android.view.accessibility.AccessibilityNodeInfo#getError](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getError())
- [android.view.accessibility.AccessibilityNodeInfo#setError](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setError(kotlin.CharSequence)) 

### CONTENT_CHANGE_TYPE_EXPANDED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTENT_CHANGE_TYPE_EXPANDED: Int
```

Change type for [TYPE_WINDOW_CONTENT_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOW_CONTENT_CHANGED:kotlin.Int) event: The source node changed its expanded state which is returned by [AccessibilityNodeInfo.getExpandedState()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getExpandedState()). The view changing the node's expanded state should call [android.view.accessibility.AccessibilityNodeInfo#setExpandedState(int)](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setExpandedState(kotlin.Int))and then send this event. 

 Value: 16384

**See Also**

- [android.view.accessibility.AccessibilityNodeInfo#getExpandedState()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getExpandedState())
- [android.view.accessibility.AccessibilityNodeInfo#setExpandedState(int)](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setExpandedState(kotlin.Int)) 

### CONTENT_CHANGE_TYPE_PANE_APPEARED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTENT_CHANGE_TYPE_PANE_APPEARED: Int
```

Change type for [TYPE_WINDOW_STATE_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOW_STATE_CHANGED:kotlin.Int) event: The node has a pane title, and either just appeared or just was assigned a title when it had none before. 

 Value: 16

**See Also**

- [android.view.View#setAccessibilityPaneTitle(CharSequence)](https://developer.android.com/reference/kotlin/android/view/View.html#setAccessibilityPaneTitle(kotlin.CharSequence)) 

### CONTENT_CHANGE_TYPE_PANE_DISAPPEARED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTENT_CHANGE_TYPE_PANE_DISAPPEARED: Int
```

Change type for [TYPE_WINDOW_STATE_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOW_STATE_CHANGED:kotlin.Int) event: Can mean one of two slightly different things. The primary meaning is that the node has a pane title, and was removed from the node hierarchy. It will also be sent if the pane title is set to`null`after it contained a title. No source will be returned if the node is no longer on the screen. To make the change more clear for the user, the first entry in [getText()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getText())will return the value that would have been returned by`getSource().getPaneTitle()`. 

 Value: 32

**See Also**

- [android.view.View#setAccessibilityPaneTitle(CharSequence)](https://developer.android.com/reference/kotlin/android/view/View.html#setAccessibilityPaneTitle(kotlin.CharSequence)) 

### CONTENT_CHANGE_TYPE_PANE_TITLE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTENT_CHANGE_TYPE_PANE_TITLE: Int
```

Change type for [TYPE_WINDOW_STATE_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOW_STATE_CHANGED:kotlin.Int) event: The node's pane title changed.

If this makes the pane appear, [CONTENT_CHANGE_TYPE_PANE_APPEARED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_PANE_APPEARED:kotlin.Int) is sent instead. If this makes the pane disappear, [CONTENT_CHANGE_TYPE_PANE_DISAPPEARED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_PANE_DISAPPEARED:kotlin.Int) is sent. 

 Value: 8

**See Also**

- [android.view.View#setAccessibilityPaneTitle(CharSequence)](https://developer.android.com/reference/kotlin/android/view/View.html#setAccessibilityPaneTitle(kotlin.CharSequence)) 

### CONTENT_CHANGE_TYPE_SORT_DIRECTION

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTENT_CHANGE_TYPE_SORT_DIRECTION: Int
```

Change type for [TYPE_WINDOW_CONTENT_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOW_CONTENT_CHANGED:kotlin.Int) event: The source node's collection item info changed its sort direction state for the data corresponding to this collection item, which is returned by [AccessibilityNodeInfo.CollectionItemInfo.getSortDirection()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.CollectionItemInfo#getSortDirection()). The view changing its collection item info's sort direction should set a [AccessibilityNodeInfo.CollectionItemInfo](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.CollectionItemInfo) created with [AccessibilityNodeInfo.CollectionItemInfo.Builder.setSortDirection(int)](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.CollectionItemInfo.Builder#setSortDirection(kotlin.Int))and then send this event. 

 Value: 65536

**See Also**

- [android.view.accessibility.AccessibilityNodeInfo.CollectionItemInfo#getSortDirection()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.CollectionItemInfo#getSortDirection())
- [android.view.accessibility.AccessibilityNodeInfo.CollectionItemInfo.Builder#setSortDirection(int)](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.CollectionItemInfo.Builder#setSortDirection(kotlin.Int)) 

### CONTENT_CHANGE_TYPE_STATE_DESCRIPTION

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTENT_CHANGE_TYPE_STATE_DESCRIPTION: Int
```

Change type for [TYPE_WINDOW_CONTENT_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOW_CONTENT_CHANGED:kotlin.Int) event: state description of the node as returned by [AccessibilityNodeInfo.getStateDescription](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getStateDescription())changed. If part of the state description changes, the changed part can be put into event text. For example, if state description changed from "on, wifi signal full" to "on, wifi three bars", "wifi three bars" can be put into the event text. 

 Value: 64

**See Also**

- [android.view.View#setStateDescription(CharSequence)](https://developer.android.com/reference/kotlin/android/view/View.html#setStateDescription(kotlin.CharSequence)) 

### CONTENT_CHANGE_TYPE_SUBTREE

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTENT_CHANGE_TYPE_SUBTREE: Int
```

Change type for [TYPE_WINDOW_CONTENT_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOW_CONTENT_CHANGED:kotlin.Int) event: One or more content changes occurred in the the subtree rooted at the source node, or the subtree's structure changed when a node was added or removed. 

 Value: 1

### CONTENT_CHANGE_TYPE_SUPPLEMENTAL_DESCRIPTION

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTENT_CHANGE_TYPE_SUPPLEMENTAL_DESCRIPTION: Int
```

Change type for [TYPE_WINDOW_CONTENT_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOW_CONTENT_CHANGED:kotlin.Int) event: The source node changed its supplemental description, which is returned by [AccessibilityNodeInfo.getSupplementalDescription()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getSupplementalDescription()). The view changing its supplemental description should call [AccessibilityNodeInfo.setSupplementalDescription(CharSequence)](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setSupplementalDescription(kotlin.CharSequence))and then send this event. 

 Value: 32768

**See Also**

- [android.view.accessibility.AccessibilityNodeInfo#getSupplementalDescription()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#getSupplementalDescription())
- [android.view.accessibility.AccessibilityNodeInfo#setSupplementalDescription(CharSequence)](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setSupplementalDescription(kotlin.CharSequence)) 

### CONTENT_CHANGE_TYPE_TEXT

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTENT_CHANGE_TYPE_TEXT: Int
```

Change type for [TYPE_WINDOW_CONTENT_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOW_CONTENT_CHANGED:kotlin.Int) event: The node's text changed. 

 Value: 2

**See Also**

- [android.view.accessibility.AccessibilityNodeInfo#setText(CharSequence)](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setText(kotlin.CharSequence)) 

### CONTENT_CHANGE_TYPE_UNDEFINED

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTENT_CHANGE_TYPE_UNDEFINED: Int
```

Change type for [TYPE_WINDOW_CONTENT_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOW_CONTENT_CHANGED:kotlin.Int) event: The type of change is not defined. 

 Value: 0

### INVALID_POSITION

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INVALID_POSITION: Int
```

Invalid selection/focus position. 

 Value: -1

**See Also**

- [#getCurrentItemIndex()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getCurrentItemIndex()) 

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

- [#getBeforeText()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getBeforeText())
- [#getText()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#getText()) 

### SPEECH_STATE_LISTENING_END

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SPEECH_STATE_LISTENING_END: Int
```

Change type for [TYPE_SPEECH_STATE_CHANGE](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_SPEECH_STATE_CHANGE:kotlin.Int) event: another service is no longer listening to the microphone. 

 Value: 8

### SPEECH_STATE_LISTENING_START

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SPEECH_STATE_LISTENING_START: Int
```

Change type for [TYPE_SPEECH_STATE_CHANGE](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_SPEECH_STATE_CHANGE:kotlin.Int) event: another service is listening to the microphone. 

 Value: 4

### SPEECH_STATE_SPEAKING_END

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SPEECH_STATE_SPEAKING_END: Int
```

Change type for [TYPE_SPEECH_STATE_CHANGE](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_SPEECH_STATE_CHANGE:kotlin.Int) event: another service is no longer speaking. 

 Value: 2

### SPEECH_STATE_SPEAKING_START

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SPEECH_STATE_SPEAKING_START: Int
```

Change type for [TYPE_SPEECH_STATE_CHANGE](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_SPEECH_STATE_CHANGE:kotlin.Int) event: another service is speaking. 

 Value: 1

### TYPES_ALL_MASK

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPES_ALL_MASK: Int
```

Mask for [AccessibilityEvent](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#) all types. 

 Value: -1

**See Also**

- [#TYPE_VIEW_CLICKED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_CLICKED:kotlin.Int)
- [#TYPE_VIEW_LONG_CLICKED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_LONG_CLICKED:kotlin.Int)
- [#TYPE_VIEW_SELECTED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_SELECTED:kotlin.Int)
- [#TYPE_VIEW_FOCUSED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_FOCUSED:kotlin.Int)
- [#TYPE_VIEW_TEXT_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_TEXT_CHANGED:kotlin.Int)
- [#TYPE_WINDOW_STATE_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOW_STATE_CHANGED:kotlin.Int)
- [#TYPE_NOTIFICATION_STATE_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_NOTIFICATION_STATE_CHANGED:kotlin.Int)
- [#TYPE_VIEW_HOVER_ENTER](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_HOVER_ENTER:kotlin.Int)
- [#TYPE_VIEW_HOVER_EXIT](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_HOVER_EXIT:kotlin.Int)
- [#TYPE_TOUCH_EXPLORATION_GESTURE_START](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_TOUCH_EXPLORATION_GESTURE_START:kotlin.Int)
- [#TYPE_TOUCH_EXPLORATION_GESTURE_END](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_TOUCH_EXPLORATION_GESTURE_END:kotlin.Int)
- [#TYPE_WINDOW_CONTENT_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOW_CONTENT_CHANGED:kotlin.Int)
- [#TYPE_VIEW_SCROLLED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_SCROLLED:kotlin.Int)
- [#TYPE_VIEW_TEXT_SELECTION_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_TEXT_SELECTION_CHANGED:kotlin.Int)
- [#TYPE_ANNOUNCEMENT](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_ANNOUNCEMENT:kotlin.Int)
- [#TYPE_VIEW_ACCESSIBILITY_FOCUSED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_ACCESSIBILITY_FOCUSED:kotlin.Int)
- [#TYPE_VIEW_ACCESSIBILITY_FOCUS_CLEARED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_ACCESSIBILITY_FOCUS_CLEARED:kotlin.Int)
- [#TYPE_VIEW_TEXT_TRAVERSED_AT_MOVEMENT_GRANULARITY](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_TEXT_TRAVERSED_AT_MOVEMENT_GRANULARITY:kotlin.Int)
- [#TYPE_GESTURE_DETECTION_START](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_GESTURE_DETECTION_START:kotlin.Int)
- [#TYPE_GESTURE_DETECTION_END](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_GESTURE_DETECTION_END:kotlin.Int)
- [#TYPE_TOUCH_INTERACTION_START](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_TOUCH_INTERACTION_START:kotlin.Int)
- [#TYPE_TOUCH_INTERACTION_END](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_TOUCH_INTERACTION_END:kotlin.Int)
- [#TYPE_WINDOWS_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOWS_CHANGED:kotlin.Int)
- [#TYPE_VIEW_CONTEXT_CLICKED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_CONTEXT_CLICKED:kotlin.Int)
- [#TYPE_ASSIST_READING_CONTEXT](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_ASSIST_READING_CONTEXT:kotlin.Int)
- [#TYPE_SPEECH_STATE_CHANGE](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_SPEECH_STATE_CHANGE:kotlin.Int)
- [#TYPE_VIEW_TARGETED_BY_SCROLL](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_TARGETED_BY_SCROLL:kotlin.Int) 

### TYPE_ANNOUNCEMENT

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_ANNOUNCEMENT: Int
```

**Deprecated:** *Use one of the semantic alternative methods described in the documentation of [View.announceForAccessibility(CharSequence)](https://developer.android.com/reference/kotlin/android/view/View.html#announceForAccessibility(kotlin.CharSequence))instead of using this event, as accessibility services may choose to ignore dispatch of this event type.*

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

Represents the event showing a [android.app.Notification](https://developer.android.com/reference/kotlin/android/app/Notification.html#). 

 Value: 64

### TYPE_SPEECH_STATE_CHANGE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_SPEECH_STATE_CHANGE: Int
```

Represents a change in the speech state defined by the speech state change types. A change in the speech state occurs when an application wants to signal that it is either speaking or listening for human speech. This event helps avoid conflicts where two applications want to speak or one listens when another speaks. When sending this event, the sender should ensure that the accompanying state change types make sense. For example, the sender should not send [SPEECH_STATE_SPEAKING_START](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#SPEECH_STATE_SPEAKING_START:kotlin.Int) and [SPEECH_STATE_SPEAKING_END](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#SPEECH_STATE_SPEAKING_END:kotlin.Int) together. 

 Value: 33554432

**See Also**

- [#SPEECH_STATE_SPEAKING_START](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#SPEECH_STATE_SPEAKING_START:kotlin.Int)
- [#SPEECH_STATE_SPEAKING_END](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#SPEECH_STATE_SPEAKING_END:kotlin.Int)
- [#SPEECH_STATE_LISTENING_START](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#SPEECH_STATE_LISTENING_START:kotlin.Int)
- [#SPEECH_STATE_LISTENING_END](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#SPEECH_STATE_LISTENING_END:kotlin.Int)
- [#getSpeechStateChangeTypes](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getSpeechStateChangeTypes())
- [#setSpeechStateChangeTypes](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#setSpeechStateChangeTypes(kotlin.Int)) 

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

- [android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction#ACTION_ACCESSIBILITY_FOCUS](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_ACCESSIBILITY_FOCUS:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction) 

### TYPE_VIEW_ACCESSIBILITY_FOCUS_CLEARED

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_VIEW_ACCESSIBILITY_FOCUS_CLEARED: Int
```

Represents the event of clearing accessibility focus. 

 Value: 65536

**See Also**

- [android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction#ACTION_ACCESSIBILITY_FOCUS](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_ACCESSIBILITY_FOCUS:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction) 

### TYPE_VIEW_CLICKED

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_VIEW_CLICKED: Int
```

Represents the event of clicking on a [android.view.View](https://developer.android.com/reference/kotlin/android/view/View.html#) like [android.widget.Button](https://developer.android.com/reference/kotlin/android/widget/Button.html#), [android.widget.CompoundButton](https://developer.android.com/reference/kotlin/android/widget/CompoundButton.html#), etc.

See [AccessibilityNodeInfo.AccessibilityAction.ACTION_CLICK](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_CLICK:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction) for more details. 

 Value: 1

### TYPE_VIEW_CONTEXT_CLICKED

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_VIEW_CONTEXT_CLICKED: Int
```

Represents the event of a context click on a [android.view.View](https://developer.android.com/reference/kotlin/android/view/View.html#).

See [AccessibilityNodeInfo.AccessibilityAction.ACTION_CONTEXT_CLICK](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_CONTEXT_CLICK:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction) for more details. 

 Value: 8388608

### TYPE_VIEW_FOCUSED

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_VIEW_FOCUSED: Int
```

Represents the event of setting input focus of a [android.view.View](https://developer.android.com/reference/kotlin/android/view/View.html#). 

 Value: 8

**See Also**

- [android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction#ACTION_ACCESSIBILITY_FOCUS](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_ACCESSIBILITY_FOCUS:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction) 

### TYPE_VIEW_HOVER_ENTER

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_VIEW_HOVER_ENTER: Int
```

Represents the event of a hover enter over a [android.view.View](https://developer.android.com/reference/kotlin/android/view/View.html#). 

 Value: 128

### TYPE_VIEW_HOVER_EXIT

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_VIEW_HOVER_EXIT: Int
```

Represents the event of a hover exit over a [android.view.View](https://developer.android.com/reference/kotlin/android/view/View.html#). 

 Value: 256

### TYPE_VIEW_LONG_CLICKED

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_VIEW_LONG_CLICKED: Int
```

Represents the event of long clicking on a [android.view.View](https://developer.android.com/reference/kotlin/android/view/View.html#) like [android.widget.Button](https://developer.android.com/reference/kotlin/android/widget/Button.html#), [android.widget.CompoundButton](https://developer.android.com/reference/kotlin/android/widget/CompoundButton.html#), etc.

See [AccessibilityNodeInfo.AccessibilityAction.ACTION_LONG_CLICK](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_LONG_CLICK:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction) for more details. 

 Value: 2

### TYPE_VIEW_SCROLLED

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_VIEW_SCROLLED: Int
```

Represents the event of scrolling a view. This event type is generally not sent directly. In the View system, this is sent in [android.view.View#onScrollChanged(int, int, int, int)](https://developer.android.com/reference/kotlin/android/view/View.html#onScrollChanged(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))

In addition to the source and package name, the event should populate scroll-specific properties like [setScrollDeltaX(int)](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#setScrollDeltaX(kotlin.Int)), [setScrollDeltaY(int)](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#setScrollDeltaY(kotlin.Int)), [setMaxScrollX(int)](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#setMaxScrollX(kotlin.Int)), and [setMaxScrollY(int)](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord#setMaxScrollY(kotlin.Int)).

Services are encouraged to rely on the source to query UI state over AccessibilityEvents properties. For example, to check after a scroll if the bottom of the scrolling UI element has been reached, check if the source node is scrollable and has the [AccessibilityNodeInfo.AccessibilityAction.ACTION_SCROLL_BACKWARD](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_SCROLL_BACKWARD:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction) action but not the [AccessibilityNodeInfo.AccessibilityAction.ACTION_SCROLL_FORWARD](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_SCROLL_FORWARD:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction) action. For scrolling to a target, use [TYPE_VIEW_TARGETED_BY_SCROLL](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_TARGETED_BY_SCROLL:kotlin.Int). 

 Value: 4096

### TYPE_VIEW_SELECTED

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_VIEW_SELECTED: Int
```

Represents the event of selecting an item usually in the context of an [android.widget.AdapterView](https://developer.android.com/reference/kotlin/android/widget/AdapterView.html#). 

 Value: 4

**See Also**

- [android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction#ACTION_SELECT](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.AccessibilityAction#ACTION_SELECT:android.view.accessibility.AccessibilityNodeInfo.AccessibilityAction) 

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

Represents the event of changing the text of an [android.widget.EditText](https://developer.android.com/reference/kotlin/android/widget/EditText.html#). 

 Value: 16

**See Also**

- [android.view.accessibility.AccessibilityNodeInfo#setText(CharSequence)](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#setText(kotlin.CharSequence)) 

### TYPE_VIEW_TEXT_SELECTION_CHANGED

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_VIEW_TEXT_SELECTION_CHANGED: Int
```

Represents the event of changing the selection in an [android.widget.EditText](https://developer.android.com/reference/kotlin/android/widget/EditText.html#). 

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

These events should only be dispatched from [android.view.View](https://developer.android.com/reference/kotlin/android/view/View.html#) s that have accessibility pane titles, and replaces [TYPE_WINDOW_CONTENT_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOW_CONTENT_CHANGED:kotlin.Int) for those sources. Details about the change are available from [getContentChangeTypes()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#getContentChangeTypes()).

Do not use this to get an accessibility service to make non-pane announcements. Instead, follow the practices described in [View.announceForAccessibility(CharSequence)](https://developer.android.com/reference/kotlin/android/view/View.html#announceForAccessibility(kotlin.CharSequence)).**Note:**this does not suggest calling announceForAccessibility(), but using the suggestions listed in its documentation. 

 Value: 32

### WINDOWS_CHANGE_ACCESSIBILITY_FOCUSED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WINDOWS_CHANGE_ACCESSIBILITY_FOCUSED: Int
```

Change type for [TYPE_WINDOWS_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOWS_CHANGED:kotlin.Int) event: The window's [AccessibilityWindowInfo.isAccessibilityFocused()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#isAccessibilityFocused())changed. 

 Value: 128

### WINDOWS_CHANGE_ACTIVE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WINDOWS_CHANGE_ACTIVE: Int
```

Change type for [TYPE_WINDOWS_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOWS_CHANGED:kotlin.Int) event: The window's [AccessibilityWindowInfo.isActive()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#isActive())changed. 

 Value: 32

### WINDOWS_CHANGE_ADDED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WINDOWS_CHANGE_ADDED: Int
```

Change type for [TYPE_WINDOWS_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOWS_CHANGED:kotlin.Int) event: The window was added. 

 Value: 1

### WINDOWS_CHANGE_BOUNDS

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WINDOWS_CHANGE_BOUNDS: Int
```

Change type for [TYPE_WINDOWS_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOWS_CHANGED:kotlin.Int) event: The window's bounds changed.

Starting in [R](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int), this event implies the window's region changed. It's also possible that region changed but bounds doesn't. 

 Value: 8

### WINDOWS_CHANGE_CHILDREN

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WINDOWS_CHANGE_CHILDREN: Int
```

Change type for [TYPE_WINDOWS_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOWS_CHANGED:kotlin.Int) event: The window's children changed. 

 Value: 512

### WINDOWS_CHANGE_FOCUSED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WINDOWS_CHANGE_FOCUSED: Int
```

Change type for [TYPE_WINDOWS_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOWS_CHANGED:kotlin.Int) event: The window's [AccessibilityWindowInfo.isFocused()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo#isFocused())changed. 

 Value: 64

### WINDOWS_CHANGE_LAYER

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WINDOWS_CHANGE_LAYER: Int
```

Change type for [TYPE_WINDOWS_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOWS_CHANGED:kotlin.Int) event: The window's layer changed. 

 Value: 16

### WINDOWS_CHANGE_PARENT

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WINDOWS_CHANGE_PARENT: Int
```

Change type for [TYPE_WINDOWS_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOWS_CHANGED:kotlin.Int) event: The window's parent changed. 

 Value: 256

### WINDOWS_CHANGE_PIP

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WINDOWS_CHANGE_PIP: Int
```

Change type for [TYPE_WINDOWS_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOWS_CHANGED:kotlin.Int) event: The window either entered or exited picture-in-picture mode. 

 Value: 1024

### WINDOWS_CHANGE_REMOVED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WINDOWS_CHANGE_REMOVED: Int
```

Change type for [TYPE_WINDOWS_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOWS_CHANGED:kotlin.Int) event: A window was removed. 

 Value: 2

### WINDOWS_CHANGE_TITLE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WINDOWS_CHANGE_TITLE: Int
```

Change type for [TYPE_WINDOWS_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOWS_CHANGED:kotlin.Int) event: The window's title changed. 

 Value: 4

## Public constructors

### AccessibilityEvent

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AccessibilityEvent()
```

Creates a new [AccessibilityEvent](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#). 

### AccessibilityEvent

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AccessibilityEvent(event: AccessibilityEvent)
```

Copy constructor. Creates a new [AccessibilityEvent](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#), and this instance is initialized from the given`event`.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `event` | [AccessibilityEvent](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#):The other event. This value cannot be`null`. |

### AccessibilityEvent

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AccessibilityEvent(eventType: Int)
```

Creates a new [AccessibilityEvent](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#) with the given`eventType`.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------|
| `eventType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The event type. |

## Public methods

### appendRecord

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun appendRecord(record: AccessibilityRecord!): Unit
```

Appends an [AccessibilityRecord](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord) to the end of event records.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `record` | [AccessibilityRecord](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord)!:The record to append. |

| Exceptions ||
|-----------------------------------|-----------------------------------------|
| `java.lang.IllegalStateException` | If called from an AccessibilityService. |

### describeContents

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of [writeToParcel(android.os.Parcel,int)](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)), the return value of this method must include the [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) bit.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### eventTypeToString

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun eventTypeToString(eventType: Int): String!
```

Returns the string representation of an event type. For example, [TYPE_VIEW_CLICKED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_CLICKED:kotlin.Int) is represented by the string TYPE_VIEW_CLICKED.

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

Gets the bit mask of change types signaled by a [TYPE_WINDOW_CONTENT_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOW_CONTENT_CHANGED:kotlin.Int) event or [TYPE_WINDOW_STATE_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOW_STATE_CHANGED:kotlin.Int). A single event may represent multiple change types.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The bit mask of change types. One or more of: - [CONTENT_CHANGE_TYPE_CONTENT_DESCRIPTION](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_CONTENT_DESCRIPTION:kotlin.Int) - [CONTENT_CHANGE_TYPE_STATE_DESCRIPTION](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_STATE_DESCRIPTION:kotlin.Int) - [CONTENT_CHANGE_TYPE_SUBTREE](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_SUBTREE:kotlin.Int) - [CONTENT_CHANGE_TYPE_TEXT](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_TEXT:kotlin.Int) - [CONTENT_CHANGE_TYPE_PANE_TITLE](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_PANE_TITLE:kotlin.Int) - [CONTENT_CHANGE_TYPE_UNDEFINED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_UNDEFINED:kotlin.Int) - [CONTENT_CHANGE_TYPE_PANE_APPEARED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_PANE_APPEARED:kotlin.Int) - [CONTENT_CHANGE_TYPE_PANE_DISAPPEARED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_PANE_DISAPPEARED:kotlin.Int) - [CONTENT_CHANGE_TYPE_DRAG_STARTED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_DRAG_STARTED:kotlin.Int) - [CONTENT_CHANGE_TYPE_DRAG_DROPPED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_DRAG_DROPPED:kotlin.Int) - [CONTENT_CHANGE_TYPE_DRAG_CANCELLED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_DRAG_CANCELLED:kotlin.Int) - [CONTENT_CHANGE_TYPE_CONTENT_INVALID](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_CONTENT_INVALID:kotlin.Int) - [CONTENT_CHANGE_TYPE_ERROR](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_ERROR:kotlin.Int) - [CONTENT_CHANGE_TYPE_ENABLED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_ENABLED:kotlin.Int) Value is either`0`or a combination of [android.view.accessibility.AccessibilityEvent#CONTENT_CHANGE_TYPE_UNDEFINED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_UNDEFINED:kotlin.Int), [android.view.accessibility.AccessibilityEvent#CONTENT_CHANGE_TYPE_SUBTREE](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_SUBTREE:kotlin.Int), [android.view.accessibility.AccessibilityEvent#CONTENT_CHANGE_TYPE_TEXT](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_TEXT:kotlin.Int), [android.view.accessibility.AccessibilityEvent#CONTENT_CHANGE_TYPE_CONTENT_DESCRIPTION](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_CONTENT_DESCRIPTION:kotlin.Int), [android.view.accessibility.AccessibilityEvent#CONTENT_CHANGE_TYPE_STATE_DESCRIPTION](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_STATE_DESCRIPTION:kotlin.Int), [android.view.accessibility.AccessibilityEvent#CONTENT_CHANGE_TYPE_PANE_TITLE](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_PANE_TITLE:kotlin.Int), [android.view.accessibility.AccessibilityEvent#CONTENT_CHANGE_TYPE_PANE_APPEARED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_PANE_APPEARED:kotlin.Int), [android.view.accessibility.AccessibilityEvent#CONTENT_CHANGE_TYPE_PANE_DISAPPEARED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_PANE_DISAPPEARED:kotlin.Int), [android.view.accessibility.AccessibilityEvent#CONTENT_CHANGE_TYPE_DRAG_STARTED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_DRAG_STARTED:kotlin.Int), [android.view.accessibility.AccessibilityEvent#CONTENT_CHANGE_TYPE_DRAG_DROPPED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_DRAG_DROPPED:kotlin.Int), [android.view.accessibility.AccessibilityEvent#CONTENT_CHANGE_TYPE_DRAG_CANCELLED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_DRAG_CANCELLED:kotlin.Int), [android.view.accessibility.AccessibilityEvent#CONTENT_CHANGE_TYPE_CONTENT_INVALID](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_CONTENT_INVALID:kotlin.Int), [android.view.accessibility.AccessibilityEvent#CONTENT_CHANGE_TYPE_ERROR](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_ERROR:kotlin.Int), [android.view.accessibility.AccessibilityEvent#CONTENT_CHANGE_TYPE_ENABLED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_ENABLED:kotlin.Int), [android.view.accessibility.AccessibilityEvent#CONTENT_CHANGE_TYPE_CHECKED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_CHECKED:kotlin.Int), [android.view.accessibility.AccessibilityEvent#CONTENT_CHANGE_TYPE_EXPANDED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_EXPANDED:kotlin.Int), and [android.view.accessibility.AccessibilityEvent#CONTENT_CHANGE_TYPE_SUPPLEMENTAL_DESCRIPTION](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_SUPPLEMENTAL_DESCRIPTION:kotlin.Int) |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The event type. Value is either`0`or a combination of [android.view.accessibility.AccessibilityEvent#TYPE_VIEW_CLICKED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_CLICKED:kotlin.Int), [android.view.accessibility.AccessibilityEvent#TYPE_VIEW_LONG_CLICKED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_LONG_CLICKED:kotlin.Int), [android.view.accessibility.AccessibilityEvent#TYPE_VIEW_SELECTED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_SELECTED:kotlin.Int), [android.view.accessibility.AccessibilityEvent#TYPE_VIEW_FOCUSED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_FOCUSED:kotlin.Int), [android.view.accessibility.AccessibilityEvent#TYPE_VIEW_TEXT_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_TEXT_CHANGED:kotlin.Int), [android.view.accessibility.AccessibilityEvent#TYPE_WINDOW_STATE_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOW_STATE_CHANGED:kotlin.Int), [android.view.accessibility.AccessibilityEvent#TYPE_NOTIFICATION_STATE_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_NOTIFICATION_STATE_CHANGED:kotlin.Int), [android.view.accessibility.AccessibilityEvent#TYPE_VIEW_HOVER_ENTER](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_HOVER_ENTER:kotlin.Int), [android.view.accessibility.AccessibilityEvent#TYPE_VIEW_HOVER_EXIT](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_HOVER_EXIT:kotlin.Int), [android.view.accessibility.AccessibilityEvent#TYPE_TOUCH_EXPLORATION_GESTURE_START](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_TOUCH_EXPLORATION_GESTURE_START:kotlin.Int), [android.view.accessibility.AccessibilityEvent#TYPE_TOUCH_EXPLORATION_GESTURE_END](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_TOUCH_EXPLORATION_GESTURE_END:kotlin.Int), [android.view.accessibility.AccessibilityEvent#TYPE_WINDOW_CONTENT_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOW_CONTENT_CHANGED:kotlin.Int), [android.view.accessibility.AccessibilityEvent#TYPE_VIEW_SCROLLED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_SCROLLED:kotlin.Int), [android.view.accessibility.AccessibilityEvent#TYPE_VIEW_TEXT_SELECTION_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_TEXT_SELECTION_CHANGED:kotlin.Int), [android.view.accessibility.AccessibilityEvent#TYPE_ANNOUNCEMENT](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_ANNOUNCEMENT:kotlin.Int), [android.view.accessibility.AccessibilityEvent#TYPE_VIEW_ACCESSIBILITY_FOCUSED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_ACCESSIBILITY_FOCUSED:kotlin.Int), [android.view.accessibility.AccessibilityEvent#TYPE_VIEW_ACCESSIBILITY_FOCUS_CLEARED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_ACCESSIBILITY_FOCUS_CLEARED:kotlin.Int), [android.view.accessibility.AccessibilityEvent#TYPE_VIEW_TEXT_TRAVERSED_AT_MOVEMENT_GRANULARITY](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_TEXT_TRAVERSED_AT_MOVEMENT_GRANULARITY:kotlin.Int), [android.view.accessibility.AccessibilityEvent#TYPE_GESTURE_DETECTION_START](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_GESTURE_DETECTION_START:kotlin.Int), [android.view.accessibility.AccessibilityEvent#TYPE_GESTURE_DETECTION_END](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_GESTURE_DETECTION_END:kotlin.Int), [android.view.accessibility.AccessibilityEvent#TYPE_TOUCH_INTERACTION_START](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_TOUCH_INTERACTION_START:kotlin.Int), [android.view.accessibility.AccessibilityEvent#TYPE_TOUCH_INTERACTION_END](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_TOUCH_INTERACTION_END:kotlin.Int), [android.view.accessibility.AccessibilityEvent#TYPE_WINDOWS_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOWS_CHANGED:kotlin.Int), [android.view.accessibility.AccessibilityEvent#TYPE_VIEW_CONTEXT_CLICKED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_CONTEXT_CLICKED:kotlin.Int), [android.view.accessibility.AccessibilityEvent#TYPE_ASSIST_READING_CONTEXT](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_ASSIST_READING_CONTEXT:kotlin.Int), [android.view.accessibility.AccessibilityEvent#TYPE_SPEECH_STATE_CHANGE](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_SPEECH_STATE_CHANGE:kotlin.Int), and [android.view.accessibility.AccessibilityEvent#TYPE_VIEW_TARGETED_BY_SCROLL](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_TARGETED_BY_SCROLL:kotlin.Int) |

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
| [AccessibilityRecord](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord)! | The record at the specified index. |

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

Gets the bit mask of the speech state signaled by a [TYPE_SPEECH_STATE_CHANGE](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_SPEECH_STATE_CHANGE:kotlin.Int) event.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The bit mask of speech change types. |

**See Also**

- [#SPEECH_STATE_SPEAKING_START](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#SPEECH_STATE_SPEAKING_START:kotlin.Int)
- [#SPEECH_STATE_SPEAKING_END](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#SPEECH_STATE_SPEAKING_END:kotlin.Int)
- [#SPEECH_STATE_LISTENING_START](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#SPEECH_STATE_LISTENING_START:kotlin.Int)
- [#SPEECH_STATE_LISTENING_END](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#SPEECH_STATE_LISTENING_END:kotlin.Int) 

### getWindowChanges

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getWindowChanges(): Int
```

Get the bit mask of change types signaled by a [TYPE_WINDOWS_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOWS_CHANGED:kotlin.Int) event. A single event may represent multiple change types.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The bit mask of change types. Value is either`0`or a combination of [android.view.accessibility.AccessibilityEvent#WINDOWS_CHANGE_ADDED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#WINDOWS_CHANGE_ADDED:kotlin.Int), [android.view.accessibility.AccessibilityEvent#WINDOWS_CHANGE_REMOVED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#WINDOWS_CHANGE_REMOVED:kotlin.Int), [android.view.accessibility.AccessibilityEvent#WINDOWS_CHANGE_TITLE](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#WINDOWS_CHANGE_TITLE:kotlin.Int), [android.view.accessibility.AccessibilityEvent#WINDOWS_CHANGE_BOUNDS](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#WINDOWS_CHANGE_BOUNDS:kotlin.Int), [android.view.accessibility.AccessibilityEvent#WINDOWS_CHANGE_LAYER](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#WINDOWS_CHANGE_LAYER:kotlin.Int), [android.view.accessibility.AccessibilityEvent#WINDOWS_CHANGE_ACTIVE](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#WINDOWS_CHANGE_ACTIVE:kotlin.Int), [android.view.accessibility.AccessibilityEvent#WINDOWS_CHANGE_FOCUSED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#WINDOWS_CHANGE_FOCUSED:kotlin.Int), [android.view.accessibility.AccessibilityEvent#WINDOWS_CHANGE_ACCESSIBILITY_FOCUSED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#WINDOWS_CHANGE_ACCESSIBILITY_FOCUSED:kotlin.Int), [android.view.accessibility.AccessibilityEvent#WINDOWS_CHANGE_PARENT](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#WINDOWS_CHANGE_PARENT:kotlin.Int), [android.view.accessibility.AccessibilityEvent#WINDOWS_CHANGE_CHILDREN](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#WINDOWS_CHANGE_CHILDREN:kotlin.Int), and [android.view.accessibility.AccessibilityEvent#WINDOWS_CHANGE_PIP](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#WINDOWS_CHANGE_PIP:kotlin.Int) |

**See Also**

- [#WINDOWS_CHANGE_ADDED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#WINDOWS_CHANGE_ADDED:kotlin.Int)
- [#WINDOWS_CHANGE_REMOVED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#WINDOWS_CHANGE_REMOVED:kotlin.Int)
- [#WINDOWS_CHANGE_TITLE](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#WINDOWS_CHANGE_TITLE:kotlin.Int)
- [#WINDOWS_CHANGE_BOUNDS](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#WINDOWS_CHANGE_BOUNDS:kotlin.Int)
- [#WINDOWS_CHANGE_LAYER](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#WINDOWS_CHANGE_LAYER:kotlin.Int)
- [#WINDOWS_CHANGE_ACTIVE](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#WINDOWS_CHANGE_ACTIVE:kotlin.Int)
- [#WINDOWS_CHANGE_FOCUSED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#WINDOWS_CHANGE_FOCUSED:kotlin.Int)
- [#WINDOWS_CHANGE_ACCESSIBILITY_FOCUSED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#WINDOWS_CHANGE_ACCESSIBILITY_FOCUSED:kotlin.Int)
- [#WINDOWS_CHANGE_PARENT](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#WINDOWS_CHANGE_PARENT:kotlin.Int)
- [#WINDOWS_CHANGE_CHILDREN](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#WINDOWS_CHANGE_CHILDREN:kotlin.Int)
- [#WINDOWS_CHANGE_PIP](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#WINDOWS_CHANGE_PIP:kotlin.Int) 

### initFromParcel

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun initFromParcel(parcel: Parcel!): Unit
```

Creates a new instance from a [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#).

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parcel` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)!:A parcel containing the state of a [AccessibilityEvent](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#). |

### isAccessibilityDataSensitive

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isAccessibilityDataSensitive(): Boolean
```

Whether the event should only be delivered to an [android.accessibilityservice.AccessibilityService](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#) with the [android.accessibilityservice.AccessibilityServiceInfo#isAccessibilityTool](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo.html#isAccessibilityTool())property set to true.

Initial value matches the [android.view.View#isAccessibilityDataSensitive](https://developer.android.com/reference/kotlin/android/view/View.html#isAccessibilityDataSensitive())property from the event's source node, if present, or false by default.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the event should be delivered only to isAccessibilityTool services, false otherwise. |

**See Also**

- [#setAccessibilityDataSensitive](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#setAccessibilityDataSensitive(kotlin.Boolean)) 

### obtain

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun obtain(): AccessibilityEvent!
```

**Deprecated:** *Object pooling has been discontinued. Create a new instance using the constructor [AccessibilityEvent()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#AccessibilityEvent())instead.*

Instantiates a new AccessibilityEvent instance.

| Return ||
|----------------------------------------------------------------------------------------------------------------------|--------------|
| [AccessibilityEvent](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#)! | An instance. |

### obtain

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun obtain(event: AccessibilityEvent!): AccessibilityEvent!
```

**Deprecated:** *Object pooling has been discontinued. Create a new instance using the constructor [AccessibilityEvent()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#AccessibilityEvent())instead.*

Instantiates a new AccessibilityEvent instance. The returned instance is initialized from the given`event`.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------|
| `event` | [AccessibilityEvent](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#)!:The other event. |

| Return ||
|----------------------------------------------------------------------------------------------------------------------|--------------|
| [AccessibilityEvent](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#)! | An instance. |

### obtain

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun obtain(eventType: Int): AccessibilityEvent!
```

**Deprecated:** *Object pooling has been discontinued. Create a new instance using the constructor [AccessibilityEvent()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#AccessibilityEvent())instead.*

Instantiates a new AccessibilityEvent instance with its type property set.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------|
| `eventType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The event type. |

| Return ||
|----------------------------------------------------------------------------------------------------------------------|--------------|
| [AccessibilityEvent](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#)! | An instance. |

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

Sets whether the event should only be delivered to an [android.accessibilityservice.AccessibilityService](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#) with the [android.accessibilityservice.AccessibilityServiceInfo#isAccessibilityTool](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo.html#isAccessibilityTool())property set to true.

This will be set automatically based on the event's source (if present). If creating and sending an event directly through [AccessibilityManager](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager)(where an event may have no source) then this method must be called explicitly if you want non-default behavior.

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

Valid actions are defined in [AccessibilityNodeInfo](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo):

- [AccessibilityNodeInfo.ACTION_ACCESSIBILITY_FOCUS](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_ACCESSIBILITY_FOCUS:kotlin.Int)
- [AccessibilityNodeInfo.ACTION_CLEAR_ACCESSIBILITY_FOCUS](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_CLEAR_ACCESSIBILITY_FOCUS:kotlin.Int)
- [AccessibilityNodeInfo.ACTION_CLEAR_FOCUS](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_CLEAR_FOCUS:kotlin.Int)
- [AccessibilityNodeInfo.ACTION_CLEAR_SELECTION](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_CLEAR_SELECTION:kotlin.Int)
- [AccessibilityNodeInfo.ACTION_CLICK](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_CLICK:kotlin.Int)
- [AccessibilityNodeInfo.ACTION_LONG_CLICK](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_LONG_CLICK:kotlin.Int)
- [AccessibilityNodeInfo.ACTION_NEXT_AT_MOVEMENT_GRANULARITY](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_NEXT_AT_MOVEMENT_GRANULARITY:kotlin.Int)
- [AccessibilityNodeInfo.ACTION_PREVIOUS_AT_MOVEMENT_GRANULARITY](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_PREVIOUS_AT_MOVEMENT_GRANULARITY:kotlin.Int)
- [AccessibilityNodeInfo.ACTION_NEXT_HTML_ELEMENT](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_NEXT_HTML_ELEMENT:kotlin.Int)
- [AccessibilityNodeInfo.ACTION_PREVIOUS_HTML_ELEMENT](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_PREVIOUS_HTML_ELEMENT:kotlin.Int)
- [AccessibilityNodeInfo.ACTION_SCROLL_FORWARD](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_SCROLL_FORWARD:kotlin.Int)
- [AccessibilityNodeInfo.ACTION_SCROLL_BACKWARD](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_SCROLL_BACKWARD:kotlin.Int)
- [AccessibilityNodeInfo.ACTION_COPY](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_COPY:kotlin.Int)
- [AccessibilityNodeInfo.ACTION_PASTE](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_PASTE:kotlin.Int)
- [AccessibilityNodeInfo.ACTION_CUT](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_CUT:kotlin.Int)
- [AccessibilityNodeInfo.ACTION_SET_SELECTION](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_SET_SELECTION:kotlin.Int)
- [AccessibilityNodeInfo.ACTION_EXPAND](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_EXPAND:kotlin.Int)
- [AccessibilityNodeInfo.ACTION_COLLAPSE](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_COLLAPSE:kotlin.Int)
- [AccessibilityNodeInfo.ACTION_DISMISS](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_DISMISS:kotlin.Int)
- [AccessibilityNodeInfo.ACTION_SET_TEXT](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#ACTION_SET_TEXT:kotlin.Int)
- etc.

| Parameters ||
|----------|----------------------------------------------------------------------------------------|
| `action` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The action. |

| Exceptions ||
|-----------------------------------|-----------------------------------------|
| `java.lang.IllegalStateException` | If called from an AccessibilityService. |

**See Also**

- [android.view.accessibility.AccessibilityNodeInfo#performAction(int)](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo#performAction(kotlin.Int)) 

### setContentChangeTypes

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setContentChangeTypes(changeTypes: Int): Unit
```

Sets the bit mask of node tree changes signaled by an [TYPE_WINDOW_CONTENT_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOW_CONTENT_CHANGED:kotlin.Int) event.

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `changeTypes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The bit mask of change types. Value is either`0`or a combination of [android.view.accessibility.AccessibilityEvent#CONTENT_CHANGE_TYPE_UNDEFINED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_UNDEFINED:kotlin.Int), [android.view.accessibility.AccessibilityEvent#CONTENT_CHANGE_TYPE_SUBTREE](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_SUBTREE:kotlin.Int), [android.view.accessibility.AccessibilityEvent#CONTENT_CHANGE_TYPE_TEXT](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_TEXT:kotlin.Int), [android.view.accessibility.AccessibilityEvent#CONTENT_CHANGE_TYPE_CONTENT_DESCRIPTION](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_CONTENT_DESCRIPTION:kotlin.Int), [android.view.accessibility.AccessibilityEvent#CONTENT_CHANGE_TYPE_STATE_DESCRIPTION](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_STATE_DESCRIPTION:kotlin.Int), [android.view.accessibility.AccessibilityEvent#CONTENT_CHANGE_TYPE_PANE_TITLE](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_PANE_TITLE:kotlin.Int), [android.view.accessibility.AccessibilityEvent#CONTENT_CHANGE_TYPE_PANE_APPEARED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_PANE_APPEARED:kotlin.Int), [android.view.accessibility.AccessibilityEvent#CONTENT_CHANGE_TYPE_PANE_DISAPPEARED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_PANE_DISAPPEARED:kotlin.Int), [android.view.accessibility.AccessibilityEvent#CONTENT_CHANGE_TYPE_DRAG_STARTED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_DRAG_STARTED:kotlin.Int), [android.view.accessibility.AccessibilityEvent#CONTENT_CHANGE_TYPE_DRAG_DROPPED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_DRAG_DROPPED:kotlin.Int), [android.view.accessibility.AccessibilityEvent#CONTENT_CHANGE_TYPE_DRAG_CANCELLED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_DRAG_CANCELLED:kotlin.Int), [android.view.accessibility.AccessibilityEvent#CONTENT_CHANGE_TYPE_CONTENT_INVALID](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_CONTENT_INVALID:kotlin.Int), [android.view.accessibility.AccessibilityEvent#CONTENT_CHANGE_TYPE_ERROR](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_ERROR:kotlin.Int), [android.view.accessibility.AccessibilityEvent#CONTENT_CHANGE_TYPE_ENABLED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_ENABLED:kotlin.Int), [android.view.accessibility.AccessibilityEvent#CONTENT_CHANGE_TYPE_CHECKED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_CHECKED:kotlin.Int), [android.view.accessibility.AccessibilityEvent#CONTENT_CHANGE_TYPE_EXPANDED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_EXPANDED:kotlin.Int), and [android.view.accessibility.AccessibilityEvent#CONTENT_CHANGE_TYPE_SUPPLEMENTAL_DESCRIPTION](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#CONTENT_CHANGE_TYPE_SUPPLEMENTAL_DESCRIPTION:kotlin.Int) |

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
| `eventType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The event type. Value is either`0`or a combination of [android.view.accessibility.AccessibilityEvent#TYPE_VIEW_CLICKED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_CLICKED:kotlin.Int), [android.view.accessibility.AccessibilityEvent#TYPE_VIEW_LONG_CLICKED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_LONG_CLICKED:kotlin.Int), [android.view.accessibility.AccessibilityEvent#TYPE_VIEW_SELECTED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_SELECTED:kotlin.Int), [android.view.accessibility.AccessibilityEvent#TYPE_VIEW_FOCUSED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_FOCUSED:kotlin.Int), [android.view.accessibility.AccessibilityEvent#TYPE_VIEW_TEXT_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_TEXT_CHANGED:kotlin.Int), [android.view.accessibility.AccessibilityEvent#TYPE_WINDOW_STATE_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOW_STATE_CHANGED:kotlin.Int), [android.view.accessibility.AccessibilityEvent#TYPE_NOTIFICATION_STATE_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_NOTIFICATION_STATE_CHANGED:kotlin.Int), [android.view.accessibility.AccessibilityEvent#TYPE_VIEW_HOVER_ENTER](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_HOVER_ENTER:kotlin.Int), [android.view.accessibility.AccessibilityEvent#TYPE_VIEW_HOVER_EXIT](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_HOVER_EXIT:kotlin.Int), [android.view.accessibility.AccessibilityEvent#TYPE_TOUCH_EXPLORATION_GESTURE_START](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_TOUCH_EXPLORATION_GESTURE_START:kotlin.Int), [android.view.accessibility.AccessibilityEvent#TYPE_TOUCH_EXPLORATION_GESTURE_END](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_TOUCH_EXPLORATION_GESTURE_END:kotlin.Int), [android.view.accessibility.AccessibilityEvent#TYPE_WINDOW_CONTENT_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOW_CONTENT_CHANGED:kotlin.Int), [android.view.accessibility.AccessibilityEvent#TYPE_VIEW_SCROLLED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_SCROLLED:kotlin.Int), [android.view.accessibility.AccessibilityEvent#TYPE_VIEW_TEXT_SELECTION_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_TEXT_SELECTION_CHANGED:kotlin.Int), [android.view.accessibility.AccessibilityEvent#TYPE_ANNOUNCEMENT](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_ANNOUNCEMENT:kotlin.Int), [android.view.accessibility.AccessibilityEvent#TYPE_VIEW_ACCESSIBILITY_FOCUSED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_ACCESSIBILITY_FOCUSED:kotlin.Int), [android.view.accessibility.AccessibilityEvent#TYPE_VIEW_ACCESSIBILITY_FOCUS_CLEARED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_ACCESSIBILITY_FOCUS_CLEARED:kotlin.Int), [android.view.accessibility.AccessibilityEvent#TYPE_VIEW_TEXT_TRAVERSED_AT_MOVEMENT_GRANULARITY](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_TEXT_TRAVERSED_AT_MOVEMENT_GRANULARITY:kotlin.Int), [android.view.accessibility.AccessibilityEvent#TYPE_GESTURE_DETECTION_START](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_GESTURE_DETECTION_START:kotlin.Int), [android.view.accessibility.AccessibilityEvent#TYPE_GESTURE_DETECTION_END](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_GESTURE_DETECTION_END:kotlin.Int), [android.view.accessibility.AccessibilityEvent#TYPE_TOUCH_INTERACTION_START](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_TOUCH_INTERACTION_START:kotlin.Int), [android.view.accessibility.AccessibilityEvent#TYPE_TOUCH_INTERACTION_END](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_TOUCH_INTERACTION_END:kotlin.Int), [android.view.accessibility.AccessibilityEvent#TYPE_WINDOWS_CHANGED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_WINDOWS_CHANGED:kotlin.Int), [android.view.accessibility.AccessibilityEvent#TYPE_VIEW_CONTEXT_CLICKED](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_CONTEXT_CLICKED:kotlin.Int), [android.view.accessibility.AccessibilityEvent#TYPE_ASSIST_READING_CONTEXT](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_ASSIST_READING_CONTEXT:kotlin.Int), [android.view.accessibility.AccessibilityEvent#TYPE_SPEECH_STATE_CHANGE](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_SPEECH_STATE_CHANGE:kotlin.Int), and [android.view.accessibility.AccessibilityEvent#TYPE_VIEW_TARGETED_BY_SCROLL](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_VIEW_TARGETED_BY_SCROLL:kotlin.Int) |

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

Sets the bit mask of the speech state change types signaled by a [TYPE_SPEECH_STATE_CHANGE](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#TYPE_SPEECH_STATE_CHANGE:kotlin.Int) event. The sender is responsible for ensuring that the state change types make sense. For example, the sender should not send [SPEECH_STATE_SPEAKING_START](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#SPEECH_STATE_SPEAKING_START:kotlin.Int) and [SPEECH_STATE_SPEAKING_END](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#SPEECH_STATE_SPEAKING_END:kotlin.Int) together.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `state` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is either`0`or a combination of [android.view.accessibility.AccessibilityEvent#SPEECH_STATE_SPEAKING_START](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#SPEECH_STATE_SPEAKING_START:kotlin.Int), [android.view.accessibility.AccessibilityEvent#SPEECH_STATE_SPEAKING_END](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#SPEECH_STATE_SPEAKING_END:kotlin.Int), [android.view.accessibility.AccessibilityEvent#SPEECH_STATE_LISTENING_START](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#SPEECH_STATE_LISTENING_START:kotlin.Int), and [android.view.accessibility.AccessibilityEvent#SPEECH_STATE_LISTENING_END](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#SPEECH_STATE_LISTENING_END:kotlin.Int) |

**See Also**

- [#SPEECH_STATE_SPEAKING_START](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#SPEECH_STATE_SPEAKING_START:kotlin.Int)
- [#SPEECH_STATE_SPEAKING_END](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#SPEECH_STATE_SPEAKING_END:kotlin.Int)
- [#SPEECH_STATE_LISTENING_START](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#SPEECH_STATE_LISTENING_START:kotlin.Int)
- [#SPEECH_STATE_LISTENING_END](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent#SPEECH_STATE_LISTENING_END:kotlin.Int) 

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
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<AccessibilityEvent!>
```  
**See Also**

- [android.os.Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)
