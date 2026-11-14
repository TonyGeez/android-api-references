# android.accessibilityservice

# android.accessibilityservice

Kotlin| [Java](_package.md)
| --- | --- |

## Interfaces

| [TakeScreenshotCallback](../android/accessibilityservice/AccessibilityService.TakeScreenshotCallback.md) | Interface used to report status of taking screenshot. |
| --- | --- |
| [BrailleDisplayController](BrailleDisplayController.md) | Used to communicate with a Braille display that supports the Braille display HID standard (usage page 0x41). |
| [Callback](../android/accessibilityservice/TouchInteractionController.Callback.md) | callbacks allow services to receive motion events and state change updates. |

## Classes

| [AccessibilityButtonController](AccessibilityButtonController.md) | Controller for the accessibility button within the system's navigation area |
| --- | --- |
| [AccessibilityGestureEvent](AccessibilityGestureEvent.md) | This class describes the gesture event including gesture id and which display it happens on. |
| [AccessibilityService](AccessibilityService.md) | Accessibility services should only be used to assist users with disabilities in using Android devices and apps. |
| [AccessibilityServiceInfo](AccessibilityServiceInfo.md) | This class describes an [AccessibilityService](AccessibilityService.md). |
| --- | --- |
| [FingerprintGestureController](FingerprintGestureController.md) | An [AccessibilityService](AccessibilityService.md) can capture gestures performed on a device's fingerprint sensor, as long as the device has a sensor capable of detecting gestures. |
| [GestureDescription](GestureDescription.md) | Accessibility services with the [android.R.styleable#AccessibilityService_canPerformGestures](../android/R.styleable.md) property can dispatch gestures. |
| [InputMethod](InputMethod.md) | This class provides input method APIs. |
| --- | --- |
| [MagnificationConfig](MagnificationConfig.md) | This class describes the magnification config for [AccessibilityService](AccessibilityService.md) to control the magnification. |
| [TouchInteractionController](TouchInteractionController.md) | This class allows a service to handle touch exploration and the detection of specialized accessibility gestures. |
