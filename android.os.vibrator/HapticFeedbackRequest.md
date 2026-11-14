# HapticFeedbackRequest

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# HapticFeedbackRequest

Kotlin| [Java](https://developer.android.com/reference/android/os/vibrator/HapticFeedbackRequest "View this page in Java") 

```
class HapticFeedbackRequest
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.os.vibrator.HapticFeedbackRequest](https://developer.android.com/reference/kotlin/android/os/vibrator/HapticFeedbackRequest#) |

Encapsulates a request to perform a haptic feedback.

Use [Builder](https://developer.android.com/reference/kotlin/android/os/vibrator/HapticFeedbackRequest.Builder) to create a new instance of this class.

## Summary

| Nested classes ||
|---|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/os/vibrator/HapticFeedbackRequest.Builder) Builder for [HapticFeedbackRequest](https://developer.android.com/reference/kotlin/android/os/vibrator/HapticFeedbackRequest#). |

| Public methods ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/os/vibrator/HapticFeedbackRequest#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getFeedbackConstant](https://developer.android.com/reference/kotlin/android/os/vibrator/HapticFeedbackRequest#getFeedbackConstant())`()` Returns the haptic feedback constant used to define the vibration effect to be played by this request. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getFlags](https://developer.android.com/reference/kotlin/android/os/vibrator/HapticFeedbackRequest#getFlags())`()` Returns the [HapticFeedbackConstants](https://developer.android.com/reference/kotlin/android/view/HapticFeedbackConstants.html#) flags for the haptic feedback request. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getUsage](https://developer.android.com/reference/kotlin/android/os/vibrator/HapticFeedbackRequest#getUsage())`()` Returns the [VibrationAttributes](https://developer.android.com/reference/kotlin/android/os/VibrationAttributes.html#) usage for the haptic feedback request. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/os/vibrator/HapticFeedbackRequest#hashCode())`()` <br /> |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.view.HapticFeedbackConstants#NO_HAPTICS](https://developer.android.com/reference/kotlin/android/view/HapticFeedbackConstants.html#NO_HAPTICS:kotlin.Int), [android.view.HapticFeedbackConstants#LONG_PRESS](https://developer.android.com/reference/kotlin/android/view/HapticFeedbackConstants.html#LONG_PRESS:kotlin.Int), [android.view.HapticFeedbackConstants#VIRTUAL_KEY](https://developer.android.com/reference/kotlin/android/view/HapticFeedbackConstants.html#VIRTUAL_KEY:kotlin.Int), [android.view.HapticFeedbackConstants#KEYBOARD_TAP](https://developer.android.com/reference/kotlin/android/view/HapticFeedbackConstants.html#KEYBOARD_TAP:kotlin.Int), [android.view.HapticFeedbackConstants#CLOCK_TICK](https://developer.android.com/reference/kotlin/android/view/HapticFeedbackConstants.html#CLOCK_TICK:kotlin.Int), android.view.HapticFeedbackConstants.CALENDAR_DATE, [android.view.HapticFeedbackConstants#CONTEXT_CLICK](https://developer.android.com/reference/kotlin/android/view/HapticFeedbackConstants.html#CONTEXT_CLICK:kotlin.Int), [android.view.HapticFeedbackConstants#KEYBOARD_RELEASE](https://developer.android.com/reference/kotlin/android/view/HapticFeedbackConstants.html#KEYBOARD_RELEASE:kotlin.Int), [android.view.HapticFeedbackConstants#VIRTUAL_KEY_RELEASE](https://developer.android.com/reference/kotlin/android/view/HapticFeedbackConstants.html#VIRTUAL_KEY_RELEASE:kotlin.Int), [android.view.HapticFeedbackConstants#TEXT_HANDLE_MOVE](https://developer.android.com/reference/kotlin/android/view/HapticFeedbackConstants.html#TEXT_HANDLE_MOVE:kotlin.Int), android.view.HapticFeedbackConstants.DRAG_CROSSING, [android.view.HapticFeedbackConstants#GESTURE_START](https://developer.android.com/reference/kotlin/android/view/HapticFeedbackConstants.html#GESTURE_START:kotlin.Int), [android.view.HapticFeedbackConstants#GESTURE_END](https://developer.android.com/reference/kotlin/android/view/HapticFeedbackConstants.html#GESTURE_END:kotlin.Int), android.view.HapticFeedbackConstants.EDGE_SQUEEZE, android.view.HapticFeedbackConstants.EDGE_RELEASE, [android.view.HapticFeedbackConstants#CONFIRM](https://developer.android.com/reference/kotlin/android/view/HapticFeedbackConstants.html#CONFIRM:kotlin.Int), [android.view.HapticFeedbackConstants#REJECT](https://developer.android.com/reference/kotlin/android/view/HapticFeedbackConstants.html#REJECT:kotlin.Int), android.view.HapticFeedbackConstants.SCROLL_TICK, android.view.HapticFeedbackConstants.SCROLL_ITEM_FOCUS, android.view.HapticFeedbackConstants.SCROLL_LIMIT, [android.view.HapticFeedbackConstants#TOGGLE_ON](https://developer.android.com/reference/kotlin/android/view/HapticFeedbackConstants.html#TOGGLE_ON:kotlin.Int), [android.view.HapticFeedbackConstants#TOGGLE_OFF](https://developer.android.com/reference/kotlin/android/view/HapticFeedbackConstants.html#TOGGLE_OFF:kotlin.Int), [android.view.HapticFeedbackConstants#GESTURE_THRESHOLD_ACTIVATE](https://developer.android.com/reference/kotlin/android/view/HapticFeedbackConstants.html#GESTURE_THRESHOLD_ACTIVATE:kotlin.Int), [android.view.HapticFeedbackConstants#GESTURE_THRESHOLD_DEACTIVATE](https://developer.android.com/reference/kotlin/android/view/HapticFeedbackConstants.html#GESTURE_THRESHOLD_DEACTIVATE:kotlin.Int), [android.view.HapticFeedbackConstants#DRAG_START](https://developer.android.com/reference/kotlin/android/view/HapticFeedbackConstants.html#DRAG_START:kotlin.Int), [android.view.HapticFeedbackConstants#SEGMENT_TICK](https://developer.android.com/reference/kotlin/android/view/HapticFeedbackConstants.html#SEGMENT_TICK:kotlin.Int), [android.view.HapticFeedbackConstants#SEGMENT_FREQUENT_TICK](https://developer.android.com/reference/kotlin/android/view/HapticFeedbackConstants.html#SEGMENT_FREQUENT_TICK:kotlin.Int), android.view.HapticFeedbackConstants.SAFE_MODE_ENABLED, android.view.HapticFeedbackConstants.ASSISTANT_BUTTON, android.view.HapticFeedbackConstants.LONG_PRESS_POWER_BUTTON, android.view.HapticFeedbackConstants.BIOMETRIC_CONFIRM, or android.view.HapticFeedbackConstants.BIOMETRIC_REJECT |

**See Also**

- [android.view.HapticFeedbackConstants](https://developer.android.com/reference/kotlin/android/view/HapticFeedbackConstants.html#) 

### getFlags

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFlags(): Int
```

Returns the [HapticFeedbackConstants](https://developer.android.com/reference/kotlin/android/view/HapticFeedbackConstants.html#) flags for the haptic feedback request.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is either`0`or a combination of [android.view.HapticFeedbackConstants#FLAG_IGNORE_VIEW_SETTING](https://developer.android.com/reference/kotlin/android/view/HapticFeedbackConstants.html#FLAG_IGNORE_VIEW_SETTING:kotlin.Int), and [android.view.HapticFeedbackConstants#FLAG_IGNORE_GLOBAL_SETTING](https://developer.android.com/reference/kotlin/android/view/HapticFeedbackConstants.html#FLAG_IGNORE_GLOBAL_SETTING:kotlin.Int) |

### getUsage

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getUsage(): Int
```

Returns the [VibrationAttributes](https://developer.android.com/reference/kotlin/android/os/VibrationAttributes.html#) usage for the haptic feedback request.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.os.VibrationAttributes#USAGE_UNKNOWN](https://developer.android.com/reference/kotlin/android/os/VibrationAttributes.html#USAGE_UNKNOWN:kotlin.Int), [android.os.VibrationAttributes#USAGE_ACCESSIBILITY](https://developer.android.com/reference/kotlin/android/os/VibrationAttributes.html#USAGE_ACCESSIBILITY:kotlin.Int), [android.os.VibrationAttributes#USAGE_ALARM](https://developer.android.com/reference/kotlin/android/os/VibrationAttributes.html#USAGE_ALARM:kotlin.Int), [android.os.VibrationAttributes#USAGE_COMMUNICATION_REQUEST](https://developer.android.com/reference/kotlin/android/os/VibrationAttributes.html#USAGE_COMMUNICATION_REQUEST:kotlin.Int), [android.os.VibrationAttributes#USAGE_HARDWARE_FEEDBACK](https://developer.android.com/reference/kotlin/android/os/VibrationAttributes.html#USAGE_HARDWARE_FEEDBACK:kotlin.Int), [android.os.VibrationAttributes#USAGE_MEDIA](https://developer.android.com/reference/kotlin/android/os/VibrationAttributes.html#USAGE_MEDIA:kotlin.Int), [android.os.VibrationAttributes#USAGE_NOTIFICATION](https://developer.android.com/reference/kotlin/android/os/VibrationAttributes.html#USAGE_NOTIFICATION:kotlin.Int), [android.os.VibrationAttributes#USAGE_PHYSICAL_EMULATION](https://developer.android.com/reference/kotlin/android/os/VibrationAttributes.html#USAGE_PHYSICAL_EMULATION:kotlin.Int), [android.os.VibrationAttributes#USAGE_RINGTONE](https://developer.android.com/reference/kotlin/android/os/VibrationAttributes.html#USAGE_RINGTONE:kotlin.Int), [android.os.VibrationAttributes#USAGE_TOUCH](https://developer.android.com/reference/kotlin/android/os/VibrationAttributes.html#USAGE_TOUCH:kotlin.Int), android.os.VibrationAttributes.USAGE_IME_FEEDBACK, or [android.os.VibrationAttributes#USAGE_GESTURE_INPUT](https://developer.android.com/reference/kotlin/android/os/VibrationAttributes.html#USAGE_GESTURE_INPUT:kotlin.Int) |

**See Also**

- [android.os.VibrationAttributes#getUsage](https://developer.android.com/reference/kotlin/android/os/VibrationAttributes.html#getUsage()) 

### hashCode

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |
