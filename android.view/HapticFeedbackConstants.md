# HapticFeedbackConstants

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# HapticFeedbackConstants

Kotlin| [Java](https://developer.android.com/reference/android/view/HapticFeedbackConstants "View this page in Java") 

```
open class HapticFeedbackConstants
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.view.HapticFeedbackConstants](https://developer.android.com/reference/kotlin/android/view/HapticFeedbackConstants#) |

Constants to be used to perform haptic feedback effects via [View.performHapticFeedback(int)](https://developer.android.com/reference/kotlin/android/view/View#performHapticFeedback(kotlin.Int))

## Summary

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CLOCK_TICK](https://developer.android.com/reference/kotlin/android/view/HapticFeedbackConstants#CLOCK_TICK:kotlin.Int) The user has pressed either an hour or minute tick of a Clock. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONFIRM](https://developer.android.com/reference/kotlin/android/view/HapticFeedbackConstants#CONFIRM:kotlin.Int) A haptic effect to signal the confirmation or successful completion of a user interaction. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTEXT_CLICK](https://developer.android.com/reference/kotlin/android/view/HapticFeedbackConstants#CONTEXT_CLICK:kotlin.Int) The user has performed a context click on an object. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DRAG_START](https://developer.android.com/reference/kotlin/android/view/HapticFeedbackConstants#DRAG_START:kotlin.Int) The user has started a drag-and-drop gesture. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_IGNORE_GLOBAL_SETTING](https://developer.android.com/reference/kotlin/android/view/HapticFeedbackConstants#FLAG_IGNORE_GLOBAL_SETTING:kotlin.Int) Flag for [View.performHapticFeedback(int, int)](https://developer.android.com/reference/kotlin/android/view/View#performHapticFeedback(kotlin.Int,%20kotlin.Int)): Ignore the global setting for whether to perform haptic feedback, do it always. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_IGNORE_VIEW_SETTING](https://developer.android.com/reference/kotlin/android/view/HapticFeedbackConstants#FLAG_IGNORE_VIEW_SETTING:kotlin.Int) Flag for [View.performHapticFeedback(int, int)](https://developer.android.com/reference/kotlin/android/view/View#performHapticFeedback(kotlin.Int,%20kotlin.Int)): Ignore the setting in the view for whether to perform haptic feedback, do it always. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GESTURE_END](https://developer.android.com/reference/kotlin/android/view/HapticFeedbackConstants#GESTURE_END:kotlin.Int) The user has finished a gesture (e.g. on the soft keyboard). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GESTURE_START](https://developer.android.com/reference/kotlin/android/view/HapticFeedbackConstants#GESTURE_START:kotlin.Int) The user has started a gesture (e.g. on the soft keyboard). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GESTURE_THRESHOLD_ACTIVATE](https://developer.android.com/reference/kotlin/android/view/HapticFeedbackConstants#GESTURE_THRESHOLD_ACTIVATE:kotlin.Int) The user is executing a swipe/drag-style gesture, such as pull-to-refresh, where the gesture action is "eligible" at a certain threshold of movement, and can be cancelled by moving back past the threshold. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GESTURE_THRESHOLD_DEACTIVATE](https://developer.android.com/reference/kotlin/android/view/HapticFeedbackConstants#GESTURE_THRESHOLD_DEACTIVATE:kotlin.Int) The user is executing a swipe/drag-style gesture, such as pull-to-refresh, where the gesture action is "eligible" at a certain threshold of movement, and can be cancelled by moving back past the threshold. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [KEYBOARD_PRESS](https://developer.android.com/reference/kotlin/android/view/HapticFeedbackConstants#KEYBOARD_PRESS:kotlin.Int) The user has pressed a virtual or software keyboard key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [KEYBOARD_RELEASE](https://developer.android.com/reference/kotlin/android/view/HapticFeedbackConstants#KEYBOARD_RELEASE:kotlin.Int) The user has released a virtual keyboard key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [KEYBOARD_TAP](https://developer.android.com/reference/kotlin/android/view/HapticFeedbackConstants#KEYBOARD_TAP:kotlin.Int) The user has pressed a soft keyboard key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LONG_PRESS](https://developer.android.com/reference/kotlin/android/view/HapticFeedbackConstants#LONG_PRESS:kotlin.Int) The user has performed a long press on an object that is resulting in an action being performed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NO_HAPTICS](https://developer.android.com/reference/kotlin/android/view/HapticFeedbackConstants#NO_HAPTICS:kotlin.Int) No haptic feedback should be performed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REJECT](https://developer.android.com/reference/kotlin/android/view/HapticFeedbackConstants#REJECT:kotlin.Int) A haptic effect to signal the rejection or failure of a user interaction. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SEGMENT_FREQUENT_TICK](https://developer.android.com/reference/kotlin/android/view/HapticFeedbackConstants#SEGMENT_FREQUENT_TICK:kotlin.Int) The user is switching between a series of many potential choices, for example minutes on a clock face, or individual percentages. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SEGMENT_TICK](https://developer.android.com/reference/kotlin/android/view/HapticFeedbackConstants#SEGMENT_TICK:kotlin.Int) The user is switching between a series of potential choices, for example items in a list or discrete points on a slider. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TEXT_HANDLE_MOVE](https://developer.android.com/reference/kotlin/android/view/HapticFeedbackConstants#TEXT_HANDLE_MOVE:kotlin.Int) The user has performed a selection/insertion handle move on text field. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TOGGLE_OFF](https://developer.android.com/reference/kotlin/android/view/HapticFeedbackConstants#TOGGLE_OFF:kotlin.Int) The user has toggled a switch or button into the off position. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TOGGLE_ON](https://developer.android.com/reference/kotlin/android/view/HapticFeedbackConstants#TOGGLE_ON:kotlin.Int) The user has toggled a switch or button into the on position. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VIRTUAL_KEY](https://developer.android.com/reference/kotlin/android/view/HapticFeedbackConstants#VIRTUAL_KEY:kotlin.Int) The user has pressed on a virtual on-screen key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VIRTUAL_KEY_RELEASE](https://developer.android.com/reference/kotlin/android/view/HapticFeedbackConstants#VIRTUAL_KEY_RELEASE:kotlin.Int) The user has released a virtual key. |

## Constants

### CLOCK_TICK

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CLOCK_TICK: Int
```

The user has pressed either an hour or minute tick of a Clock. 

 Value: 4

### CONFIRM

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONFIRM: Int
```

A haptic effect to signal the confirmation or successful completion of a user interaction. 

 Value: 16

### CONTEXT_CLICK

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTEXT_CLICK: Int
```

The user has performed a context click on an object. 

 Value: 6

### DRAG_START

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DRAG_START: Int
```

The user has started a drag-and-drop gesture. The drag target has just been "picked up". 

 Value: 25

### FLAG_IGNORE_GLOBAL_SETTING

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_IGNORE_GLOBAL_SETTING: Int
```

**Deprecated:** *Starting from [android.os.Build.VERSION_CODES#TIRAMISU](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int) only privileged apps can ignore user settings for touch feedback.*

Flag for [View.performHapticFeedback(int, int)](https://developer.android.com/reference/kotlin/android/view/View#performHapticFeedback(kotlin.Int,%20kotlin.Int)): Ignore the global setting for whether to perform haptic feedback, do it always. 

 Value: 2

### FLAG_IGNORE_VIEW_SETTING

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_IGNORE_VIEW_SETTING: Int
```

Flag for [View.performHapticFeedback(int, int)](https://developer.android.com/reference/kotlin/android/view/View#performHapticFeedback(kotlin.Int,%20kotlin.Int)): Ignore the setting in the view for whether to perform haptic feedback, do it always. 

 Value: 1

### GESTURE_END

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GESTURE_END: Int
```

The user has finished a gesture (e.g. on the soft keyboard). 

 Value: 13

### GESTURE_START

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GESTURE_START: Int
```

The user has started a gesture (e.g. on the soft keyboard). 

 Value: 12

### GESTURE_THRESHOLD_ACTIVATE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GESTURE_THRESHOLD_ACTIVATE: Int
```

The user is executing a swipe/drag-style gesture, such as pull-to-refresh, where the gesture action is "eligible" at a certain threshold of movement, and can be cancelled by moving back past the threshold. This constant indicates that the user's motion has just passed the threshold for the action to be activated on release. 

 Value: 23

**See Also**

- [#GESTURE_THRESHOLD_DEACTIVATE](https://developer.android.com/reference/kotlin/android/view/HapticFeedbackConstants#GESTURE_THRESHOLD_DEACTIVATE:kotlin.Int) 

### GESTURE_THRESHOLD_DEACTIVATE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GESTURE_THRESHOLD_DEACTIVATE: Int
```

The user is executing a swipe/drag-style gesture, such as pull-to-refresh, where the gesture action is "eligible" at a certain threshold of movement, and can be cancelled by moving back past the threshold. This constant indicates that the user's motion has just re-crossed back "under" the threshold for the action to be activated, meaning the gesture is currently in a cancelled state. 

 Value: 24

**See Also**

- [#GESTURE_THRESHOLD_ACTIVATE](https://developer.android.com/reference/kotlin/android/view/HapticFeedbackConstants#GESTURE_THRESHOLD_ACTIVATE:kotlin.Int) 

### KEYBOARD_PRESS

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KEYBOARD_PRESS: Int
```

The user has pressed a virtual or software keyboard key. 

 Value: 3

### KEYBOARD_RELEASE

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KEYBOARD_RELEASE: Int
```

The user has released a virtual keyboard key. 

 Value: 7

### KEYBOARD_TAP

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KEYBOARD_TAP: Int
```

The user has pressed a soft keyboard key. 

 Value: 3

### LONG_PRESS

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LONG_PRESS: Int
```

The user has performed a long press on an object that is resulting in an action being performed. 

 Value: 0

### NO_HAPTICS

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NO_HAPTICS: Int
```

No haptic feedback should be performed. Applications may use this value to indicate skipping a call to android.view.View#performHapticFeedback entirely, or else rely that it will immediately return`false`. 

 Value: -1

### REJECT

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REJECT: Int
```

A haptic effect to signal the rejection or failure of a user interaction. 

 Value: 17

### SEGMENT_FREQUENT_TICK

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SEGMENT_FREQUENT_TICK: Int
```

The user is switching between a series of many potential choices, for example minutes on a clock face, or individual percentages. This constant is expected to be very soft, so as not to be uncomfortable when performed a lot in quick succession. If the device can't make a suitably soft vibration, then it may not make any vibration.

Some specializations of this constant exist for specific actions, notably [CLOCK_TICK](https://developer.android.com/reference/kotlin/android/view/HapticFeedbackConstants#CLOCK_TICK:kotlin.Int) and [TEXT_HANDLE_MOVE](https://developer.android.com/reference/kotlin/android/view/HapticFeedbackConstants#TEXT_HANDLE_MOVE:kotlin.Int).

See also [SEGMENT_TICK](https://developer.android.com/reference/kotlin/android/view/HapticFeedbackConstants#SEGMENT_TICK:kotlin.Int). 

 Value: 27

### SEGMENT_TICK

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SEGMENT_TICK: Int
```

The user is switching between a series of potential choices, for example items in a list or discrete points on a slider.

See also [SEGMENT_FREQUENT_TICK](https://developer.android.com/reference/kotlin/android/view/HapticFeedbackConstants#SEGMENT_FREQUENT_TICK:kotlin.Int) for cases where density of choices is high, and the haptics should be lighter or suppressed for a better user experience. 

 Value: 26

### TEXT_HANDLE_MOVE

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TEXT_HANDLE_MOVE: Int
```

The user has performed a selection/insertion handle move on text field. 

 Value: 9

### TOGGLE_OFF

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TOGGLE_OFF: Int
```

The user has toggled a switch or button into the off position. 

 Value: 22

### TOGGLE_ON

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TOGGLE_ON: Int
```

The user has toggled a switch or button into the on position. 

 Value: 21

### VIRTUAL_KEY

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VIRTUAL_KEY: Int
```

The user has pressed on a virtual on-screen key. 

 Value: 1

### VIRTUAL_KEY_RELEASE

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VIRTUAL_KEY_RELEASE: Int
```

The user has released a virtual key. 

 Value: 8
