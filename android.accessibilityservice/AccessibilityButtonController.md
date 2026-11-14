Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AccessibilityButtonController

Kotlin | [Java](https://developer.android.com/reference/android/accessibilityservice/AccessibilityButtonController "View this page in Java")
| --- | --- |

```
class AccessibilityButtonController
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.accessibilityservice.AccessibilityButtonController](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityButtonController#) |

Controller for the accessibility button within the system's navigation area

This class may be used to query the accessibility button's state and register callbacks for interactions with and state changes to the accessibility button when `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FLAG_REQUEST_ACCESSIBILITY_BUTTON:kotlin.Int` is set.

**Note:** This class and `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FLAG_REQUEST_ACCESSIBILITY_BUTTON:kotlin.Int` should not be used as the sole means for offering functionality to users via an `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService`. Some device implementations may choose not to provide a software-rendered system navigation area, making this affordance permanently unavailable.

**Note:** On device implementations where the accessibility button is supported, it may not be available at all times, such as when a foreground application uses `https://developer.android.com/reference/kotlin/android/view/View.html#SYSTEM_UI_FLAG_HIDE_NAVIGATION:kotlin.Int`. A user may also choose to assign this button to another accessibility service or feature. In each of these cases, a registered `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityButtonController.AccessibilityButtonCallback`'s `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityButtonController.AccessibilityButtonCallback#onAvailabilityChanged(android.accessibilityservice.AccessibilityButtonController,%20kotlin.Boolean)` method will be invoked to provide notifications of changes in the accessibility button's availability to the registering service.

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityButtonController.AccessibilityButtonCallback` Callback for interaction with and changes to state of the accessibility button within the system's navigation area. |

| Public methods ||
|---|---|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityButtonController#isAccessibilityButtonAvailable()()` Retrieves whether the accessibility button in the system's navigation area is available to the calling service. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityButtonController#registerAccessibilityButtonCallback(android.accessibilityservice.AccessibilityButtonController.AccessibilityButtonCallback)(callback: https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityButtonController.AccessibilityButtonCallback)` Registers the provided `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityButtonController.AccessibilityButtonCallback` for interaction and state changes callbacks related to the accessibility button. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityButtonController#registerAccessibilityButtonCallback(android.accessibilityservice.AccessibilityButtonController.AccessibilityButtonCallback,%20android.os.Handler)(callback: https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityButtonController.AccessibilityButtonCallback, handler: https://developer.android.com/reference/kotlin/android/os/Handler.html#)` Registers the provided `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityButtonController.AccessibilityButtonCallback` for interaction and state change callbacks related to the accessibility button. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityButtonController#unregisterAccessibilityButtonCallback(android.accessibilityservice.AccessibilityButtonController.AccessibilityButtonCallback)(callback: https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityButtonController.AccessibilityButtonCallback)` Unregisters the provided `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityButtonController.AccessibilityButtonCallback` for interaction and state change callbacks related to the accessibility button. |

## Public methods

### isAccessibilityButtonAvailable

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isAccessibilityButtonAvailable(): Boolean
```

Retrieves whether the accessibility button in the system's navigation area is available to the calling service.

**Note:** If the service is not yet connected (e.g. `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#onServiceConnected()` has not yet been called) or the service has been disconnected, this method will have no effect and return `false`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the accessibility button in the system's navigation area is available to the calling service, `false` otherwise |

### registerAccessibilityButtonCallback

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun registerAccessibilityButtonCallback(callback: AccessibilityButtonController.AccessibilityButtonCallback): Unit
```

Registers the provided `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityButtonController.AccessibilityButtonCallback` for interaction and state changes callbacks related to the accessibility button.

| Parameters ||
|---|---|
| `callback` | [AccessibilityButtonController.AccessibilityButtonCallback](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityButtonController.AccessibilityButtonCallback): the callback to add, must be non-null |

### registerAccessibilityButtonCallback

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun registerAccessibilityButtonCallback(
    callback: AccessibilityButtonController.AccessibilityButtonCallback, 
    handler: Handler
): Unit
```

Registers the provided `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityButtonController.AccessibilityButtonCallback` for interaction and state change callbacks related to the accessibility button. The callback will occur on the specified `https://developer.android.com/reference/kotlin/android/os/Handler.html#`'s thread, or on the services's main thread if the handler is `null`.

| Parameters ||
|---|---|
| `callback` | [AccessibilityButtonController.AccessibilityButtonCallback](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityButtonController.AccessibilityButtonCallback): the callback to add, must be non-null |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#): the handler on which the callback should execute, must be non-null |

### unregisterAccessibilityButtonCallback

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun unregisterAccessibilityButtonCallback(callback: AccessibilityButtonController.AccessibilityButtonCallback): Unit
```

Unregisters the provided `https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityButtonController.AccessibilityButtonCallback` for interaction and state change callbacks related to the accessibility button.

| Parameters ||
|---|---|
| `callback` | [AccessibilityButtonController.AccessibilityButtonCallback](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityButtonController.AccessibilityButtonCallback): the callback to remove, must be non-null |
