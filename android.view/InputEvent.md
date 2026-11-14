# InputEvent

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InputEvent

Kotlin| [Java](InputEvent.md) 
| --- | --- |

```
abstract class InputEvent : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.InputEvent](InputEvent.md) |

| Known Direct Subclasses [KeyEvent](KeyEvent.md), [MotionEvent](MotionEvent.md) |----------------------------------------------------------------------------------------|------------------------------------------------------------------------| | [KeyEvent](KeyEvent.md) | Object used to report key and button events. | | [MotionEvent](MotionEvent.md) | Object used to report movement (mouse, pen, finger, trackball) events. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Common base class for input events.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](InputEvent.md))`()` <br /> |
| [InputDevice](InputDevice.md)! | [getDevice](InputEvent.md))`()` Gets the device that this event came from. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDeviceId](InputEvent.md))`()` Gets the id for the device that this event came from. |
| --- | --- |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getEventTime](InputEvent.md))`()` Retrieve the time this event occurred, in the [android.os.SystemClock#uptimeMillis](../android.os/SystemClock.md))time base. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSource](InputEvent.md))`()` Gets the source of the event. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isFromSource](InputEvent.md))`(`source:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Determines whether the event is from the given source. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android.os/Parcelable.md))`(`dest:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Flatten this object in to a Parcel. <br /> | ||

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [InputEvent](InputEvent.md)!\> | [CREATOR](InputEvent.md) <br /> |

## Public methods

### describeContents

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) |

### getDevice

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDevice(): InputDevice!
```

Gets the device that this event came from.

| Return ||
|-----------------------------------------------------------------------------------------|---------------------------------|
| [InputDevice](InputDevice.md)! | The device, or null if unknown. |

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

- [android.view.InputDevice#getDevice](InputDevice.md)) 

### getEventTime

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getEventTime(): Long
```

Retrieve the time this event occurred, in the [android.os.SystemClock#uptimeMillis](../android.os/SystemClock.md))time base.

| Return ||
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | Returns the time this event occurred, in the [android.os.SystemClock#uptimeMillis](../android.os/SystemClock.md))time base. |

### getSource

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getSource(): Int
```

Gets the source of the event.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The event source or [InputDevice.SOURCE_UNKNOWN](InputDevice.md) if unknown. |

**See Also**

- [android.view.InputDevice#getSources](InputDevice.md)) 

### isFromSource

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isFromSource(source: Int): Boolean
```

Determines whether the event is from the given source.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `source` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The input source to check against. This can be a specific device type, such as [InputDevice.SOURCE_TOUCH_NAVIGATION](InputDevice.md), or a more generic device class, such as [InputDevice.SOURCE_CLASS_POINTER](InputDevice.md). |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Whether the event is from the given source. |

## Properties

### CREATOR

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<InputEvent!>
```
