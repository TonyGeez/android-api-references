# WindowContentFrameStats

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WindowContentFrameStats

Kotlin| [Java](../android/view/WindowContentFrameStats.md) 
| --- | --- |

```
class WindowContentFrameStats : FrameStats, Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.view.FrameStats](../android/view/FrameStats.md) ||
| | ↳ | [android.view.WindowContentFrameStats](../android/view/WindowContentFrameStats.md) |

This class contains window content frame statistics. For example, a window content is rendred in frames when a view is scrolled. The frame statistics are a snapshot for the time interval from [getStartTimeNano()](../android/view/FrameStats.md))to [getEndTimeNano()](../android/view/FrameStats.md)).

The key idea is that in order to provide a smooth user experience an application has to draw a frame at a specific time interval obtained by calling [getRefreshPeriodNano()](../android/view/FrameStats.md)). If the application does not render a frame every refresh period the user will see irregular UI transitions.

An application posts a frame for presentation by synchronously rendering its contents in a buffer which is then posted or posting a buffer to which the application is asychronously rendering the content via GL. After the frame is posted and rendered (potentially asynchronosly) it is presented to the user. The time a frame was posted can be obtained via [getFramePostedTimeNano(int)](../android/view/WindowContentFrameStats.md)), the time a frame content was rendered and ready for dsiplay (GL case) via [getFrameReadyTimeNano(int)](../android/view/WindowContentFrameStats.md)), and the time a frame was presented on the screen via [getFramePresentedTimeNano(int)](../android/view/FrameStats.md)).

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||
| From class [FrameStats](../android/view/FrameStats.md) |------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [UNDEFINED_TIME_NANO](../android/view/FrameStats.md) <br /> Undefined time. <br /> | ||

| Public methods ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/view/WindowContentFrameStats.md))`()` <br /> |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getFramePostedTimeNano](../android/view/WindowContentFrameStats.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the time a frame at a given index was posted by the producer (e.g. the application). |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getFrameReadyTimeNano](../android/view/WindowContentFrameStats.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the time a frame at a given index was ready for presentation. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/view/WindowContentFrameStats.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/view/WindowContentFrameStats.md))`(`parcel:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Inherited functions ||
|---|---|
| From class [FrameStats](../android/view/FrameStats.md) |------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getEndTimeNano](../android/view/FrameStats.md))`()` <br /> Gets the end time of the interval for which these statistics apply. The end interval is the time when the last frame was presented. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getFrameCount](../android/view/FrameStats.md))`()` <br /> Gets the number of frames for which there is data. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getFramePresentedTimeNano](../android/view/FrameStats.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Get the time a frame at a given index was presented. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getRefreshPeriodNano](../android/view/FrameStats.md))`()` <br /> Gets the refresh period of the display hosting the window(s) for which these statistics apply. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getStartTimeNano](../android/view/FrameStats.md))`()` <br /> Gets the start time of the interval for which these statistics apply. The start interval is the time when the first frame was presented. <br /> | ||

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [WindowContentFrameStats](../android/view/WindowContentFrameStats.md)!\> | [CREATOR](../android/view/WindowContentFrameStats.md) <br /> |

## Public methods

### describeContents

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### getFramePostedTimeNano

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFramePostedTimeNano(index: Int): Long
```

Get the time a frame at a given index was posted by the producer (e.g. the application). It is either explicitly set or defaulted to the time when the render buffer was posted.

**Note:** A frame can be posted and still it contents being rendered asynchronously in GL. To get the time the frame content was completely rendered and ready to display call [getFrameReadyTimeNano(int)](../android/view/WindowContentFrameStats.md)).

| Parameters ||
|---------|---------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The frame index. |

| Return ||
|------------------------------------------------------------------------------|---------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The posted time in nanoseconds. |

### getFrameReadyTimeNano

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFrameReadyTimeNano(index: Int): Long
```

Get the time a frame at a given index was ready for presentation.

**Note:**A frame can be posted and still it contents being rendered asynchronously in GL. In such a case this is the time when the frame contents were completely rendered.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The frame index. |

| Return ||
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The ready time in nanoseconds or [UNDEFINED_TIME_NANO](../android/view/FrameStats.md) if the frame is not ready yet. |

### toString

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    parcel: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<WindowContentFrameStats!>
```
