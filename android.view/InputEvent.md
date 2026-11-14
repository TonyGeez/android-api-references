# InputEvent

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InputEvent

Kotlin| [Java](https://developer.android.com/reference/android/view/InputEvent "View this page in Java") 
| --- | --- |

```
abstract class InputEvent : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.InputEvent](https://developer.android.com/reference/kotlin/android/view/InputEvent#) |

| Known Direct Subclasses [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent), [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent) |----------------------------------------------------------------------------------------|------------------------------------------------------------------------| | [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent) | Object used to report key and button events. | | [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent) | Object used to report movement (mouse, pen, finger, trackball) events. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Common base class for input events.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/view/InputEvent#describeContents())`()` <br /> |
| [InputDevice](https://developer.android.com/reference/kotlin/android/view/InputDevice)! | [getDevice](https://developer.android.com/reference/kotlin/android/view/InputEvent#getDevice())`()` Gets the device that this event came from. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDeviceId](https://developer.android.com/reference/kotlin/android/view/InputEvent#getDeviceId())`()` Gets the id for the device that this event came from. |
| --- | --- |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getEventTime](https://developer.android.com/reference/kotlin/android/view/InputEvent#getEventTime())`()` Retrieve the time this event occurred, in the [android.os.SystemClock#uptimeMillis](https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis())time base. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSource](https://developer.android.com/reference/kotlin/android/view/InputEvent#getSource())`()` Gets the source of the event. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isFromSource](https://developer.android.com/reference/kotlin/android/view/InputEvent#isFromSource(kotlin.Int))`(`source:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Determines whether the event is from the given source. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Flatten this object in to a Parcel. <br /> | ||

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [InputEvent](https://developer.android.com/reference/kotlin/android/view/InputEvent#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/view/InputEvent#CREATOR:android.os.Parcelable.Creator) <br /> |

## Public methods

### describeContents

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getDevice

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDevice(): InputDevice!
```

Gets the device that this event came from.

| Return ||
|-----------------------------------------------------------------------------------------|---------------------------------|
| [InputDevice](https://developer.android.com/reference/kotlin/android/view/InputDevice)! | The device, or null if unknown. |

### getDeviceId

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getDeviceId(): Int
```

Gets the id for the device that this event came from. An id of zero indicates that the event didn't come from a physical device and maps to the default keymap. The other numbers are arbitrary and you shouldn't depend on the values.

| Return ||
|----------------------------------------------------------------------------|----------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The device id. |

**See Also**

- [android.view.InputDevice#getDevice](https://developer.android.com/reference/kotlin/android/view/InputDevice#getDevice(kotlin.Int)) 

### getEventTime

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getEventTime(): Long
```

Retrieve the time this event occurred, in the [android.os.SystemClock#uptimeMillis](https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis())time base.

| Return ||
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | Returns the time this event occurred, in the [android.os.SystemClock#uptimeMillis](https://developer.android.com/reference/kotlin/android/os/SystemClock.html#uptimeMillis())time base. |

### getSource

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getSource(): Int
```

Gets the source of the event.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The event source or [InputDevice.SOURCE_UNKNOWN](https://developer.android.com/reference/kotlin/android/view/InputDevice#SOURCE_UNKNOWN:kotlin.Int) if unknown. |

**See Also**

- [android.view.InputDevice#getSources](https://developer.android.com/reference/kotlin/android/view/InputDevice#getSources()) 

### isFromSource

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isFromSource(source: Int): Boolean
```

Determines whether the event is from the given source.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `source` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The input source to check against. This can be a specific device type, such as [InputDevice.SOURCE_TOUCH_NAVIGATION](https://developer.android.com/reference/kotlin/android/view/InputDevice#SOURCE_TOUCH_NAVIGATION:kotlin.Int), or a more generic device class, such as [InputDevice.SOURCE_CLASS_POINTER](https://developer.android.com/reference/kotlin/android/view/InputDevice#SOURCE_CLASS_POINTER:kotlin.Int). |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Whether the event is from the given source. |

## Properties

### CREATOR

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<InputEvent!>
```
