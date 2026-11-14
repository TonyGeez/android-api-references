# FingerprintGestureController

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FingerprintGestureController

Kotlin| [Java](../android/accessibilityservice/FingerprintGestureController.md) 
| --- | --- |

```
class FingerprintGestureController
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.accessibilityservice.FingerprintGestureController](../android/accessibilityservice/FingerprintGestureController.md) |

An [AccessibilityService](../android/accessibilityservice/AccessibilityService.md) can capture gestures performed on a device's fingerprint sensor, as long as the device has a sensor capable of detecting gestures.

This capability must be declared by the service as [AccessibilityServiceInfo.CAPABILITY_CAN_REQUEST_FINGERPRINT_GESTURES](../android/accessibilityservice/AccessibilityServiceInfo.md). It also requires the permission [android.Manifest.permission#USE_FINGERPRINT](../android/Manifest.permission.md).

Because capturing fingerprint gestures may have side effects, services with the capability only capture gestures when [AccessibilityServiceInfo.FLAG_REQUEST_FINGERPRINT_GESTURES](../android/accessibilityservice/AccessibilityServiceInfo.md) is set.

**Note:** The fingerprint sensor is used for authentication in critical use cases, so services must carefully design their user's experience when performing gestures on the sensor. When the sensor is in use by an app, for example, when authenticating or enrolling a user, the sensor will not detect gestures. Services need to ensure that users understand when the sensor is in-use for authentication to prevent users from authenticating unintentionally when trying to interact with the service. They can use [FingerprintGestureCallback.onGestureDetectionAvailabilityChanged(boolean)](../android/accessibilityservice/FingerprintGestureController.FingerprintGestureCallback.md))to learn when gesture detection becomes unavailable.

Multiple accessibility services may listen for fingerprint gestures simultaneously, so services should provide a way for the user to disable the use of this feature so multiple services don't conflict with each other.

{@see android.hardware.fingerprint.FingerprintManager#isHardwareDetected}

## Summary

| Nested classes ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [FingerprintGestureCallback](../android/accessibilityservice/FingerprintGestureController.FingerprintGestureCallback.md) Class that is called back when fingerprint gestures are being used for accessibility. |

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FINGERPRINT_GESTURE_SWIPE_DOWN](../android/accessibilityservice/FingerprintGestureController.md) Identifier for a swipe down on the fingerprint sensor |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FINGERPRINT_GESTURE_SWIPE_LEFT](../android/accessibilityservice/FingerprintGestureController.md) Identifier for a swipe left on the fingerprint sensor |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FINGERPRINT_GESTURE_SWIPE_RIGHT](../android/accessibilityservice/FingerprintGestureController.md) Identifier for a swipe right on the fingerprint sensor |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FINGERPRINT_GESTURE_SWIPE_UP](../android/accessibilityservice/FingerprintGestureController.md) Identifier for a swipe up on the fingerprint sensor |

| Public methods ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isGestureDetectionAvailable](../android/accessibilityservice/FingerprintGestureController.md))`()` Gets if the fingerprint sensor's gesture detection is available. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerFingerprintGestureCallback](../android/accessibilityservice/FingerprintGestureController.md))`(`callback:` ` [FingerprintGestureController.FingerprintGestureCallback](../android/accessibilityservice/FingerprintGestureController.FingerprintGestureCallback.md)`, `handler:` ` [Handler](../android/os/Handler.md)?`)` Register a callback to be informed of fingerprint sensor gesture events. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterFingerprintGestureCallback](../android/accessibilityservice/FingerprintGestureController.md))`(`callback:` ` [FingerprintGestureController.FingerprintGestureCallback](../android/accessibilityservice/FingerprintGestureController.FingerprintGestureCallback.md)!`)` Unregister a listener added with [registerFingerprintGestureCallback](../android/accessibilityservice/FingerprintGestureController.md)). |
| --- | --- |

## Constants

### FINGERPRINT_GESTURE_SWIPE_DOWN

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FINGERPRINT_GESTURE_SWIPE_DOWN: Int
```

Identifier for a swipe down on the fingerprint sensor 

 Value: 8

### FINGERPRINT_GESTURE_SWIPE_LEFT

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FINGERPRINT_GESTURE_SWIPE_LEFT: Int
```

Identifier for a swipe left on the fingerprint sensor 

 Value: 2

### FINGERPRINT_GESTURE_SWIPE_RIGHT

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FINGERPRINT_GESTURE_SWIPE_RIGHT: Int
```

Identifier for a swipe right on the fingerprint sensor 

 Value: 1

### FINGERPRINT_GESTURE_SWIPE_UP

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FINGERPRINT_GESTURE_SWIPE_UP: Int
```

Identifier for a swipe up on the fingerprint sensor 

 Value: 4

## Public methods

### isGestureDetectionAvailable

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isGestureDetectionAvailable(): Boolean
```

Gets if the fingerprint sensor's gesture detection is available.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the sensor's gesture detection is available.`false`if it is not currently detecting gestures (for example, if it is enrolling a finger). |

### registerFingerprintGestureCallback

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun registerFingerprintGestureCallback(
    callback: FingerprintGestureController.FingerprintGestureCallback, 
    handler: Handler?
): Unit
```

Register a callback to be informed of fingerprint sensor gesture events.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [FingerprintGestureController.FingerprintGestureCallback](../android/accessibilityservice/FingerprintGestureController.FingerprintGestureCallback.md):The listener to be added. This value cannot be`null`. |
| `handler` | [Handler](../android/os/Handler.md)?:The handler to use for the callback. If`null`, callbacks will happen on the service's main thread. |

### unregisterFingerprintGestureCallback

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun unregisterFingerprintGestureCallback(callback: FingerprintGestureController.FingerprintGestureCallback!): Unit
```

Unregister a listener added with [registerFingerprintGestureCallback](../android/accessibilityservice/FingerprintGestureController.md)).

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [FingerprintGestureController.FingerprintGestureCallback](../android/accessibilityservice/FingerprintGestureController.FingerprintGestureCallback.md)!:The callback to remove. Removing a callback that was never added has no effect. |
