# android.accessibilityservice

# android.accessibilityservice

Kotlin| [Java](../android/accessibilityservice/_package.md)
| --- | --- |

## Interfaces

| [TakeScreenshotCallback](../android/accessibilityservice/AccessibilityService.TakeScreenshotCallback.md) | Interface used to report status of taking screenshot. |
| --- | --- |
| [BrailleDisplayController](../android/accessibilityservice/BrailleDisplayController.md) | Used to communicate with a Braille display that supports the Braille display HID standard (usage page 0x41). |
| [Callback](../android/accessibilityservice/TouchInteractionController.Callback.md) | callbacks allow services to receive motion events and state change updates. |

## Classes

| [AccessibilityButtonController](../android/accessibilityservice/AccessibilityButtonController.md) | Controller for the accessibility button within the system's navigation area |
| --- | --- |
| [AccessibilityGestureEvent](../android/accessibilityservice/AccessibilityGestureEvent.md) | This class describes the gesture event including gesture id and which display it happens on. |
| [AccessibilityService](../android/accessibilityservice/AccessibilityService.md) | Accessibility services should only be used to assist users with disabilities in using Android devices and apps. |
| [AccessibilityServiceInfo](../android/accessibilityservice/AccessibilityServiceInfo.md) | This class describes an [AccessibilityService](../android/accessibilityservice/AccessibilityService.md). |
| --- | --- |
| [FingerprintGestureController](../android/accessibilityservice/FingerprintGestureController.md) | An [AccessibilityService](../android/accessibilityservice/AccessibilityService.md) can capture gestures performed on a device's fingerprint sensor, as long as the device has a sensor capable of detecting gestures. |
| [GestureDescription](../android/accessibilityservice/GestureDescription.md) | Accessibility services with the [android.R.styleable#AccessibilityService_canPerformGestures](../android/R.styleable.md) property can dispatch gestures. |
| [InputMethod](../android/accessibilityservice/InputMethod.md) | This class provides input method APIs. |
| --- | --- |
| [MagnificationConfig](../android/accessibilityservice/MagnificationConfig.md) | This class describes the magnification config for [AccessibilityService](../android/accessibilityservice/AccessibilityService.md) to control the magnification. |
| [TouchInteractionController](../android/accessibilityservice/TouchInteractionController.md) | This class allows a service to handle touch exploration and the detection of specialized accessibility gestures. |
