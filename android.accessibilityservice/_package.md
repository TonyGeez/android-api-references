# android.accessibilityservice

# android.accessibilityservice

Kotlin| [Java](https://developer.android.com/reference/android/accessibilityservice/package-summary "View this page in Java")

## Interfaces

| [TakeScreenshotCallback](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.TakeScreenshotCallback) | Interface used to report status of taking screenshot. |
| [BrailleDisplayController](https://developer.android.com/reference/kotlin/android/accessibilityservice/BrailleDisplayController) | Used to communicate with a Braille display that supports the Braille display HID standard (usage page 0x41). |
| [Callback](https://developer.android.com/reference/kotlin/android/accessibilityservice/TouchInteractionController.Callback) | callbacks allow services to receive motion events and state change updates. |

## Classes

| [AccessibilityButtonController](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityButtonController) | Controller for the accessibility button within the system's navigation area |
| [AccessibilityGestureEvent](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityGestureEvent) | This class describes the gesture event including gesture id and which display it happens on. |
| [AccessibilityService](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService) | Accessibility services should only be used to assist users with disabilities in using Android devices and apps. |
| [AccessibilityServiceInfo](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo) | This class describes an [AccessibilityService](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService). |
| [FingerprintGestureController](https://developer.android.com/reference/kotlin/android/accessibilityservice/FingerprintGestureController) | An [AccessibilityService](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService) can capture gestures performed on a device's fingerprint sensor, as long as the device has a sensor capable of detecting gestures. |
| [GestureDescription](https://developer.android.com/reference/kotlin/android/accessibilityservice/GestureDescription) | Accessibility services with the [android.R.styleable#AccessibilityService_canPerformGestures](https://developer.android.com/reference/kotlin/android/R.styleable.html#AccessibilityService_canPerformGestures:kotlin.Int) property can dispatch gestures. |
| [InputMethod](https://developer.android.com/reference/kotlin/android/accessibilityservice/InputMethod) | This class provides input method APIs. |
| [MagnificationConfig](https://developer.android.com/reference/kotlin/android/accessibilityservice/MagnificationConfig) | This class describes the magnification config for [AccessibilityService](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService) to control the magnification. |
| [TouchInteractionController](https://developer.android.com/reference/kotlin/android/accessibilityservice/TouchInteractionController) | This class allows a service to handle touch exploration and the detection of specialized accessibility gestures. |
