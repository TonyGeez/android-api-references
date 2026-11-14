# android.view.accessibility

# android.view.accessibility

Kotlin| [Java](../android/view/accessibility/_package.md)
| --- | --- |

## Interfaces

| [AccessibilityEventSource](../android/view/accessibility/AccessibilityEventSource.md) | This interface is implemented by classes source of [AccessibilityEvent](../android/view/accessibility/AccessibilityEvent.md) s. |
| --- | --- |
| [AccessibilityServicesStateChangeListener](../android/view/accessibility/AccessibilityManager.AccessibilityServicesStateChangeListener.md) | Listener for changes to the state of accessibility services. |
| [AccessibilityStateChangeListener](../android/view/accessibility/AccessibilityManager.AccessibilityStateChangeListener.md) | Listener for the system accessibility state. |
| [AudioDescriptionRequestedChangeListener](../android/view/accessibility/AccessibilityManager.AudioDescriptionRequestedChangeListener.md) | Listener for the audio description by default state. |
| --- | --- |
| [HighContrastTextStateChangeListener](../android/view/accessibility/AccessibilityManager.HighContrastTextStateChangeListener.md) | Listener for the system high contrast text state. |
| [TouchExplorationStateChangeListener](../android/view/accessibility/AccessibilityManager.TouchExplorationStateChangeListener.md) | Listener for the system touch exploration state. |

## Classes

| [AccessibilityEvent](../android/view/accessibility/AccessibilityEvent.md) | This class represents accessibility events that are sent by the system when something notable happens in the user interface. |
| --- | --- |
| [AccessibilityManager](../android/view/accessibility/AccessibilityManager.md) | System level service that serves as an event dispatch for [AccessibilityEvent](../android/view/accessibility/AccessibilityEvent.md) s, and provides facilities for querying the accessibility state of the system. |
| [AccessibilityNodeInfo](../android/view/accessibility/AccessibilityNodeInfo.md) | This class represents a node of the window content as well as actions that can be requested from its source. |
| [AccessibilityNodeProvider](../android/view/accessibility/AccessibilityNodeProvider.md) | This class is the contract a client should implement to enable support of a virtual view hierarchy rooted at a given view for accessibility purposes. |
| --- | --- |
| [AccessibilityRecord](../android/view/accessibility/AccessibilityRecord.md) | Represents a record in an [AccessibilityEvent](../android/view/accessibility/AccessibilityEvent.md) and contains information about state change of its source [android.view.View](../android/view/View.md). |
| [AccessibilityRequestPreparer](../android/view/accessibility/AccessibilityRequestPreparer.md) | Object responsible to ensuring that a [View](../android/view/View.md) is prepared to meet a synchronous request for accessibility data. |
| [AccessibilityWindowInfo](../android/view/accessibility/AccessibilityWindowInfo.md) | This class represents a state snapshot of a window for accessibility purposes. |
| --- | --- |
| [CaptioningManager](../android/view/accessibility/CaptioningManager.md) | Contains methods for accessing and monitoring preferred video captioning state and visual properties. |
