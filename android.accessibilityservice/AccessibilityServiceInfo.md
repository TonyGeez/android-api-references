Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AccessibilityServiceInfo

```
open class AccessibilityServiceInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.accessibilityservice.AccessibilityServiceInfo](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#) |

This class describes an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService`. The system notifies an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService` for `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#`s according to the information encapsulated in this class.

> [!NOTE]
>
> ### Developer Guides
>
> For more information about creating AccessibilityServices, read the [Accessibility](https://developer.android.com/guide/topics/ui/accessibility/index.html) developer guide.

<br />

## Summary

| XML attributes ||
|---|---|
| [`android:accessibilityEventTypes`](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#attr_AccessibilityServiceInfo) | The event types this service would like to receive as specified in android. |
| [`android:accessibilityFeedbackType`](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#attr_AccessibilityServiceInfo) | The feedback types this service provides as specified in android. |
| [`android:accessibilityFlags`](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#attr_AccessibilityServiceInfo) | Additional flags as specified in android. |
| --- | --- |
| [`android:animatedImageDrawable`](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#attr_AccessibilityServiceInfo) | Animated image of the accessibility service purpose or behavior, to help users understand how the service can help them. |
| [`android:canControlMagnification`](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#attr_AccessibilityServiceInfo) | Attribute whether the accessibility service wants to be able to control display magnification. |
| [`android:canPerformGestures`](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#attr_AccessibilityServiceInfo) | Attribute whether the accessibility service wants to be able to perform gestures. |
| --- | --- |
| [`android:canRequestFilterKeyEvents`](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#attr_AccessibilityServiceInfo) | Attribute whether the accessibility service wants to be able to request to filter key events. |
| [`android:canRequestFingerprintGestures`](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#attr_AccessibilityServiceInfo) | Attribute whether the accessibility service wants to be able to capture gestures from the fingerprint sensor. |
| [`android:canRequestTouchExplorationMode`](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#attr_AccessibilityServiceInfo) | Attribute whether the accessibility service wants to be able to request touch exploration mode in which touched items are spoken aloud and the UI can be explored via gestures. |
| --- | --- |
| [`android:canRetrieveWindowContent`](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#attr_AccessibilityServiceInfo) | Attribute whether the accessibility service wants to be able to retrieve the active window content. |
| [`android:canTakeScreenshot`](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#attr_AccessibilityServiceInfo) | Attribute whether the accessibility service wants to be able to take screenshot. |
| [`android:description`](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#attr_AccessibilityServiceInfo) | Description of the accessibility service usage, availability, or limitations (e.g. isn't supported by all apps). |
| --- | --- |
| [`android:htmlDescription`](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#attr_AccessibilityServiceInfo) | Html description of the accessibility service usage, availability, or limitations (e.g. isn't supported by all apps). |
| [`android:interactiveUiTimeout`](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#attr_AccessibilityServiceInfo) | A recommended timeout in milliseconds used in android. |
| [`android:intro`](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#attr_AccessibilityServiceInfo) | Detailed intro of the accessibility service purpose or behavior. |
| --- | --- |
| [`android:isAccessibilityTool`](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#attr_AccessibilityServiceInfo) | Attribute indicating whether the accessibility service is used to assist users with disabilities. |
| [`android:nonInteractiveUiTimeout`](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#attr_AccessibilityServiceInfo) | A recommended timeout in milliseconds used in android. |
| [`android:notificationTimeout`](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#attr_AccessibilityServiceInfo) | The minimal period in milliseconds between two accessibility events of the same type are sent to this service. |
| --- | --- |
| [`android:packageNames`](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#attr_AccessibilityServiceInfo) | Comma separated package names from which this service would like to receive events (leave out for all packages). |
| [`android:settingsActivity`](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#attr_AccessibilityServiceInfo) | Fully qualified class name of an activity that allows the user to modify the settings for this service. |
| [`android:summary`](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#attr_AccessibilityServiceInfo) | Brief summary of the accessibility service purpose or behavior. |
| --- | --- |
| [`android:tileService`](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#attr_AccessibilityServiceInfo) | Fully qualified class name of android. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#CAPABILITY_CAN_CONTROL_MAGNIFICATION:kotlin.Int` Capability: This accessibility service can control display magnification. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#CAPABILITY_CAN_PERFORM_GESTURES:kotlin.Int` Capability: This accessibility service can perform gestures. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#CAPABILITY_CAN_REQUEST_ENHANCED_WEB_ACCESSIBILITY:kotlin.Int` <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#CAPABILITY_CAN_REQUEST_FILTER_KEY_EVENTS:kotlin.Int` Capability: This accessibility service can request to filter the key event stream. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#CAPABILITY_CAN_REQUEST_FINGERPRINT_GESTURES:kotlin.Int` Capability: This accessibility service can capture gestures from the fingerprint sensor |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#CAPABILITY_CAN_REQUEST_TOUCH_EXPLORATION:kotlin.Int` Capability: This accessibility service can request touch exploration mode in which touched items are spoken aloud and the UI can be explored via gestures. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#CAPABILITY_CAN_RETRIEVE_WINDOW_CONTENT:kotlin.Int` Capability: This accessibility service can retrieve the active window content. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#CAPABILITY_CAN_TAKE_SCREENSHOT:kotlin.Int` Capability: This accessibility service can take screenshot. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#DEFAULT:kotlin.Int` If an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService` is the default for a given type. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FEEDBACK_ALL_MASK:kotlin.Int` Mask for all feedback types. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FEEDBACK_AUDIBLE:kotlin.Int` Denotes audible (not spoken) feedback. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FEEDBACK_BRAILLE:kotlin.Int` Denotes braille feedback. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FEEDBACK_GENERIC:kotlin.Int` Denotes generic feedback. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FEEDBACK_HAPTIC:kotlin.Int` Denotes haptic feedback. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FEEDBACK_SPOKEN:kotlin.Int` Denotes spoken feedback. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FEEDBACK_VISUAL:kotlin.Int` Denotes visual feedback. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FLAG_ENABLE_ACCESSIBILITY_VOLUME:kotlin.Int` This flag requests that all audio tracks system-wide with `https://developer.android.com/reference/kotlin/android/media/AudioAttributes.html#USAGE_ASSISTANCE_ACCESSIBILITY:kotlin.Int` be controlled by the `https://developer.android.com/reference/kotlin/android/media/AudioManager.html#STREAM_ACCESSIBILITY:kotlin.Int` volume. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FLAG_INCLUDE_NOT_IMPORTANT_VIEWS:kotlin.Int` If this flag is set the system will regard views that are not important for accessibility in addition to the ones that are important for accessibility. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FLAG_INPUT_METHOD_EDITOR:kotlin.Int` This flag makes the AccessibilityService an input method editor with a subset of input method editor capabilities: get the `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection.html#` and get text selection change notifications. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FLAG_REPORT_VIEW_IDS:kotlin.Int` This flag requests that the `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.html#`s obtained by an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService` contain the id of the source view. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FLAG_REQUEST_2_FINGER_PASSTHROUGH:kotlin.Int` This flag requests that when `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FLAG_REQUEST_MULTI_FINGER_GESTURES:kotlin.Int` is enabled, two-finger passthrough gestures are re-enabled. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FLAG_REQUEST_ACCESSIBILITY_BUTTON:kotlin.Int` This flag indicates to the system that the accessibility service requests that an accessibility button be shown within the system's navigation area, if available. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FLAG_REQUEST_ENHANCED_WEB_ACCESSIBILITY:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FLAG_REQUEST_FILTER_KEY_EVENTS:kotlin.Int` This flag requests from the system to filter key events. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FLAG_REQUEST_FINGERPRINT_GESTURES:kotlin.Int` This flag requests that all fingerprint gestures be sent to the accessibility service. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FLAG_REQUEST_MULTI_FINGER_GESTURES:kotlin.Int` This flag requests that when `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FLAG_REQUEST_TOUCH_EXPLORATION_MODE:kotlin.Int` is enabled, multi-finger gestures are also enabled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FLAG_REQUEST_SHORTCUT_WARNING_DIALOG_SPOKEN_FEEDBACK:kotlin.Int` This flag requests that accessibility shortcut warning dialog has spoken feedback when dialog is shown. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FLAG_REQUEST_TOUCH_EXPLORATION_MODE:kotlin.Int` This flag requests that the system gets into touch exploration mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FLAG_RETRIEVE_INTERACTIVE_WINDOWS:kotlin.Int` This flag indicates to the system that the accessibility service wants to access content of all interactive windows. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FLAG_SEND_MOTION_EVENTS:kotlin.Int` This flag requests that when `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FLAG_REQUEST_TOUCH_EXPLORATION_MODE:kotlin.Int` is enabled, a service will receive the motion events for each successfully-detected gesture. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FLAG_SERVICE_HANDLES_DOUBLE_TAP:kotlin.Int` This flag requests that when `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FLAG_REQUEST_TOUCH_EXPLORATION_MODE:kotlin.Int` is enabled, double tap and double tap and hold gestures are dispatched to the service rather than being handled by the framework. |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#AccessibilityServiceInfo()()` Creates a new instance. |

| Public methods ||
|---|---|
| open static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#capabilityToString(kotlin.Int)(capability: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the string representation of a capability. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| --- | --- |
| open static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#feedbackTypeToString(kotlin.Int)(feedbackType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the string representation of a feedback type. |
| open static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#flagToString(kotlin.Int)(flag: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the string representation of a flag. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#getCanRetrieveWindowContent()()` Whether this service can retrieve the current window's content. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#getCapabilities()()` Returns the bit mask of capabilities this accessibility service has such as being able to retrieve the active window content, etc. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#getDescription()()` Gets the non-localized description of the accessibility service. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#getId()()` The accessibility service id. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#getInteractiveUiTimeoutMillis()()` Get the recommended timeout for interactive controls. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#getMotionEventSources()()` Returns the bit mask of `https://developer.android.com/reference/kotlin/android/view/InputDevice.html#` sources that the accessibility service wants to listen to for generic `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#`s. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#getNonInteractiveUiTimeoutMillis()()` Get the recommended timeout for non-interactive controls. |
| --- | --- |
| open [ResolveInfo](https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo.html#)! | `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#getResolveInfo()()` The service `https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo.html#`. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#getSettingsActivityName()()` The settings activity name. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#getTileServiceName()()` Gets the name of `https://developer.android.com/reference/kotlin/android/service/quicksettings/TileService.html#` is associated with this accessibility service. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#hashCode()()` Returns a hash code value for the object. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#isAccessibilityTool()()` Indicates if the service is used to assist users with disabilities. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#loadDescription(android.content.pm.PackageManager)(packageManager: https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#!)` The localized description of the accessibility service. |
| --- | --- |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#loadIntro(android.content.pm.PackageManager)(packageManager: https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#)` The localized intro of the accessibility service. |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#loadSummary(android.content.pm.PackageManager)(packageManager: https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#!)` The localized summary of the accessibility service. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#setInteractiveUiTimeoutMillis(kotlin.Int)(timeout: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set the recommended time that interactive controls need to remain on the screen to support the user. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#setMotionEventSources(kotlin.Int)(motionEventSources: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the bit mask of `https://developer.android.com/reference/kotlin/android/view/InputDevice.html#` sources that the accessibility service wants to listen to for generic `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#`s. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#setNonInteractiveUiTimeoutMillis(kotlin.Int)(timeout: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set the recommended time that non-interactive controls need to remain on the screen to support the user. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#toString()()` Returns a string representation of the object. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#writeToParcel(android.os.Parcel,%20kotlin.Int)(parcel: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flagz: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [AccessibilityServiceInfo](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#)!\> | `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#CREATOR:android.os.Parcelable.Creator` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#eventTypes:kotlin.Int` The event types an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService` is interested in. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#feedbackType:kotlin.Int` The feedback type an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService` provides. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#flags:kotlin.Int` This field represents a set of flags used for configuring an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService`. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#notificationTimeout:kotlin.Long` The timeout, in milliseconds, after the most recent event of a given type before an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService` is notified. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#packageNames:kotlin.Array` The package names an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService` is interested in. |
| --- | --- |

## XML attributes

### android:accessibilityEventTypes

```
android:accessibilityEventTypes
```
The event types this service would like to receive as specified in `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#`. This setting can be changed at runtime by calling `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#setServiceInfo(android.accessibilityservice.AccessibilityServiceInfo)`.

Must be one or more (separated by '|') of the following constant values.
| --- | --- |

| Constant | Value | Description |
|---|---|---|
| typeAllMask | ffffffff | Receives `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#TYPES_ALL_MASK:kotlin.Int` i.e. all events. |
| typeAnnouncement | 4000 | Receives `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#TYPE_ANNOUNCEMENT:kotlin.Int` events. |
| typeAssistReadingContext | 1000000 | Receives `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#TYPE_ASSIST_READING_CONTEXT:kotlin.Int` events. |
| --- | --- | --- |
| typeContextClicked | 800000 | Receives `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#TYPE_VIEW_CONTEXT_CLICKED:kotlin.Int` events. |
| typeGestureDetectionEnd | 80000 | Receives `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#TYPE_GESTURE_DETECTION_END:kotlin.Int` events. |
| typeGestureDetectionStart | 40000 | Receives `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#TYPE_GESTURE_DETECTION_START:kotlin.Int` events. |
| --- | --- | --- |
| typeNotificationStateChanged | 40 | Receives `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#TYPE_NOTIFICATION_STATE_CHANGED:kotlin.Int` events. |
| typeSpeechStateChange | 2000000 | Receives `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#TYPE_SPEECH_STATE_CHANGE:kotlin.Int` events. |
| typeTouchExplorationGestureEnd | 400 | Receives `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#TYPE_TOUCH_EXPLORATION_GESTURE_END:kotlin.Int` events. |
| --- | --- | --- |
| typeTouchExplorationGestureStart | 200 | Receives `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#TYPE_TOUCH_EXPLORATION_GESTURE_START:kotlin.Int` events. |
| typeTouchInteractionEnd | 200000 | Receives `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#TYPE_TOUCH_INTERACTION_END:kotlin.Int` events. |
| typeTouchInteractionStart | 100000 | Receives `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#TYPE_TOUCH_INTERACTION_START:kotlin.Int` events. |
| --- | --- | --- |
| typeViewAccessibilityFocusCleared | 10000 | Receives `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#TYPE_VIEW_ACCESSIBILITY_FOCUS_CLEARED:kotlin.Int` events. |
| typeViewAccessibilityFocused | 8000 | Receives `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#TYPE_VIEW_ACCESSIBILITY_FOCUSED:kotlin.Int` events. |
| typeViewClicked | 1 | Receives `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#TYPE_VIEW_CLICKED:kotlin.Int` events. |
| --- | --- | --- |
| typeViewFocused | 8 | Receives `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#TYPE_VIEW_FOCUSED:kotlin.Int` events. |
| typeViewHoverEnter | 80 | Receives `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#TYPE_VIEW_HOVER_ENTER:kotlin.Int` events. |
| typeViewHoverExit | 100 | Receives `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#TYPE_VIEW_HOVER_EXIT:kotlin.Int` events. |
| --- | --- | --- |
| typeViewLongClicked | 2 | Receives `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#TYPE_VIEW_LONG_CLICKED:kotlin.Int` events. |
| typeViewScrolled | 1000 | Receives `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#TYPE_VIEW_SCROLLED:kotlin.Int` events. |
| typeViewSelected | 4 | Receives `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#TYPE_VIEW_SELECTED:kotlin.Int` events. |
| --- | --- | --- |
| typeViewTextChanged | 10 | Receives `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#TYPE_VIEW_TEXT_CHANGED:kotlin.Int` events. |
| typeViewTextSelectionChanged | 2000 | Receives `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#TYPE_VIEW_TEXT_SELECTION_CHANGED:kotlin.Int` events. |
| typeViewTextTraversedAtMovementGranularity | 20000 | Receives `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#TYPE_VIEW_TEXT_TRAVERSED_AT_MOVEMENT_GRANULARITY:kotlin.Int` events. |
| --- | --- | --- |
| typeWindowContentChanged | 800 | Receives `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#TYPE_WINDOW_CONTENT_CHANGED:kotlin.Int` events. |
| typeWindowStateChanged | 20 | Receives `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#TYPE_WINDOW_STATE_CHANGED:kotlin.Int` events. |
| typeWindowsChanged | 400000 | Receives `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#TYPE_WINDOWS_CHANGED:kotlin.Int` events. |
| --- | --- | --- |

### android:accessibilityFeedbackType

```
android:accessibilityFeedbackType
```
The feedback types this service provides as specified in `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#`. This setting can be changed at runtime by calling `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#setServiceInfo(android.accessibilityservice.AccessibilityServiceInfo)`.

Must be one or more (separated by '|') of the following constant values.
| --- | --- |

| Constant | Value | Description |
|---|---|---|
| feedbackAllMask | ffffffff | Provides `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FEEDBACK_ALL_MASK:kotlin.Int` feedback. |
| feedbackAudible | 4 | Provides `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FEEDBACK_AUDIBLE:kotlin.Int` feedback. |
| feedbackGeneric | 10 | Provides `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FEEDBACK_GENERIC:kotlin.Int` feedback. |
| --- | --- | --- |
| feedbackHaptic | 2 | Provides `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FEEDBACK_HAPTIC:kotlin.Int` feedback. |
| feedbackSpoken | 1 | Provides `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FEEDBACK_SPOKEN:kotlin.Int` feedback. |
| feedbackVisual | 8 | Provides `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FEEDBACK_VISUAL:kotlin.Int` feedback. |
| --- | --- | --- |

### android:accessibilityFlags

```
android:accessibilityFlags
```
Additional flags as specified in `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#`. This setting can be changed at runtime by calling `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#setServiceInfo(android.accessibilityservice.AccessibilityServiceInfo)`.

Must be one or more (separated by '|') of the following constant values.
| --- | --- |

| Constant | Value | Description |
|---|---|---|
| flagDefault | 1 | Has flag `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#DEFAULT:kotlin.Int`. |
| flagEnableAccessibilityVolume | 80 | Has flag `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FLAG_ENABLE_ACCESSIBILITY_VOLUME:kotlin.Int`. |
| flagIncludeNotImportantViews | 2 | Has flag `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FLAG_INCLUDE_NOT_IMPORTANT_VIEWS:kotlin.Int`. |
| --- | --- | --- |
| flagInputMethodEditor | 8000 | Has flag `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FLAG_INPUT_METHOD_EDITOR:kotlin.Int`. |
| flagReportViewIds | 10 | Has flag `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FLAG_REPORT_VIEW_IDS:kotlin.Int`. |
| flagRequestAccessibilityButton | 100 | Has flag `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FLAG_REQUEST_ACCESSIBILITY_BUTTON:kotlin.Int`. |
| --- | --- | --- |
| flagRequestEnhancedWebAccessibility | 8 | Has flag `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FLAG_REQUEST_ENHANCED_WEB_ACCESSIBILITY:kotlin.Int`. Not used by the framework. |
| flagRequestFilterKeyEvents | 20 | Has flag `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FLAG_REQUEST_FILTER_KEY_EVENTS:kotlin.Int`. |
| flagRequestFingerprintGestures | 200 | Has flag `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FLAG_REQUEST_FINGERPRINT_GESTURES:kotlin.Int`. |
| --- | --- | --- |
| flagRequestMultiFingerGestures | 1000 | Has flag `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FLAG_REQUEST_MULTI_FINGER_GESTURES:kotlin.Int`. |
| flagRequestShortcutWarningDialogSpokenFeedback | 400 | Has flag `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FLAG_REQUEST_SHORTCUT_WARNING_DIALOG_SPOKEN_FEEDBACK:kotlin.Int`. |
| flagRequestTouchExplorationMode | 4 | Has flag `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FLAG_REQUEST_TOUCH_EXPLORATION_MODE:kotlin.Int`. |
| --- | --- | --- |
| flagRequireShortcut | 20000 | Has flag android.accessibilityservice.AccessibilityServiceInfo#FLAG_REQUIRE_SHORTCUT. |
| flagRetrieveInteractiveWindows | 40 | Has flag `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FLAG_RETRIEVE_INTERACTIVE_WINDOWS:kotlin.Int`. |
| flagSendMotionEvents | 4000 | |
| --- | --- | --- |
| flagServiceHandlesDoubleTap | 800 | Has flag `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FLAG_SERVICE_HANDLES_DOUBLE_TAP:kotlin.Int`. |

### android:animatedImageDrawable

```
android:animatedImageDrawable
```
Animated image of the accessibility service purpose or behavior, to help users understand how the service can help them.

May be a reference to another resource, in the form "`@[+][package:]type/name`" or a theme attribute in the form "`?[package:]type/name`".

### android:canControlMagnification

```
android:canControlMagnification
```
Attribute whether the accessibility service wants to be able to control display magnification.

May be a boolean value, such as "`true`" or "`false`".

### android:canPerformGestures

```
android:canPerformGestures
```
Attribute whether the accessibility service wants to be able to perform gestures.

May be a boolean value, such as "`true`" or "`false`".

### android:canRequestFilterKeyEvents

```
android:canRequestFilterKeyEvents
```
Attribute whether the accessibility service wants to be able to request to filter key events.

Required to allow setting the `https://developer.android.com/reference/kotlin/android/accessibilityservice/package-summary` flag.

May be a boolean value, such as "`true`" or "`false`".

### android:canRequestFingerprintGestures

```
android:canRequestFingerprintGestures
```
Attribute whether the accessibility service wants to be able to capture gestures from the fingerprint sensor.

Required to allow setting the `https://developer.android.com/reference/kotlin/android/accessibilityservice/package-summary` flag to have any effect.

May be a boolean value, such as "`true`" or "`false`".

### android:canRequestTouchExplorationMode

```
android:canRequestTouchExplorationMode
```
Attribute whether the accessibility service wants to be able to request touch exploration mode in which touched items are spoken aloud and the UI can be explored via gestures.

Required to allow setting the `https://developer.android.com/reference/kotlin/android/accessibilityservice/package-summary` flag.

May be a boolean value, such as "`true`" or "`false`".

### android:canRetrieveWindowContent

```
android:canRetrieveWindowContent
```
Attribute whether the accessibility service wants to be able to retrieve the active window content. This setting cannot be changed at runtime.

Required to allow setting the `https://developer.android.com/reference/kotlin/android/accessibilityservice/package-summary` flag.

May be a boolean value, such as "`true`" or "`false`".

### android:canTakeScreenshot

```
android:canTakeScreenshot
```
Attribute whether the accessibility service wants to be able to take screenshot.

May be a boolean value, such as "`true`" or "`false`".

### android:description

```
android:description
```
Description of the accessibility service usage, availability, or limitations (e.g. isn't supported by all apps).

May be a reference to another resource, in the form "`@[+][package:]type/name`" or a theme attribute in the form "`?[package:]type/name`".

### android:htmlDescription

```
android:htmlDescription
```
Html description of the accessibility service usage, availability, or limitations (e.g. isn't supported by all apps).

May be a reference to another resource, in the form "`@[+][package:]type/name`" or a theme attribute in the form "`?[package:]type/name`".

### android:interactiveUiTimeout

```
android:interactiveUiTimeout
```
A recommended timeout in milliseconds used in `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.html#getRecommendedTimeoutMillis(kotlin.Int,%20kotlin.Int)` to return a suitable value for interactive controls. This setting can be changed at runtime by calling `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#setServiceInfo(android.accessibilityservice.AccessibilityServiceInfo)`.

May be an integer value, such as "`100`".

### android:intro

```
android:intro
```
Detailed intro of the accessibility service purpose or behavior.

May be a reference to another resource, in the form "`@[+][package:]type/name`" or a theme attribute in the form "`?[package:]type/name`".

### android:isAccessibilityTool

```
android:isAccessibilityTool
```
Attribute indicating whether the accessibility service is used to assist users with disabilities. This criteria might be defined by the installer. The default is false.

Note: If this flag is false, system will show a notification after a duration to inform the user about the privacy implications of the service.

May be a boolean value, such as "`true`" or "`false`".

### android:nonInteractiveUiTimeout

```
android:nonInteractiveUiTimeout
```
A recommended timeout in milliseconds used in `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.html#getRecommendedTimeoutMillis(kotlin.Int,%20kotlin.Int)` to return a suitable value for UIs that do not include interactive controls. This setting can be changed at runtime by calling `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#setServiceInfo(android.accessibilityservice.AccessibilityServiceInfo)`.

May be an integer value, such as "`100`".

### android:notificationTimeout

```
android:notificationTimeout
```
The minimal period in milliseconds between two accessibility events of the same type are sent to this service. This setting can be changed at runtime by calling `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#setServiceInfo(android.accessibilityservice.AccessibilityServiceInfo)`.

May be an integer value, such as "`100`".

### android:packageNames

```
android:packageNames
```
Comma separated package names from which this service would like to receive events (leave out for all packages). `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#setServiceInfo(android.accessibilityservice.AccessibilityServiceInfo)`.

May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character;

### android:settingsActivity

```
android:settingsActivity
```
Fully qualified class name of an activity that allows the user to modify the settings for this service. This setting cannot be changed at runtime.

May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character;

### android:summary

```
android:summary
```
Brief summary of the accessibility service purpose or behavior.

May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character;

### android:tileService

```
android:tileService
```
Fully qualified class name of `https://developer.android.com/reference/kotlin/android/service/quicksettings/TileService.html#` is associated with this accessibility service for one to one mapping. It is used by system settings to remind users this accessibility service has a `https://developer.android.com/reference/kotlin/android/service/quicksettings/TileService.html#`.

May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character;

## Constants

### CAPABILITY_CAN_CONTROL_MAGNIFICATION

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CAPABILITY_CAN_CONTROL_MAGNIFICATION: Int
```

Capability: This accessibility service can control display magnification.

 Value: 16

**See Also**

- `https://developer.android.com/reference/kotlin/android/R.styleable.html#AccessibilityService_canControlMagnification:kotlin.Int`

### CAPABILITY_CAN_PERFORM_GESTURES

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CAPABILITY_CAN_PERFORM_GESTURES: Int
```

Capability: This accessibility service can perform gestures.

 Value: 32

**See Also**

- `https://developer.android.com/reference/kotlin/android/R.styleable.html#AccessibilityService_canPerformGestures:kotlin.Int`

### CAPABILITY_CAN_REQUEST_ENHANCED_WEB_ACCESSIBILITY

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CAPABILITY_CAN_REQUEST_ENHANCED_WEB_ACCESSIBILITY: Int
```

**Deprecated:** *No longer used*

 Value: 4

### CAPABILITY_CAN_REQUEST_FILTER_KEY_EVENTS

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CAPABILITY_CAN_REQUEST_FILTER_KEY_EVENTS: Int
```

Capability: This accessibility service can request to filter the key event stream.

 Value: 8

**See Also**

- `https://developer.android.com/reference/kotlin/android/R.styleable.html#AccessibilityService_canRequestFilterKeyEvents:kotlin.Int`

### CAPABILITY_CAN_REQUEST_FINGERPRINT_GESTURES

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CAPABILITY_CAN_REQUEST_FINGERPRINT_GESTURES: Int
```

Capability: This accessibility service can capture gestures from the fingerprint sensor

 Value: 64

**See Also**

- `https://developer.android.com/reference/kotlin/android/R.styleable.html#AccessibilityService_canRequestFingerprintGestures:kotlin.Int`

### CAPABILITY_CAN_REQUEST_TOUCH_EXPLORATION

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CAPABILITY_CAN_REQUEST_TOUCH_EXPLORATION: Int
```

Capability: This accessibility service can request touch exploration mode in which touched items are spoken aloud and the UI can be explored via gestures.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/R.styleable.html#AccessibilityService_canRequestTouchExplorationMode:kotlin.Int`

### CAPABILITY_CAN_RETRIEVE_WINDOW_CONTENT

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CAPABILITY_CAN_RETRIEVE_WINDOW_CONTENT: Int
```

Capability: This accessibility service can retrieve the active window content.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/R.styleable.html#AccessibilityService_canRetrieveWindowContent:kotlin.Int`

### CAPABILITY_CAN_TAKE_SCREENSHOT

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CAPABILITY_CAN_TAKE_SCREENSHOT: Int
```

Capability: This accessibility service can take screenshot.

 Value: 128

**See Also**

- `https://developer.android.com/reference/kotlin/android/R.styleable.html#AccessibilityService_canTakeScreenshot:kotlin.Int`

### DEFAULT

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DEFAULT: Int
```

If an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService` is the default for a given type. Default service is invoked only if no package specific one exists. In case of more than one package specific service only the earlier registered is notified.

 Value: 1

### FEEDBACK_ALL_MASK

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEEDBACK_ALL_MASK: Int
```

Mask for all feedback types.

 Value: -1

**See Also**

- `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FEEDBACK_SPOKEN:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FEEDBACK_HAPTIC:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FEEDBACK_AUDIBLE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FEEDBACK_VISUAL:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FEEDBACK_GENERIC:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FEEDBACK_BRAILLE:kotlin.Int`

### FEEDBACK_AUDIBLE

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEEDBACK_AUDIBLE: Int
```

Denotes audible (not spoken) feedback.

 Value: 4

### FEEDBACK_BRAILLE

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEEDBACK_BRAILLE: Int
```

Denotes braille feedback.

 Value: 32

### FEEDBACK_GENERIC

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEEDBACK_GENERIC: Int
```

Denotes generic feedback.

 Value: 16

### FEEDBACK_HAPTIC

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEEDBACK_HAPTIC: Int
```

Denotes haptic feedback.

 Value: 2

### FEEDBACK_SPOKEN

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEEDBACK_SPOKEN: Int
```

Denotes spoken feedback.

 Value: 1

### FEEDBACK_VISUAL

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEEDBACK_VISUAL: Int
```

Denotes visual feedback.

 Value: 8

### FLAG_ENABLE_ACCESSIBILITY_VOLUME

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_ENABLE_ACCESSIBILITY_VOLUME: Int
```

This flag requests that all audio tracks system-wide with `https://developer.android.com/reference/kotlin/android/media/AudioAttributes.html#USAGE_ASSISTANCE_ACCESSIBILITY:kotlin.Int` be controlled by the `https://developer.android.com/reference/kotlin/android/media/AudioManager.html#STREAM_ACCESSIBILITY:kotlin.Int` volume.

 Value: 128

### FLAG_INCLUDE_NOT_IMPORTANT_VIEWS

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_INCLUDE_NOT_IMPORTANT_VIEWS: Int
```

If this flag is set the system will regard views that are not important for accessibility in addition to the ones that are important for accessibility. That is, views that are marked as not important for accessibility via `https://developer.android.com/reference/kotlin/android/view/View.html#IMPORTANT_FOR_ACCESSIBILITY_NO:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/View.html#IMPORTANT_FOR_ACCESSIBILITY_NO_HIDE_DESCENDANTS:kotlin.Int` and views that are marked as potentially important for accessibility via `https://developer.android.com/reference/kotlin/android/view/View.html#IMPORTANT_FOR_ACCESSIBILITY_AUTO:kotlin.Int` for which the system has determined that are not important for accessibility, are reported while querying the window content and also the accessibility service will receive accessibility events from them.

**Note:** For accessibility services targeting Android 4.1 (API level 16) or higher, this flag has to be explicitly set for the system to regard views that are not important for accessibility. For accessibility services targeting Android 4.0.4 (API level 15) or lower, this flag is ignored and all views are regarded for accessibility purposes.

Usually views not important for accessibility are layout managers that do not react to user actions, do not draw any content, and do not have any special semantics in the context of the screen content. For example, a three by three grid can be implemented as three horizontal linear layouts and one vertical, or three vertical linear layouts and one horizontal, or one grid layout, etc. In this context, the actual layout managers used to achieve the grid configuration are not important; rather it is important that there are nine evenly distributed elements.

 Value: 2

### FLAG_INPUT_METHOD_EDITOR

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_INPUT_METHOD_EDITOR: Int
```

This flag makes the AccessibilityService an input method editor with a subset of input method editor capabilities: get the `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection.html#` and get text selection change notifications.

 Value: 32768

**See Also**

- `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#getInputMethod()`

### FLAG_REPORT_VIEW_IDS

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_REPORT_VIEW_IDS: Int
```

This flag requests that the `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.html#`s obtained by an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService` contain the id of the source view. The source view id will be a fully qualified resource name of the form "package:id/name", for example "foo.bar:id/my_list", and it is useful for UI test automation. This flag is not set by default.

 Value: 16

### FLAG_REQUEST_2_FINGER_PASSTHROUGH

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_REQUEST_2_FINGER_PASSTHROUGH: Int
```

This flag requests that when `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FLAG_REQUEST_MULTI_FINGER_GESTURES:kotlin.Int` is enabled, two-finger passthrough gestures are re-enabled. Two-finger swipe gestures are not detected, but instead passed through as one-finger gestures. In addition, three-finger swipes from the bottom of the screen are not detected, and instead are passed through unchanged. If `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FLAG_REQUEST_MULTI_FINGER_GESTURES:kotlin.Int` is disabled this flag has no effect.

 Value: 8192

**See Also**

- `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FLAG_REQUEST_TOUCH_EXPLORATION_MODE:kotlin.Int`

### FLAG_REQUEST_ACCESSIBILITY_BUTTON

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_REQUEST_ACCESSIBILITY_BUTTON: Int
```

This flag indicates to the system that the accessibility service requests that an accessibility button be shown within the system's navigation area, if available.

**Note:** For accessibility services targeting APIs greater than `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int`, this flag must be specified in the accessibility service metadata file. Otherwise, it will be ignored.

 Value: 256

### FLAG_REQUEST_ENHANCED_WEB_ACCESSIBILITY

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_REQUEST_ENHANCED_WEB_ACCESSIBILITY: Int
```

**Deprecated:** *No longer used*

 Value: 8

### FLAG_REQUEST_FILTER_KEY_EVENTS

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_REQUEST_FILTER_KEY_EVENTS: Int
```

This flag requests from the system to filter key events. If this flag is set the accessibility service will receive the key events before applications allowing it implement global shortcuts.

Services that want to set this flag have to declare this capability in their meta-data by setting the attribute `https://developer.android.com/reference/kotlin/android/R.attr.html#` to true, otherwise this flag will be ignored. For how to declare the meta-data of a service refer to {@value AccessibilityService#SERVICE_META_DATA}.

 Value: 32

**See Also**

- `https://developer.android.com/reference/kotlin/android/R.styleable.html#AccessibilityService_canRequestFilterKeyEvents:kotlin.Int`

### FLAG_REQUEST_FINGERPRINT_GESTURES

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_REQUEST_FINGERPRINT_GESTURES: Int
```

This flag requests that all fingerprint gestures be sent to the accessibility service.

Services that want to set this flag have to declare the capability to retrieve window content in their meta-data by setting the attribute `https://developer.android.com/reference/kotlin/android/R.attr.html#canRequestFingerprintGestures:kotlin.Int` to true, otherwise this flag will be ignored. For how to declare the meta-data of a service refer to {@value AccessibilityService#SERVICE_META_DATA}.

 Value: 512

**See Also**

- `https://developer.android.com/reference/kotlin/android/R.styleable.html#AccessibilityService_canRequestFingerprintGestures:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#getFingerprintGestureController()`

### FLAG_REQUEST_MULTI_FINGER_GESTURES

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_REQUEST_MULTI_FINGER_GESTURES: Int
```

This flag requests that when `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FLAG_REQUEST_TOUCH_EXPLORATION_MODE:kotlin.Int` is enabled, multi-finger gestures are also enabled. As a consequence, two-finger bypass gestures will be disabled. If `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FLAG_REQUEST_TOUCH_EXPLORATION_MODE:kotlin.Int` is disabled this flag has no effect.

 Value: 4096

**See Also**

- `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FLAG_REQUEST_TOUCH_EXPLORATION_MODE:kotlin.Int`

### FLAG_REQUEST_SHORTCUT_WARNING_DIALOG_SPOKEN_FEEDBACK

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_REQUEST_SHORTCUT_WARNING_DIALOG_SPOKEN_FEEDBACK: Int
```

This flag requests that accessibility shortcut warning dialog has spoken feedback when dialog is shown.

 Value: 1024

### FLAG_REQUEST_TOUCH_EXPLORATION_MODE

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_REQUEST_TOUCH_EXPLORATION_MODE: Int
```

This flag requests that the system gets into touch exploration mode. In this mode a single finger moving on the screen behaves as a mouse pointer hovering over the user interface. The system will also detect certain gestures performed on the touch screen and notify this service. The system will enable touch exploration mode if there is at least one accessibility service that has this flag set. Hence, clearing this flag does not guarantee that the device will not be in touch exploration mode since there may be another enabled service that requested it.

For accessibility services targeting Android 4.3 (API level 18) or higher that want to set this flag have to declare this capability in their meta-data by setting the attribute `https://developer.android.com/reference/kotlin/android/R.attr.html#canRequestTouchExplorationMode:kotlin.Int` to true. Otherwise, this flag will be ignored. For how to declare the meta-data of a service refer to {@value AccessibilityService#SERVICE_META_DATA}.

Services targeting Android 4.2.2 (API level 17) or lower will work normally. In other words, the first time they are run, if this flag is specified, a dialog is shown to the user to confirm enabling explore by touch.

 Value: 4

**See Also**

- `https://developer.android.com/reference/kotlin/android/R.styleable.html#AccessibilityService_canRequestTouchExplorationMode:kotlin.Int`

### FLAG_RETRIEVE_INTERACTIVE_WINDOWS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_RETRIEVE_INTERACTIVE_WINDOWS: Int
```

This flag indicates to the system that the accessibility service wants to access content of all interactive windows. An interactive window is a window that has input focus or can be touched by a sighted user when explore by touch is not enabled. If this flag is not set your service will not receive `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#TYPE_WINDOWS_CHANGED:kotlin.Int` events, calling AccessibilityService`https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#getWindows()` will return an empty list, and `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo.html#getWindow()` will return null.

Services that want to set this flag have to declare the capability to retrieve window content in their meta-data by setting the attribute `https://developer.android.com/reference/kotlin/android/R.attr.html#canRetrieveWindowContent:kotlin.Int` to true, otherwise this flag will be ignored. For how to declare the meta-data of a service refer to {@value AccessibilityService#SERVICE_META_DATA}.

 Value: 64

**See Also**

- `https://developer.android.com/reference/kotlin/android/R.styleable.html#AccessibilityService_canRetrieveWindowContent:kotlin.Int`

### FLAG_SEND_MOTION_EVENTS

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_SEND_MOTION_EVENTS: Int
```

This flag requests that when `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FLAG_REQUEST_TOUCH_EXPLORATION_MODE:kotlin.Int` is enabled, a service will receive the motion events for each successfully-detected gesture. The service will also receive an AccessibilityGestureEvent of type GESTURE_INVALID for each cancelled gesture along with its motion events. A service will receive a gesture of type GESTURE_PASSTHROUGH and accompanying motion events for every passthrough gesture that does not start gesture detection. This information can be used to collect instances of improper gesture detection behavior and relay that information to framework developers. If `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FLAG_REQUEST_TOUCH_EXPLORATION_MODE:kotlin.Int` is disabled this flag has no effect.

 Value: 16384

**See Also**

- `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FLAG_REQUEST_TOUCH_EXPLORATION_MODE:kotlin.Int`

### FLAG_SERVICE_HANDLES_DOUBLE_TAP

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_SERVICE_HANDLES_DOUBLE_TAP: Int
```

This flag requests that when `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FLAG_REQUEST_TOUCH_EXPLORATION_MODE:kotlin.Int` is enabled, double tap and double tap and hold gestures are dispatched to the service rather than being handled by the framework. If `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FLAG_REQUEST_TOUCH_EXPLORATION_MODE:kotlin.Int` is disabled this flag has no effect.

 Value: 2048

**See Also**

- `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FLAG_REQUEST_TOUCH_EXPLORATION_MODE:kotlin.Int`

## Public constructors

### AccessibilityServiceInfo

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
AccessibilityServiceInfo()
```

Creates a new instance.

## Public methods

### capabilityToString

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun capabilityToString(capability: Int): String!
```

Returns the string representation of a capability. For example, `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#CAPABILITY_CAN_RETRIEVE_WINDOW_CONTENT:kotlin.Int` is represented by the string CAPABILITY_CAN_RETRIEVE_WINDOW_CONTENT.

| Parameters ||
|---|---|
| `capability` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The capability. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | The string representation. |

### describeContents

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### equals

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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
| `obj` | This value may be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

### feedbackTypeToString

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun feedbackTypeToString(feedbackType: Int): String!
```

Returns the string representation of a feedback type. For example, `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FEEDBACK_SPOKEN:kotlin.Int` is represented by the string FEEDBACK_SPOKEN.

| Parameters ||
|---|---|
| `feedbackType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The feedback type. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | The string representation. |

### flagToString

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun flagToString(flag: Int): String!
```

Returns the string representation of a flag. For example, `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#DEFAULT:kotlin.Int` is represented by the string DEFAULT.

| Parameters ||
|---|---|
| `flag` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The flag. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | The string representation. |

### getCanRetrieveWindowContent

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCanRetrieveWindowContent(): Boolean
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#getCapabilities()`.*

Whether this service can retrieve the current window's content.

**Statically set from `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#SERVICE_META_DATA:kotlin.String`.**

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if window content can be retrieved. |

### getCapabilities

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCapabilities(): Int
```

Returns the bit mask of capabilities this accessibility service has such as being able to retrieve the active window content, etc.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The capability bit mask. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#CAPABILITY_CAN_RETRIEVE_WINDOW_CONTENT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#CAPABILITY_CAN_REQUEST_TOUCH_EXPLORATION:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#CAPABILITY_CAN_REQUEST_FILTER_KEY_EVENTS:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#CAPABILITY_CAN_CONTROL_MAGNIFICATION:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#CAPABILITY_CAN_PERFORM_GESTURES:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#CAPABILITY_CAN_TAKE_SCREENSHOT:kotlin.Int`

### getDescription

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDescription(): String!
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#loadDescription(android.content.pm.PackageManager)`.*

Gets the non-localized description of the accessibility service.

**Statically set from `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#SERVICE_META_DATA:kotlin.String`.**

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | The description. |

### getId

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getId(): String!
```

The accessibility service id.

**Generated by the system.**

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | The id (or `null` if the component is not set yet). |

### getInteractiveUiTimeoutMillis

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getInteractiveUiTimeoutMillis(): Int
```

Get the recommended timeout for interactive controls.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The timeout in milliseconds. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#setInteractiveUiTimeoutMillis(kotlin.Int)`

### getMotionEventSources

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMotionEventSources(): Int
```

Returns the bit mask of `https://developer.android.com/reference/kotlin/android/view/InputDevice.html#` sources that the accessibility service wants to listen to for generic `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#`s.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/view/InputDevice.html#SOURCE_MOUSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/InputDevice.html#SOURCE_STYLUS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/InputDevice.html#SOURCE_BLUETOOTH_STYLUS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/InputDevice.html#SOURCE_TRACKBALL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/InputDevice.html#SOURCE_MOUSE_RELATIVE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/InputDevice.html#SOURCE_TOUCHPAD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/InputDevice.html#SOURCE_TOUCH_NAVIGATION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/InputDevice.html#SOURCE_ROTARY_ENCODER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/InputDevice.html#SOURCE_JOYSTICK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/InputDevice.html#SOURCE_SENSOR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/InputDevice.html#SOURCE_TOUCHSCREEN:kotlin.Int` |

### getNonInteractiveUiTimeoutMillis

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getNonInteractiveUiTimeoutMillis(): Int
```

Get the recommended timeout for non-interactive controls.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The timeout in milliseconds. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#setNonInteractiveUiTimeoutMillis(kotlin.Int)`

### getResolveInfo

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getResolveInfo(): ResolveInfo!
```

The service `https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo.html#`.

**Generated by the system.**

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo.html#!` | The info. |

### getSettingsActivityName

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSettingsActivityName(): String!
```

The settings activity name.

**Statically set from `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#SERVICE_META_DATA:kotlin.String`.**

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | The settings activity name. |

### getTileServiceName

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTileServiceName(): String?
```

Gets the name of `https://developer.android.com/reference/kotlin/android/service/quicksettings/TileService.html#` is associated with this accessibility service.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | The name of `https://developer.android.com/reference/kotlin/android/service/quicksettings/TileService.html#`. This value may be `null`. |

### hashCode

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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

### isAccessibilityTool

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isAccessibilityTool(): Boolean
```

Indicates if the service is used to assist users with disabilities.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the property is set to true. |

### loadDescription

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun loadDescription(packageManager: PackageManager!): String!
```

The localized description of the accessibility service.

**Statically set from `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#SERVICE_META_DATA:kotlin.String`.**

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | The localized description. |

### loadIntro

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun loadIntro(packageManager: PackageManager): CharSequence?
```

The localized intro of the accessibility service.

**Statically set from `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#SERVICE_META_DATA:kotlin.String`.**

| Parameters ||
|---|---|
| `packageManager` | [PackageManager](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?` | The localized intro if available, and `null` if a intro has not been provided. |

### loadSummary

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun loadSummary(packageManager: PackageManager!): CharSequence!
```

The localized summary of the accessibility service.

**Statically set from `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#SERVICE_META_DATA:kotlin.String`.**

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!` | The localized summary if available, and `null` if a summary has not been provided. |

### setInteractiveUiTimeoutMillis

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setInteractiveUiTimeoutMillis(timeout: Int): Unit
```

Set the recommended time that interactive controls need to remain on the screen to support the user.

**This value can be dynamically set at runtime by `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#setServiceInfo(android.accessibilityservice.AccessibilityServiceInfo)`.**

| Parameters ||
|---|---|
| `timeout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The timeout in milliseconds. Value is 0 or greater |

**See Also**

- `https://developer.android.com/reference/kotlin/android/R.styleable.html#AccessibilityService_interactiveUiTimeout:kotlin.Int`

### setMotionEventSources

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setMotionEventSources(motionEventSources: Int): Unit
```

Sets the bit mask of `https://developer.android.com/reference/kotlin/android/view/InputDevice.html#` sources that the accessibility service wants to listen to for generic `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#`s.

Including an `https://developer.android.com/reference/kotlin/android/view/InputDevice.html#` source that does not send `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#`s is effectively a no-op for that source, since you will not receive any events from that source.

See `https://developer.android.com/reference/kotlin/android/view/InputDevice.html#` for complete source definitions. Many input devices send `https://developer.android.com/reference/kotlin/android/view/InputEvent.html#`s from more than one type of source so you may need to include multiple `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#` sources here, in addition to using `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#onKeyEvent(android.view.KeyEvent)` to listen to `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#`s.

**Note:** `https://developer.android.com/reference/kotlin/android/view/InputDevice.html#` sources contain source class bits that complicate bitwise flag removal operations. To remove a specific source you should rebuild the entire value using bitwise OR operations on the individual source constants.

| Parameters ||
|---|---|
| `motionEventSources` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): A bit mask of `https://developer.android.com/reference/kotlin/android/view/InputDevice.html#` sources. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/view/InputDevice.html#SOURCE_MOUSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/InputDevice.html#SOURCE_STYLUS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/InputDevice.html#SOURCE_BLUETOOTH_STYLUS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/InputDevice.html#SOURCE_TRACKBALL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/InputDevice.html#SOURCE_MOUSE_RELATIVE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/InputDevice.html#SOURCE_TOUCHPAD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/InputDevice.html#SOURCE_TOUCH_NAVIGATION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/InputDevice.html#SOURCE_ROTARY_ENCODER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/InputDevice.html#SOURCE_JOYSTICK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/InputDevice.html#SOURCE_SENSOR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/InputDevice.html#SOURCE_TOUCHSCREEN:kotlin.Int` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#onMotionEvent(android.view.MotionEvent)`

### setNonInteractiveUiTimeoutMillis

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setNonInteractiveUiTimeoutMillis(timeout: Int): Unit
```

Set the recommended time that non-interactive controls need to remain on the screen to support the user.

**This value can be dynamically set at runtime by `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#setServiceInfo(android.accessibilityservice.AccessibilityServiceInfo)`.**

| Parameters ||
|---|---|
| `timeout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The timeout in milliseconds. Value is 0 or greater |

**See Also**

- `https://developer.android.com/reference/kotlin/android/R.styleable.html#AccessibilityService_nonInteractiveUiTimeout:kotlin.Int`

### toString

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun writeToParcel(
    parcel: Parcel, 
    flagz: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<AccessibilityServiceInfo!>
```
**See Also**

- `https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#`

### eventTypes

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var eventTypes: Int
```

The event types an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService` is interested in.

**Can be dynamically set at runtime.**
**See Also**

- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#TYPE_VIEW_CLICKED:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#TYPE_VIEW_LONG_CLICKED:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#TYPE_VIEW_FOCUSED:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#TYPE_VIEW_SELECTED:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#TYPE_VIEW_TEXT_CHANGED:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#TYPE_WINDOW_STATE_CHANGED:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#TYPE_NOTIFICATION_STATE_CHANGED:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#TYPE_TOUCH_EXPLORATION_GESTURE_START:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#TYPE_TOUCH_EXPLORATION_GESTURE_END:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#TYPE_VIEW_HOVER_ENTER:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#TYPE_VIEW_HOVER_EXIT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#TYPE_VIEW_SCROLLED:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#TYPE_VIEW_TEXT_SELECTION_CHANGED:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#TYPE_WINDOW_CONTENT_CHANGED:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#TYPE_TOUCH_INTERACTION_START:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#TYPE_TOUCH_INTERACTION_END:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#TYPE_ANNOUNCEMENT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#TYPE_GESTURE_DETECTION_START:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#TYPE_GESTURE_DETECTION_END:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#TYPE_VIEW_ACCESSIBILITY_FOCUSED:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#TYPE_VIEW_ACCESSIBILITY_FOCUS_CLEARED:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#TYPE_VIEW_TEXT_TRAVERSED_AT_MOVEMENT_GRANULARITY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent.html#TYPE_WINDOWS_CHANGED:kotlin.Int`

### feedbackType

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var feedbackType: Int
```

The feedback type an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService` provides.

**Can be dynamically set at runtime.**
. 
Value is either `0` or a combination of the following:

- `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FEEDBACK_AUDIBLE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FEEDBACK_GENERIC:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FEEDBACK_HAPTIC:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FEEDBACK_SPOKEN:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FEEDBACK_VISUAL:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FEEDBACK_BRAILLE:kotlin.Int`

**See Also**

- `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FEEDBACK_AUDIBLE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FEEDBACK_GENERIC:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FEEDBACK_HAPTIC:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FEEDBACK_SPOKEN:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FEEDBACK_VISUAL:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FEEDBACK_BRAILLE:kotlin.Int`

### flags

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var flags: Int
```

This field represents a set of flags used for configuring an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService`.

**Can be dynamically set at runtime.**

**Note:** Accessibility services with targetSdkVersion greater than `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int` cannot dynamically set the `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FLAG_REQUEST_ACCESSIBILITY_BUTTON:kotlin.Int` at runtime. It must be specified in the accessibility service metadata file.
**See Also**

- `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#DEFAULT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FLAG_INCLUDE_NOT_IMPORTANT_VIEWS:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FLAG_REQUEST_TOUCH_EXPLORATION_MODE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FLAG_REQUEST_ENHANCED_WEB_ACCESSIBILITY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FLAG_REQUEST_FILTER_KEY_EVENTS:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FLAG_REPORT_VIEW_IDS:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FLAG_RETRIEVE_INTERACTIVE_WINDOWS:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FLAG_ENABLE_ACCESSIBILITY_VOLUME:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FLAG_REQUEST_ACCESSIBILITY_BUTTON:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FLAG_REQUEST_SHORTCUT_WARNING_DIALOG_SPOKEN_FEEDBACK:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FLAG_INPUT_METHOD_EDITOR:kotlin.Int`

### notificationTimeout

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var notificationTimeout: Long
```

The timeout, in milliseconds, after the most recent event of a given type before an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService` is notified.

**Can be dynamically set at runtime.**

**Note:** The event notification timeout is useful to avoid propagating events to the client too frequently since this is accomplished via an expensive interprocess call. One can think of the timeout as a criteria to determine when event generation has settled down.

### packageNames

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var packageNames: Array<String!>!
```

The package names an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService` is interested in. Setting to `null` is equivalent to all packages.

**Can be dynamically set at runtime.**
