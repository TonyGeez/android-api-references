# RoundedCorner

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RoundedCorner

Kotlin| [Java](https://developer.android.com/reference/android/view/RoundedCorner "View this page in Java") 
| --- | --- |

```
class RoundedCorner : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.RoundedCorner](https://developer.android.com/reference/kotlin/android/view/RoundedCorner#) |

Represents a rounded corner of the display.

<br />

Note: The rounded corner formed by the radius and the center is an approximation.

[RoundedCorner](https://developer.android.com/reference/kotlin/android/view/RoundedCorner#) is immutable.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [POSITION_BOTTOM_LEFT](https://developer.android.com/reference/kotlin/android/view/RoundedCorner#POSITION_BOTTOM_LEFT:kotlin.Int) The rounded corner is at the bottom-left of the screen. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [POSITION_BOTTOM_RIGHT](https://developer.android.com/reference/kotlin/android/view/RoundedCorner#POSITION_BOTTOM_RIGHT:kotlin.Int) The rounded corner is at the bottom-right of the screen. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [POSITION_TOP_LEFT](https://developer.android.com/reference/kotlin/android/view/RoundedCorner#POSITION_TOP_LEFT:kotlin.Int) The rounded corner is at the top-left of the screen. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [POSITION_TOP_RIGHT](https://developer.android.com/reference/kotlin/android/view/RoundedCorner#POSITION_TOP_RIGHT:kotlin.Int) The rounded corner is at the top-right of the screen. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [RoundedCorner](https://developer.android.com/reference/kotlin/android/view/RoundedCorner#RoundedCorner(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `radius:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `centerX:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `centerY:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a [RoundedCorner](https://developer.android.com/reference/kotlin/android/view/RoundedCorner#). |

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/view/RoundedCorner#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/view/RoundedCorner#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [Point](https://developer.android.com/reference/kotlin/android/graphics/Point.html#) | [getCenter](https://developer.android.com/reference/kotlin/android/view/RoundedCorner#getCenter())`()` Returns the circle center of a quarter circle approximation of this [RoundedCorner](https://developer.android.com/reference/kotlin/android/view/RoundedCorner#). |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPosition](https://developer.android.com/reference/kotlin/android/view/RoundedCorner#getPosition())`()` Get the position of this [RoundedCorner](https://developer.android.com/reference/kotlin/android/view/RoundedCorner#). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRadius](https://developer.android.com/reference/kotlin/android/view/RoundedCorner#getRadius())`()` Returns the radius of a quarter circle approximation of this [RoundedCorner](https://developer.android.com/reference/kotlin/android/view/RoundedCorner#). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/view/RoundedCorner#hashCode())`()` <br /> |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/view/RoundedCorner#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/view/RoundedCorner#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`out:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [RoundedCorner](https://developer.android.com/reference/kotlin/android/view/RoundedCorner#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/view/RoundedCorner#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### POSITION_BOTTOM_LEFT

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val POSITION_BOTTOM_LEFT: Int
```

The rounded corner is at the bottom-left of the screen. 

 Value: 3

### POSITION_BOTTOM_RIGHT

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val POSITION_BOTTOM_RIGHT: Int
```

The rounded corner is at the bottom-right of the screen. 

 Value: 2

### POSITION_TOP_LEFT

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val POSITION_TOP_LEFT: Int
```

The rounded corner is at the top-left of the screen. 

 Value: 0

### POSITION_TOP_RIGHT

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val POSITION_TOP_RIGHT: Int
```

The rounded corner is at the top-right of the screen. 

 Value: 1

## Public constructors

### RoundedCorner

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
RoundedCorner(
    position: Int, 
    radius: Int, 
    centerX: Int, 
    centerY: Int)
```

Creates a [RoundedCorner](https://developer.android.com/reference/kotlin/android/view/RoundedCorner#).

Note that this is only useful for tests. For production code, developers should always use a [RoundedCorner](https://developer.android.com/reference/kotlin/android/view/RoundedCorner#) obtained from the system via [WindowInsets.getRoundedCorner](https://developer.android.com/reference/kotlin/android/view/WindowInsets#getRoundedCorner(kotlin.Int))or [Display.getRoundedCorner](https://developer.android.com/reference/kotlin/android/view/Display#getRoundedCorner(kotlin.Int)).

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `position` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the position of the rounded corner. Value is [android.view.RoundedCorner#POSITION_TOP_LEFT](https://developer.android.com/reference/kotlin/android/view/RoundedCorner#POSITION_TOP_LEFT:kotlin.Int), [android.view.RoundedCorner#POSITION_TOP_RIGHT](https://developer.android.com/reference/kotlin/android/view/RoundedCorner#POSITION_TOP_RIGHT:kotlin.Int), [android.view.RoundedCorner#POSITION_BOTTOM_RIGHT](https://developer.android.com/reference/kotlin/android/view/RoundedCorner#POSITION_BOTTOM_RIGHT:kotlin.Int), or [android.view.RoundedCorner#POSITION_BOTTOM_LEFT](https://developer.android.com/reference/kotlin/android/view/RoundedCorner#POSITION_BOTTOM_LEFT:kotlin.Int) |
| `radius` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the radius of the rounded corner. |
| `centerX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the x of center point of the rounded corner. |
| --- | --- |
| `centerY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the y of center point of the rounded corner. |

## Public methods

### describeContents

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### equals

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getCenter

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCenter(): Point
```

Returns the circle center of a quarter circle approximation of this [RoundedCorner](https://developer.android.com/reference/kotlin/android/view/RoundedCorner#).

| Return ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Point](https://developer.android.com/reference/kotlin/android/graphics/Point.html#) | the center point of this [RoundedCorner](https://developer.android.com/reference/kotlin/android/view/RoundedCorner#) in the application's coordinate. This value cannot be`null`. |

### getPosition

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPosition(): Int
```

Get the position of this [RoundedCorner](https://developer.android.com/reference/kotlin/android/view/RoundedCorner#).

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.view.RoundedCorner#POSITION_TOP_LEFT](https://developer.android.com/reference/kotlin/android/view/RoundedCorner#POSITION_TOP_LEFT:kotlin.Int), [android.view.RoundedCorner#POSITION_TOP_RIGHT](https://developer.android.com/reference/kotlin/android/view/RoundedCorner#POSITION_TOP_RIGHT:kotlin.Int), [android.view.RoundedCorner#POSITION_BOTTOM_RIGHT](https://developer.android.com/reference/kotlin/android/view/RoundedCorner#POSITION_BOTTOM_RIGHT:kotlin.Int), or [android.view.RoundedCorner#POSITION_BOTTOM_LEFT](https://developer.android.com/reference/kotlin/android/view/RoundedCorner#POSITION_BOTTOM_LEFT:kotlin.Int) |

**See Also**

- [#POSITION_TOP_LEFT](https://developer.android.com/reference/kotlin/android/view/RoundedCorner#POSITION_TOP_LEFT:kotlin.Int)
- [#POSITION_TOP_RIGHT](https://developer.android.com/reference/kotlin/android/view/RoundedCorner#POSITION_TOP_RIGHT:kotlin.Int)
- [#POSITION_BOTTOM_RIGHT](https://developer.android.com/reference/kotlin/android/view/RoundedCorner#POSITION_BOTTOM_RIGHT:kotlin.Int)
- [#POSITION_BOTTOM_LEFT](https://developer.android.com/reference/kotlin/android/view/RoundedCorner#POSITION_BOTTOM_LEFT:kotlin.Int) 

### getRadius

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRadius(): Int
```

Returns the radius of a quarter circle approximation of this [RoundedCorner](https://developer.android.com/reference/kotlin/android/view/RoundedCorner#).

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the rounded corner radius of this [RoundedCorner](https://developer.android.com/reference/kotlin/android/view/RoundedCorner#). Returns 0 if there is no rounded corner. |

### hashCode

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### toString

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    out: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |
| `out` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):This value cannot be`null`. |
| --- | --- |

## Properties

### CREATOR

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<RoundedCorner!>
```
