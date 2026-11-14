# AccessibilityGestureEvent

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AccessibilityGestureEvent

Kotlin| [Java](https://developer.android.com/reference/android/accessibilityservice/AccessibilityGestureEvent "View this page in Java") 

```
class AccessibilityGestureEvent : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.accessibilityservice.AccessibilityGestureEvent](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityGestureEvent#) |

This class describes the gesture event including gesture id and which display it happens on.

**Note:** Accessibility services setting the [android.accessibilityservice.AccessibilityServiceInfo#FLAG_REQUEST_TOUCH_EXPLORATION_MODE](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo#FLAG_REQUEST_TOUCH_EXPLORATION_MODE:kotlin.Int) flag can receive gestures.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AccessibilityGestureEvent](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityGestureEvent#AccessibilityGestureEvent(kotlin.Int,%20kotlin.Int,%20kotlin.collections.MutableList))`(`gestureId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `displayId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `motionEvents:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#)!>`)` Constructs an AccessibilityGestureEvent to be dispatched to an accessibility service. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityGestureEvent#describeContents())`()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [gestureIdToString](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityGestureEvent#gestureIdToString(kotlin.Int))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a string representation of the specified gesture id. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDisplayId](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityGestureEvent#getDisplayId())`()` Returns the display id of the received-gesture display, for use with [android.hardware.display.DisplayManager#getDisplay(int)](https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager.html#getDisplay(kotlin.Int)). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGestureId](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityGestureEvent#getGestureId())`()` Returns performed gesture id. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#)!\> | [getMotionEvents](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityGestureEvent#getMotionEvents())`()` Returns the motion events that lead to this gesture. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityGestureEvent#toString())`()` Returns a string representation of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityGestureEvent#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`parcel:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [AccessibilityGestureEvent](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityGestureEvent#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityGestureEvent#CREATOR:android.os.Parcelable.Creator) <br /> |

## Public constructors

### AccessibilityGestureEvent

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AccessibilityGestureEvent(
    gestureId: Int, 
    displayId: Int, 
    motionEvents: MutableList<MotionEvent!>)
```

Constructs an AccessibilityGestureEvent to be dispatched to an accessibility service.

| Parameters ||
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `gestureId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the id number of the gesture. |
| `displayId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the display on which this gesture was performed. |
| `motionEvents` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#)!\>:the motion events that lead to this gesture. This value cannot be`null`. |

## Public methods

### describeContents

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of [writeToParcel(android.os.Parcel,int)](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)), the return value of this method must include the [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) bit.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### gestureIdToString

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun gestureIdToString(id: Int): String
```

Returns a string representation of the specified gesture id.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### getDisplayId

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDisplayId(): Int
```

Returns the display id of the received-gesture display, for use with [android.hardware.display.DisplayManager#getDisplay(int)](https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager.html#getDisplay(kotlin.Int)).

| Return ||
|----------------------------------------------------------------------------|-----------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the display id. |

### getGestureId

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getGestureId(): Int
```

Returns performed gesture id.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the performed gesture id. Value is [android.accessibilityservice.AccessibilityService#GESTURE_UNKNOWN](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#GESTURE_UNKNOWN:kotlin.Int), android.accessibilityservice.AccessibilityService.GESTURE_TOUCH_EXPLORATION, [android.accessibilityservice.AccessibilityService#GESTURE_2_FINGER_SINGLE_TAP](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#GESTURE_2_FINGER_SINGLE_TAP:kotlin.Int), [android.accessibilityservice.AccessibilityService#GESTURE_2_FINGER_DOUBLE_TAP](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#GESTURE_2_FINGER_DOUBLE_TAP:kotlin.Int), [android.accessibilityservice.AccessibilityService#GESTURE_2_FINGER_DOUBLE_TAP_AND_HOLD](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#GESTURE_2_FINGER_DOUBLE_TAP_AND_HOLD:kotlin.Int), [android.accessibilityservice.AccessibilityService#GESTURE_2_FINGER_TRIPLE_TAP](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#GESTURE_2_FINGER_TRIPLE_TAP:kotlin.Int), [android.accessibilityservice.AccessibilityService#GESTURE_2_FINGER_TRIPLE_TAP_AND_HOLD](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#GESTURE_2_FINGER_TRIPLE_TAP_AND_HOLD:kotlin.Int), [android.accessibilityservice.AccessibilityService#GESTURE_3_FINGER_SINGLE_TAP](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#GESTURE_3_FINGER_SINGLE_TAP:kotlin.Int), [android.accessibilityservice.AccessibilityService#GESTURE_3_FINGER_SINGLE_TAP_AND_HOLD](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#GESTURE_3_FINGER_SINGLE_TAP_AND_HOLD:kotlin.Int), [android.accessibilityservice.AccessibilityService#GESTURE_3_FINGER_DOUBLE_TAP](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#GESTURE_3_FINGER_DOUBLE_TAP:kotlin.Int), [android.accessibilityservice.AccessibilityService#GESTURE_3_FINGER_DOUBLE_TAP_AND_HOLD](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#GESTURE_3_FINGER_DOUBLE_TAP_AND_HOLD:kotlin.Int), [android.accessibilityservice.AccessibilityService#GESTURE_3_FINGER_TRIPLE_TAP](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#GESTURE_3_FINGER_TRIPLE_TAP:kotlin.Int), [android.accessibilityservice.AccessibilityService#GESTURE_3_FINGER_TRIPLE_TAP_AND_HOLD](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#GESTURE_3_FINGER_TRIPLE_TAP_AND_HOLD:kotlin.Int), [android.accessibilityservice.AccessibilityService#GESTURE_DOUBLE_TAP](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#GESTURE_DOUBLE_TAP:kotlin.Int), [android.accessibilityservice.AccessibilityService#GESTURE_DOUBLE_TAP_AND_HOLD](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#GESTURE_DOUBLE_TAP_AND_HOLD:kotlin.Int), [android.accessibilityservice.AccessibilityService#GESTURE_SWIPE_UP](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#GESTURE_SWIPE_UP:kotlin.Int), [android.accessibilityservice.AccessibilityService#GESTURE_SWIPE_UP_AND_LEFT](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#GESTURE_SWIPE_UP_AND_LEFT:kotlin.Int), [android.accessibilityservice.AccessibilityService#GESTURE_SWIPE_UP_AND_DOWN](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#GESTURE_SWIPE_UP_AND_DOWN:kotlin.Int), [android.accessibilityservice.AccessibilityService#GESTURE_SWIPE_UP_AND_RIGHT](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#GESTURE_SWIPE_UP_AND_RIGHT:kotlin.Int), [android.accessibilityservice.AccessibilityService#GESTURE_SWIPE_DOWN](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#GESTURE_SWIPE_DOWN:kotlin.Int), [android.accessibilityservice.AccessibilityService#GESTURE_SWIPE_DOWN_AND_LEFT](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#GESTURE_SWIPE_DOWN_AND_LEFT:kotlin.Int), [android.accessibilityservice.AccessibilityService#GESTURE_SWIPE_DOWN_AND_UP](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#GESTURE_SWIPE_DOWN_AND_UP:kotlin.Int), [android.accessibilityservice.AccessibilityService#GESTURE_SWIPE_DOWN_AND_RIGHT](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#GESTURE_SWIPE_DOWN_AND_RIGHT:kotlin.Int), [android.accessibilityservice.AccessibilityService#GESTURE_SWIPE_LEFT](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#GESTURE_SWIPE_LEFT:kotlin.Int), [android.accessibilityservice.AccessibilityService#GESTURE_SWIPE_LEFT_AND_UP](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#GESTURE_SWIPE_LEFT_AND_UP:kotlin.Int), [android.accessibilityservice.AccessibilityService#GESTURE_SWIPE_LEFT_AND_RIGHT](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#GESTURE_SWIPE_LEFT_AND_RIGHT:kotlin.Int), [android.accessibilityservice.AccessibilityService#GESTURE_SWIPE_LEFT_AND_DOWN](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#GESTURE_SWIPE_LEFT_AND_DOWN:kotlin.Int), [android.accessibilityservice.AccessibilityService#GESTURE_SWIPE_RIGHT](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#GESTURE_SWIPE_RIGHT:kotlin.Int), [android.accessibilityservice.AccessibilityService#GESTURE_SWIPE_RIGHT_AND_UP](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#GESTURE_SWIPE_RIGHT_AND_UP:kotlin.Int), [android.accessibilityservice.AccessibilityService#GESTURE_SWIPE_RIGHT_AND_LEFT](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#GESTURE_SWIPE_RIGHT_AND_LEFT:kotlin.Int), [android.accessibilityservice.AccessibilityService#GESTURE_SWIPE_RIGHT_AND_DOWN](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#GESTURE_SWIPE_RIGHT_AND_DOWN:kotlin.Int), [android.accessibilityservice.AccessibilityService#GESTURE_2_FINGER_SWIPE_DOWN](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#GESTURE_2_FINGER_SWIPE_DOWN:kotlin.Int), [android.accessibilityservice.AccessibilityService#GESTURE_2_FINGER_SWIPE_LEFT](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#GESTURE_2_FINGER_SWIPE_LEFT:kotlin.Int), [android.accessibilityservice.AccessibilityService#GESTURE_2_FINGER_SWIPE_RIGHT](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#GESTURE_2_FINGER_SWIPE_RIGHT:kotlin.Int), [android.accessibilityservice.AccessibilityService#GESTURE_2_FINGER_SWIPE_UP](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#GESTURE_2_FINGER_SWIPE_UP:kotlin.Int), [android.accessibilityservice.AccessibilityService#GESTURE_3_FINGER_SWIPE_DOWN](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#GESTURE_3_FINGER_SWIPE_DOWN:kotlin.Int), [android.accessibilityservice.AccessibilityService#GESTURE_3_FINGER_SWIPE_LEFT](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#GESTURE_3_FINGER_SWIPE_LEFT:kotlin.Int), [android.accessibilityservice.AccessibilityService#GESTURE_3_FINGER_SWIPE_RIGHT](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#GESTURE_3_FINGER_SWIPE_RIGHT:kotlin.Int), [android.accessibilityservice.AccessibilityService#GESTURE_3_FINGER_SWIPE_UP](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#GESTURE_3_FINGER_SWIPE_UP:kotlin.Int), [android.accessibilityservice.AccessibilityService#GESTURE_4_FINGER_DOUBLE_TAP](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#GESTURE_4_FINGER_DOUBLE_TAP:kotlin.Int), [android.accessibilityservice.AccessibilityService#GESTURE_4_FINGER_DOUBLE_TAP_AND_HOLD](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#GESTURE_4_FINGER_DOUBLE_TAP_AND_HOLD:kotlin.Int), [android.accessibilityservice.AccessibilityService#GESTURE_4_FINGER_SINGLE_TAP](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#GESTURE_4_FINGER_SINGLE_TAP:kotlin.Int), [android.accessibilityservice.AccessibilityService#GESTURE_4_FINGER_SWIPE_DOWN](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#GESTURE_4_FINGER_SWIPE_DOWN:kotlin.Int), [android.accessibilityservice.AccessibilityService#GESTURE_4_FINGER_SWIPE_LEFT](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#GESTURE_4_FINGER_SWIPE_LEFT:kotlin.Int), [android.accessibilityservice.AccessibilityService#GESTURE_4_FINGER_SWIPE_RIGHT](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#GESTURE_4_FINGER_SWIPE_RIGHT:kotlin.Int), [android.accessibilityservice.AccessibilityService#GESTURE_4_FINGER_SWIPE_UP](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#GESTURE_4_FINGER_SWIPE_UP:kotlin.Int), or [android.accessibilityservice.AccessibilityService#GESTURE_4_FINGER_TRIPLE_TAP](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService#GESTURE_4_FINGER_TRIPLE_TAP:kotlin.Int) |

### getMotionEvents

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMotionEvents(): MutableList<MotionEvent!>
```

Returns the motion events that lead to this gesture.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#)!> | This value cannot be`null`. |

### toString

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### writeToParcel

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    parcel: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |
| `parcel` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):This value cannot be`null`. |

## Properties

### CREATOR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<AccessibilityGestureEvent!>
```  
**See Also**

- [android.os.Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)
