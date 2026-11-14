# android.view.accessibility

# android.view.accessibility

Kotlin| [Java](https://developer.android.com/reference/android/view/accessibility/package-summary "View this page in Java")
| --- | --- |

## Interfaces

| [AccessibilityEventSource](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEventSource) | This interface is implemented by classes source of [AccessibilityEvent](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent) s. |
| --- | --- |
| [AccessibilityServicesStateChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.AccessibilityServicesStateChangeListener) | Listener for changes to the state of accessibility services. |
| [AccessibilityStateChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.AccessibilityStateChangeListener) | Listener for the system accessibility state. |
| [AudioDescriptionRequestedChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.AudioDescriptionRequestedChangeListener) | Listener for the audio description by default state. |
| --- | --- |
| [HighContrastTextStateChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.HighContrastTextStateChangeListener) | Listener for the system high contrast text state. |
| [TouchExplorationStateChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.TouchExplorationStateChangeListener) | Listener for the system touch exploration state. |

## Classes

| [AccessibilityEvent](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent) | This class represents accessibility events that are sent by the system when something notable happens in the user interface. |
| --- | --- |
| [AccessibilityManager](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager) | System level service that serves as an event dispatch for [AccessibilityEvent](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent) s, and provides facilities for querying the accessibility state of the system. |
| [AccessibilityNodeInfo](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo) | This class represents a node of the window content as well as actions that can be requested from its source. |
| [AccessibilityNodeProvider](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeProvider) | This class is the contract a client should implement to enable support of a virtual view hierarchy rooted at a given view for accessibility purposes. |
| --- | --- |
| [AccessibilityRecord](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRecord) | Represents a record in an [AccessibilityEvent](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent) and contains information about state change of its source [android.view.View](https://developer.android.com/reference/kotlin/android/view/View.html#). |
| [AccessibilityRequestPreparer](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRequestPreparer) | Object responsible to ensuring that a [View](https://developer.android.com/reference/kotlin/android/view/View.html#) is prepared to meet a synchronous request for accessibility data. |
| [AccessibilityWindowInfo](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityWindowInfo) | This class represents a state snapshot of a window for accessibility purposes. |
| --- | --- |
| [CaptioningManager](https://developer.android.com/reference/kotlin/android/view/accessibility/CaptioningManager) | Contains methods for accessing and monitoring preferred video captioning state and visual properties. |
