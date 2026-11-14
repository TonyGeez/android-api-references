# android.view.accessibility

# android.view.accessibility

Kotlin| [Java](_package.md)
| --- | --- |

## Interfaces

| [AccessibilityEventSource](AccessibilityEventSource.md) | This interface is implemented by classes source of [AccessibilityEvent](AccessibilityEvent.md) s. |
| --- | --- |
| [AccessibilityServicesStateChangeListener](../android/view/accessibility/AccessibilityManager.AccessibilityServicesStateChangeListener.md) | Listener for changes to the state of accessibility services. |
| [AccessibilityStateChangeListener](../android/view/accessibility/AccessibilityManager.AccessibilityStateChangeListener.md) | Listener for the system accessibility state. |
| [AudioDescriptionRequestedChangeListener](../android/view/accessibility/AccessibilityManager.AudioDescriptionRequestedChangeListener.md) | Listener for the audio description by default state. |
| --- | --- |
| [HighContrastTextStateChangeListener](../android/view/accessibility/AccessibilityManager.HighContrastTextStateChangeListener.md) | Listener for the system high contrast text state. |
| [TouchExplorationStateChangeListener](../android/view/accessibility/AccessibilityManager.TouchExplorationStateChangeListener.md) | Listener for the system touch exploration state. |

## Classes

| [AccessibilityEvent](AccessibilityEvent.md) | This class represents accessibility events that are sent by the system when something notable happens in the user interface. |
| --- | --- |
| [AccessibilityManager](AccessibilityManager.md) | System level service that serves as an event dispatch for [AccessibilityEvent](AccessibilityEvent.md) s, and provides facilities for querying the accessibility state of the system. |
| [AccessibilityNodeInfo](AccessibilityNodeInfo.md) | This class represents a node of the window content as well as actions that can be requested from its source. |
| [AccessibilityNodeProvider](AccessibilityNodeProvider.md) | This class is the contract a client should implement to enable support of a virtual view hierarchy rooted at a given view for accessibility purposes. |
| --- | --- |
| [AccessibilityRecord](AccessibilityRecord.md) | Represents a record in an [AccessibilityEvent](AccessibilityEvent.md) and contains information about state change of its source [android.view.View](../android.view/View.md). |
| [AccessibilityRequestPreparer](AccessibilityRequestPreparer.md) | Object responsible to ensuring that a [View](../android.view/View.md) is prepared to meet a synchronous request for accessibility data. |
| [AccessibilityWindowInfo](AccessibilityWindowInfo.md) | This class represents a state snapshot of a window for accessibility purposes. |
| --- | --- |
| [CaptioningManager](CaptioningManager.md) | Contains methods for accessing and monitoring preferred video captioning state and visual properties. |
