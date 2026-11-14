# AccessibilityGestureEvent

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AccessibilityGestureEvent

Kotlin| [Java](../android/accessibilityservice/AccessibilityGestureEvent.md) 
| --- | --- |

```
class AccessibilityGestureEvent : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.accessibilityservice.AccessibilityGestureEvent](../android/accessibilityservice/AccessibilityGestureEvent.md) |

This class describes the gesture event including gesture id and which display it happens on.

**Note:** Accessibility services setting the [android.accessibilityservice.AccessibilityServiceInfo#FLAG_REQUEST_TOUCH_EXPLORATION_MODE](../android/accessibilityservice/AccessibilityServiceInfo.md) flag can receive gestures.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AccessibilityGestureEvent](../android/accessibilityservice/AccessibilityGestureEvent.md))`(`gestureId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `displayId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `motionEvents:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [MotionEvent](../android/view/MotionEvent.md)!>`)` Constructs an AccessibilityGestureEvent to be dispatched to an accessibility service. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/accessibilityservice/AccessibilityGestureEvent.md))`()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [gestureIdToString](../android/accessibilityservice/AccessibilityGestureEvent.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a string representation of the specified gesture id. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDisplayId](../android/accessibilityservice/AccessibilityGestureEvent.md))`()` Returns the display id of the received-gesture display, for use with [android.hardware.display.DisplayManager#getDisplay(int)](../android/hardware/display/DisplayManager.md)). |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGestureId](../android/accessibilityservice/AccessibilityGestureEvent.md))`()` Returns performed gesture id. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [MotionEvent](../android/view/MotionEvent.md)!\> | [getMotionEvents](../android/accessibilityservice/AccessibilityGestureEvent.md))`()` Returns the motion events that lead to this gesture. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/accessibilityservice/AccessibilityGestureEvent.md))`()` Returns a string representation of the object. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/accessibilityservice/AccessibilityGestureEvent.md))`(`parcel:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [AccessibilityGestureEvent](../android/accessibilityservice/AccessibilityGestureEvent.md)!\> | [CREATOR](../android/accessibilityservice/AccessibilityGestureEvent.md) <br /> |

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
| `motionEvents` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [MotionEvent](../android/view/MotionEvent.md)!\>:the motion events that lead to this gesture. This value cannot be`null`. |
| --- | --- |

## Public methods

### describeContents

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of [writeToParcel(android.os.Parcel,int)](../android/os/Parcelable.md)), the return value of this method must include the [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) bit.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

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

Returns the display id of the received-gesture display, for use with [android.hardware.display.DisplayManager#getDisplay(int)](../android/hardware/display/DisplayManager.md)).

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the performed gesture id. Value is [android.accessibilityservice.AccessibilityService#GESTURE_UNKNOWN](../android/accessibilityservice/AccessibilityService.md), android.accessibilityservice.AccessibilityService.GESTURE_TOUCH_EXPLORATION, [android.accessibilityservice.AccessibilityService#GESTURE_2_FINGER_SINGLE_TAP](../android/accessibilityservice/AccessibilityService.md), [android.accessibilityservice.AccessibilityService#GESTURE_2_FINGER_DOUBLE_TAP](../android/accessibilityservice/AccessibilityService.md), [android.accessibilityservice.AccessibilityService#GESTURE_2_FINGER_DOUBLE_TAP_AND_HOLD](../android/accessibilityservice/AccessibilityService.md), [android.accessibilityservice.AccessibilityService#GESTURE_2_FINGER_TRIPLE_TAP](../android/accessibilityservice/AccessibilityService.md), [android.accessibilityservice.AccessibilityService#GESTURE_2_FINGER_TRIPLE_TAP_AND_HOLD](../android/accessibilityservice/AccessibilityService.md), [android.accessibilityservice.AccessibilityService#GESTURE_3_FINGER_SINGLE_TAP](../android/accessibilityservice/AccessibilityService.md), [android.accessibilityservice.AccessibilityService#GESTURE_3_FINGER_SINGLE_TAP_AND_HOLD](../android/accessibilityservice/AccessibilityService.md), [android.accessibilityservice.AccessibilityService#GESTURE_3_FINGER_DOUBLE_TAP](../android/accessibilityservice/AccessibilityService.md), [android.accessibilityservice.AccessibilityService#GESTURE_3_FINGER_DOUBLE_TAP_AND_HOLD](../android/accessibilityservice/AccessibilityService.md), [android.accessibilityservice.AccessibilityService#GESTURE_3_FINGER_TRIPLE_TAP](../android/accessibilityservice/AccessibilityService.md), [android.accessibilityservice.AccessibilityService#GESTURE_3_FINGER_TRIPLE_TAP_AND_HOLD](../android/accessibilityservice/AccessibilityService.md), [android.accessibilityservice.AccessibilityService#GESTURE_DOUBLE_TAP](../android/accessibilityservice/AccessibilityService.md), [android.accessibilityservice.AccessibilityService#GESTURE_DOUBLE_TAP_AND_HOLD](../android/accessibilityservice/AccessibilityService.md), [android.accessibilityservice.AccessibilityService#GESTURE_SWIPE_UP](../android/accessibilityservice/AccessibilityService.md), [android.accessibilityservice.AccessibilityService#GESTURE_SWIPE_UP_AND_LEFT](../android/accessibilityservice/AccessibilityService.md), [android.accessibilityservice.AccessibilityService#GESTURE_SWIPE_UP_AND_DOWN](../android/accessibilityservice/AccessibilityService.md), [android.accessibilityservice.AccessibilityService#GESTURE_SWIPE_UP_AND_RIGHT](../android/accessibilityservice/AccessibilityService.md), [android.accessibilityservice.AccessibilityService#GESTURE_SWIPE_DOWN](../android/accessibilityservice/AccessibilityService.md), [android.accessibilityservice.AccessibilityService#GESTURE_SWIPE_DOWN_AND_LEFT](../android/accessibilityservice/AccessibilityService.md), [android.accessibilityservice.AccessibilityService#GESTURE_SWIPE_DOWN_AND_UP](../android/accessibilityservice/AccessibilityService.md), [android.accessibilityservice.AccessibilityService#GESTURE_SWIPE_DOWN_AND_RIGHT](../android/accessibilityservice/AccessibilityService.md), [android.accessibilityservice.AccessibilityService#GESTURE_SWIPE_LEFT](../android/accessibilityservice/AccessibilityService.md), [android.accessibilityservice.AccessibilityService#GESTURE_SWIPE_LEFT_AND_UP](../android/accessibilityservice/AccessibilityService.md), [android.accessibilityservice.AccessibilityService#GESTURE_SWIPE_LEFT_AND_RIGHT](../android/accessibilityservice/AccessibilityService.md), [android.accessibilityservice.AccessibilityService#GESTURE_SWIPE_LEFT_AND_DOWN](../android/accessibilityservice/AccessibilityService.md), [android.accessibilityservice.AccessibilityService#GESTURE_SWIPE_RIGHT](../android/accessibilityservice/AccessibilityService.md), [android.accessibilityservice.AccessibilityService#GESTURE_SWIPE_RIGHT_AND_UP](../android/accessibilityservice/AccessibilityService.md), [android.accessibilityservice.AccessibilityService#GESTURE_SWIPE_RIGHT_AND_LEFT](../android/accessibilityservice/AccessibilityService.md), [android.accessibilityservice.AccessibilityService#GESTURE_SWIPE_RIGHT_AND_DOWN](../android/accessibilityservice/AccessibilityService.md), [android.accessibilityservice.AccessibilityService#GESTURE_2_FINGER_SWIPE_DOWN](../android/accessibilityservice/AccessibilityService.md), [android.accessibilityservice.AccessibilityService#GESTURE_2_FINGER_SWIPE_LEFT](../android/accessibilityservice/AccessibilityService.md), [android.accessibilityservice.AccessibilityService#GESTURE_2_FINGER_SWIPE_RIGHT](../android/accessibilityservice/AccessibilityService.md), [android.accessibilityservice.AccessibilityService#GESTURE_2_FINGER_SWIPE_UP](../android/accessibilityservice/AccessibilityService.md), [android.accessibilityservice.AccessibilityService#GESTURE_3_FINGER_SWIPE_DOWN](../android/accessibilityservice/AccessibilityService.md), [android.accessibilityservice.AccessibilityService#GESTURE_3_FINGER_SWIPE_LEFT](../android/accessibilityservice/AccessibilityService.md), [android.accessibilityservice.AccessibilityService#GESTURE_3_FINGER_SWIPE_RIGHT](../android/accessibilityservice/AccessibilityService.md), [android.accessibilityservice.AccessibilityService#GESTURE_3_FINGER_SWIPE_UP](../android/accessibilityservice/AccessibilityService.md), [android.accessibilityservice.AccessibilityService#GESTURE_4_FINGER_DOUBLE_TAP](../android/accessibilityservice/AccessibilityService.md), [android.accessibilityservice.AccessibilityService#GESTURE_4_FINGER_DOUBLE_TAP_AND_HOLD](../android/accessibilityservice/AccessibilityService.md), [android.accessibilityservice.AccessibilityService#GESTURE_4_FINGER_SINGLE_TAP](../android/accessibilityservice/AccessibilityService.md), [android.accessibilityservice.AccessibilityService#GESTURE_4_FINGER_SWIPE_DOWN](../android/accessibilityservice/AccessibilityService.md), [android.accessibilityservice.AccessibilityService#GESTURE_4_FINGER_SWIPE_LEFT](../android/accessibilityservice/AccessibilityService.md), [android.accessibilityservice.AccessibilityService#GESTURE_4_FINGER_SWIPE_RIGHT](../android/accessibilityservice/AccessibilityService.md), [android.accessibilityservice.AccessibilityService#GESTURE_4_FINGER_SWIPE_UP](../android/accessibilityservice/AccessibilityService.md), or [android.accessibilityservice.AccessibilityService#GESTURE_4_FINGER_TRIPLE_TAP](../android/accessibilityservice/AccessibilityService.md) |

### getMotionEvents

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMotionEvents(): MutableList<MotionEvent!>
```

Returns the motion events that lead to this gesture.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [MotionEvent](../android/view/MotionEvent.md)!> | This value cannot be`null`. |

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
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |
| `parcel` | [Parcel](../android/os/Parcel.md):This value cannot be`null`. |
| --- | --- |

## Properties

### CREATOR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<AccessibilityGestureEvent!>
```  
**See Also**

- [android.os.Parcelable.Creator](../android/os/Parcelable.Creator.md)
