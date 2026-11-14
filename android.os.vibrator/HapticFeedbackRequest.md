# HapticFeedbackRequest

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# HapticFeedbackRequest

Kotlin| [Java](HapticFeedbackRequest.md) 
| --- | --- |

```
class HapticFeedbackRequest
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.vibrator.HapticFeedbackRequest](HapticFeedbackRequest.md) |

Encapsulates a request to perform a haptic feedback.

Use [Builder](../android/os/vibrator/HapticFeedbackRequest.Builder.md) to create a new instance of this class.

## Summary

| Nested classes ||
|---|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/os/vibrator/HapticFeedbackRequest.Builder.md) Builder for [HapticFeedbackRequest](HapticFeedbackRequest.md). |

| Public methods ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](HapticFeedbackRequest.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getFeedbackConstant](HapticFeedbackRequest.md))`()` Returns the haptic feedback constant used to define the vibration effect to be played by this request. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getFlags](HapticFeedbackRequest.md))`()` Returns the [HapticFeedbackConstants](../android.view/HapticFeedbackConstants.md) flags for the haptic feedback request. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getUsage](HapticFeedbackRequest.md))`()` Returns the [VibrationAttributes](../android.os/VibrationAttributes.md) usage for the haptic feedback request. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](HapticFeedbackRequest.md))`()` <br /> |

## Public methods

### equals

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The`equals`method implements an equivalence relation on non-null object references:

- It is*reflexive* : for any non-null reference value`x`,`x.equals(x)`should return`true`.
- It is*symmetric* : for any non-null reference values`x`and`y`,`x.equals(y)`should return`true`if and only if`y.equals(x)`returns`true`.
- It is*transitive* : for any non-null reference values`x`,`y`, and`z`, if`x.equals(y)`returns`true`and`y.equals(z)`returns`true`, then`x.equals(z)`should return`true`.
- It is*consistent* : for any non-null reference values`x`and`y`, multiple invocations of`x.equals(y)`consistently return`true`or consistently return`false`, provided no information used in`equals`comparisons on the objects is modified.
- For any non-null reference value`x`,`x.equals(null)`should return`false`.

An equivalence relation partitions the elements it operates on into*equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |
| `o` | This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getFeedbackConstant

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFeedbackConstant(): Int
```

Returns the haptic feedback constant used to define the vibration effect to be played by this request.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.view.HapticFeedbackConstants#NO_HAPTICS](../android.view/HapticFeedbackConstants.md), [android.view.HapticFeedbackConstants#LONG_PRESS](../android.view/HapticFeedbackConstants.md), [android.view.HapticFeedbackConstants#VIRTUAL_KEY](../android.view/HapticFeedbackConstants.md), [android.view.HapticFeedbackConstants#KEYBOARD_TAP](../android.view/HapticFeedbackConstants.md), [android.view.HapticFeedbackConstants#CLOCK_TICK](../android.view/HapticFeedbackConstants.md), android.view.HapticFeedbackConstants.CALENDAR_DATE, [android.view.HapticFeedbackConstants#CONTEXT_CLICK](../android.view/HapticFeedbackConstants.md), [android.view.HapticFeedbackConstants#KEYBOARD_RELEASE](../android.view/HapticFeedbackConstants.md), [android.view.HapticFeedbackConstants#VIRTUAL_KEY_RELEASE](../android.view/HapticFeedbackConstants.md), [android.view.HapticFeedbackConstants#TEXT_HANDLE_MOVE](../android.view/HapticFeedbackConstants.md), android.view.HapticFeedbackConstants.DRAG_CROSSING, [android.view.HapticFeedbackConstants#GESTURE_START](../android.view/HapticFeedbackConstants.md), [android.view.HapticFeedbackConstants#GESTURE_END](../android.view/HapticFeedbackConstants.md), android.view.HapticFeedbackConstants.EDGE_SQUEEZE, android.view.HapticFeedbackConstants.EDGE_RELEASE, [android.view.HapticFeedbackConstants#CONFIRM](../android.view/HapticFeedbackConstants.md), [android.view.HapticFeedbackConstants#REJECT](../android.view/HapticFeedbackConstants.md), android.view.HapticFeedbackConstants.SCROLL_TICK, android.view.HapticFeedbackConstants.SCROLL_ITEM_FOCUS, android.view.HapticFeedbackConstants.SCROLL_LIMIT, [android.view.HapticFeedbackConstants#TOGGLE_ON](../android.view/HapticFeedbackConstants.md), [android.view.HapticFeedbackConstants#TOGGLE_OFF](../android.view/HapticFeedbackConstants.md), [android.view.HapticFeedbackConstants#GESTURE_THRESHOLD_ACTIVATE](../android.view/HapticFeedbackConstants.md), [android.view.HapticFeedbackConstants#GESTURE_THRESHOLD_DEACTIVATE](../android.view/HapticFeedbackConstants.md), [android.view.HapticFeedbackConstants#DRAG_START](../android.view/HapticFeedbackConstants.md), [android.view.HapticFeedbackConstants#SEGMENT_TICK](../android.view/HapticFeedbackConstants.md), [android.view.HapticFeedbackConstants#SEGMENT_FREQUENT_TICK](../android.view/HapticFeedbackConstants.md), android.view.HapticFeedbackConstants.SAFE_MODE_ENABLED, android.view.HapticFeedbackConstants.ASSISTANT_BUTTON, android.view.HapticFeedbackConstants.LONG_PRESS_POWER_BUTTON, android.view.HapticFeedbackConstants.BIOMETRIC_CONFIRM, or android.view.HapticFeedbackConstants.BIOMETRIC_REJECT |

**See Also**

- [android.view.HapticFeedbackConstants](../android.view/HapticFeedbackConstants.md) 

### getFlags

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFlags(): Int
```

Returns the [HapticFeedbackConstants](../android.view/HapticFeedbackConstants.md) flags for the haptic feedback request.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is either`0`or a combination of [android.view.HapticFeedbackConstants#FLAG_IGNORE_VIEW_SETTING](../android.view/HapticFeedbackConstants.md), and [android.view.HapticFeedbackConstants#FLAG_IGNORE_GLOBAL_SETTING](../android.view/HapticFeedbackConstants.md) |

### getUsage

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getUsage(): Int
```

Returns the [VibrationAttributes](../android.os/VibrationAttributes.md) usage for the haptic feedback request.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.os.VibrationAttributes#USAGE_UNKNOWN](../android.os/VibrationAttributes.md), [android.os.VibrationAttributes#USAGE_ACCESSIBILITY](../android.os/VibrationAttributes.md), [android.os.VibrationAttributes#USAGE_ALARM](../android.os/VibrationAttributes.md), [android.os.VibrationAttributes#USAGE_COMMUNICATION_REQUEST](../android.os/VibrationAttributes.md), [android.os.VibrationAttributes#USAGE_HARDWARE_FEEDBACK](../android.os/VibrationAttributes.md), [android.os.VibrationAttributes#USAGE_MEDIA](../android.os/VibrationAttributes.md), [android.os.VibrationAttributes#USAGE_NOTIFICATION](../android.os/VibrationAttributes.md), [android.os.VibrationAttributes#USAGE_PHYSICAL_EMULATION](../android.os/VibrationAttributes.md), [android.os.VibrationAttributes#USAGE_RINGTONE](../android.os/VibrationAttributes.md), [android.os.VibrationAttributes#USAGE_TOUCH](../android.os/VibrationAttributes.md), android.os.VibrationAttributes.USAGE_IME_FEEDBACK, or [android.os.VibrationAttributes#USAGE_GESTURE_INPUT](../android.os/VibrationAttributes.md) |

**See Also**

- [android.os.VibrationAttributes#getUsage](../android.os/VibrationAttributes.md)) 

### hashCode

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |
