# RoundedCorner

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RoundedCorner

Kotlin| [Java](RoundedCorner.md) 
| --- | --- |

```
class RoundedCorner : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.RoundedCorner](RoundedCorner.md) |

Represents a rounded corner of the display.

<br />

Note: The rounded corner formed by the radius and the center is an approximation.

[RoundedCorner](RoundedCorner.md) is immutable.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [POSITION_BOTTOM_LEFT](RoundedCorner.md) The rounded corner is at the bottom-left of the screen. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [POSITION_BOTTOM_RIGHT](RoundedCorner.md) The rounded corner is at the bottom-right of the screen. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [POSITION_TOP_LEFT](RoundedCorner.md) The rounded corner is at the top-left of the screen. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [POSITION_TOP_RIGHT](RoundedCorner.md) The rounded corner is at the top-right of the screen. |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [RoundedCorner](RoundedCorner.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `radius:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `centerX:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `centerY:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a [RoundedCorner](RoundedCorner.md). |

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](RoundedCorner.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](RoundedCorner.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [Point](../android.graphics/Point.md) | [getCenter](RoundedCorner.md))`()` Returns the circle center of a quarter circle approximation of this [RoundedCorner](RoundedCorner.md). |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPosition](RoundedCorner.md))`()` Get the position of this [RoundedCorner](RoundedCorner.md). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRadius](RoundedCorner.md))`()` Returns the radius of a quarter circle approximation of this [RoundedCorner](RoundedCorner.md). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](RoundedCorner.md))`()` <br /> |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](RoundedCorner.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](RoundedCorner.md))`(`out:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [RoundedCorner](RoundedCorner.md)!\> | [CREATOR](RoundedCorner.md) <br /> |

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

Creates a [RoundedCorner](RoundedCorner.md).

Note that this is only useful for tests. For production code, developers should always use a [RoundedCorner](RoundedCorner.md) obtained from the system via [WindowInsets.getRoundedCorner](WindowInsets.md))or [Display.getRoundedCorner](Display.md)).

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `position` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the position of the rounded corner. Value is [android.view.RoundedCorner#POSITION_TOP_LEFT](RoundedCorner.md), [android.view.RoundedCorner#POSITION_TOP_RIGHT](RoundedCorner.md), [android.view.RoundedCorner#POSITION_BOTTOM_RIGHT](RoundedCorner.md), or [android.view.RoundedCorner#POSITION_BOTTOM_LEFT](RoundedCorner.md) |
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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) |

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

Returns the circle center of a quarter circle approximation of this [RoundedCorner](RoundedCorner.md).

| Return ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Point](../android.graphics/Point.md) | the center point of this [RoundedCorner](RoundedCorner.md) in the application's coordinate. This value cannot be`null`. |

### getPosition

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPosition(): Int
```

Get the position of this [RoundedCorner](RoundedCorner.md).

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.view.RoundedCorner#POSITION_TOP_LEFT](RoundedCorner.md), [android.view.RoundedCorner#POSITION_TOP_RIGHT](RoundedCorner.md), [android.view.RoundedCorner#POSITION_BOTTOM_RIGHT](RoundedCorner.md), or [android.view.RoundedCorner#POSITION_BOTTOM_LEFT](RoundedCorner.md) |

**See Also**

- [#POSITION_TOP_LEFT](RoundedCorner.md)
- [#POSITION_TOP_RIGHT](RoundedCorner.md)
- [#POSITION_BOTTOM_RIGHT](RoundedCorner.md)
- [#POSITION_BOTTOM_LEFT](RoundedCorner.md) 

### getRadius

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRadius(): Int
```

Returns the radius of a quarter circle approximation of this [RoundedCorner](RoundedCorner.md).

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the rounded corner radius of this [RoundedCorner](RoundedCorner.md). Returns 0 if there is no rounded corner. |

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
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |
| `out` | [Parcel](../android.os/Parcel.md):This value cannot be`null`. |
| --- | --- |

## Properties

### CREATOR

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<RoundedCorner!>
```
