Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AppWidgetEvent

Kotlin | [Java](../android/appwidget/AppWidgetEvent.md)
| --- | --- |

```
class AppWidgetEvent : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.appwidget.AppWidgetEvent](../android/appwidget/AppWidgetEvent.md) |

An immutable class that describes the event data for an app widget interaction event.

## Summary

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetEvent#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetEvent#getAppWidgetId()()` The app widget ID of the widget that generated this event. |
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)? | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetEvent#getClickedIds()()` This returns the set of View IDs of the views which have been clicked during the event time range. |
| --- | --- |
| [Instant](../java/time/Instant.md) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetEvent#getEnd()()` Describes the end of the time range that this event contains data for. |
| [Rect](../android/graphics/Rect.md)? | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetEvent#getPosition()()` This rect with describes the global coordinates of the widget at the end of the event time range. |
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)? | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetEvent#getScrolledIds()()` This returns the set of View IDs of the views which have been scrolled during the event time range. |
| --- | --- |
| [Instant](../java/time/Instant.md) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetEvent#getStart()()` Describes the start of the time range that this event contains data for. |
| [Duration](../java/time/Duration.md) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetEvent#getVisibleDuration()()` Describes the total duration of time during which the widget was visible. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetEvent#toString()()` Returns a string representation of the object. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetEvent#writeToParcel(android.os.Parcel,%20kotlin.Int)(out: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [AppWidgetEvent](../android/appwidget/AppWidgetEvent.md)!\> | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetEvent#CREATOR:android.os.Parcelable.Creator` Parcelable. |

## Public methods

### describeContents

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getAppWidgetId

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAppWidgetId(): Int
```

The app widget ID of the widget that generated this event.
**See Also**

- `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#getAppWidgetInfo(kotlin.Int)`

### getClickedIds

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getClickedIds(): IntArray?
```

This returns the set of View IDs of the views which have been clicked during the event time range. Use `https://developer.android.com/reference/kotlin/android/widget/RemoteViews.html#setAppWidgetEventTag(kotlin.Int,%20kotlin.Int)` to set a custom integer tag on a view for reporting clicks. If the tag is set, it will be used here instead of the View ID.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html?` | This value may be `null`. |

### getEnd

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getEnd(): Instant
```

Describes the end of the time range that this event contains data for.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/Instant.html#` | This value cannot be `null`. |

### getPosition

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPosition(): Rect?
```

This rect with describes the global coordinates of the widget at the end of the event time range.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Rect.html#?` | This value may be `null`. |

### getScrolledIds

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getScrolledIds(): IntArray?
```

This returns the set of View IDs of the views which have been scrolled during the event time range. Use `https://developer.android.com/reference/kotlin/android/widget/RemoteViews.html#setAppWidgetEventTag(kotlin.Int,%20kotlin.Int)` to set a custom integer tag on a view for reporting scrolls. If the tag is set, it will be used here instead of the View ID.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html?` | This value may be `null`. |

### getStart

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getStart(): Instant
```

Describes the start of the time range that this event contains data for.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/Instant.html#` | This value cannot be `null`. |

### getVisibleDuration

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getVisibleDuration(): Duration
```

Describes the total duration of time during which the widget was visible. This may be different than the event time range (between `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetEvent#getStart()` and `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetEvent#getEnd()` if the widget was hidden and shown multiple times during the event time range.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/Duration.html#` | This value cannot be `null`. |

### toString

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    out: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |
| `out` | [Parcel](../android/os/Parcel.md): This value cannot be `null`. |
| --- | --- |

## Properties

### CREATOR

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<AppWidgetEvent!>
```

Parcelable.Creator that instantiates AppWidgetEvent objects
