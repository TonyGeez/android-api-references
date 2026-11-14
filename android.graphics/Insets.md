# Insets

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Insets

Kotlin| [Java](https://developer.android.com/reference/android/graphics/Insets "View this page in Java") 
| --- | --- |

```
class Insets : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets#) |

An Insets instance holds four integer offsets which describe changes to the four edges of a Rectangle. By convention, positive values move edges towards the centre of the rectangle.

Insets are immutable so may be treated as values.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets#) | [add](https://developer.android.com/reference/kotlin/android/graphics/Insets#add(android.graphics.Insets,%20android.graphics.Insets))`(`a:` ` [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets#)`, `b:` ` [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets#)`)` Add two Insets. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/graphics/Insets#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/graphics/Insets#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Two Insets instances are equal iff they belong to the same class and their fields are pairwise equal. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/graphics/Insets#hashCode())`()` <br /> |
| static [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets#) | [max](https://developer.android.com/reference/kotlin/android/graphics/Insets#max(android.graphics.Insets,%20android.graphics.Insets))`(`a:` ` [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets#)`, `b:` ` [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets#)`)` Retrieves the maximum of two Insets. |
| static [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets#) | [min](https://developer.android.com/reference/kotlin/android/graphics/Insets#min(android.graphics.Insets,%20android.graphics.Insets))`(`a:` ` [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets#)`, `b:` ` [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets#)`)` Retrieves the minimum of two Insets. |
| --- | --- |
| static [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets#) | [of](https://developer.android.com/reference/kotlin/android/graphics/Insets#of(android.graphics.Rect))`(`r:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect)?`)` Return an Insets instance with the appropriate values. |
| static [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets#) | [of](https://developer.android.com/reference/kotlin/android/graphics/Insets#of(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`left:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `top:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `right:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bottom:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return an Insets instance with the appropriate values. |
| static [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets#) | [subtract](https://developer.android.com/reference/kotlin/android/graphics/Insets#subtract(android.graphics.Insets,%20android.graphics.Insets))`(`a:` ` [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets#)`, `b:` ` [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets#)`)` Subtract two Insets. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/graphics/Insets#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/graphics/Insets#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`out:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/graphics/Insets#CREATOR:android.os.Parcelable.Creator) <br /> |
| static [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets#) | [NONE](https://developer.android.com/reference/kotlin/android/graphics/Insets#NONE:android.graphics.Insets) <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [bottom](https://developer.android.com/reference/kotlin/android/graphics/Insets#bottom:kotlin.Int) <br /> |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [left](https://developer.android.com/reference/kotlin/android/graphics/Insets#left:kotlin.Int) <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [right](https://developer.android.com/reference/kotlin/android/graphics/Insets#right:kotlin.Int) <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [top](https://developer.android.com/reference/kotlin/android/graphics/Insets#top:kotlin.Int) <br /> |
| --- | --- |

## Public methods

### add

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun add(
    a: Insets, 
    b: Insets
): Insets
```

Add two Insets.

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------------------------------------------|
| `a` | [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets#):The first Insets to add. This value cannot be`null`. |
| `b` | [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets#):The second Insets to add. This value cannot be`null`. |

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets#) | a + b, i. e. all insets on every side are added together. This value cannot be`null`. |

### describeContents

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### equals

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Two Insets instances are equal iff they belong to the same class and their fields are pairwise equal.

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |
| `o` | the object to compare this instance with. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true iff this object is equal`o` |

### hashCode

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### max

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun max(
    a: Insets, 
    b: Insets
): Insets
```

Retrieves the maximum of two Insets.

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------------------------------|
| `a` | [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets#):The first Insets. This value cannot be`null`. |
| `b` | [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets#):The second Insets. This value cannot be`null`. |

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets#) | max(a, b), i. e. the larger of every inset on every side is taken for the result. This value cannot be`null`. |

### min

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun min(
    a: Insets, 
    b: Insets
): Insets
```

Retrieves the minimum of two Insets.

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------------------------------|
| `a` | [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets#):The first Insets. This value cannot be`null`. |
| `b` | [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets#):The second Insets. This value cannot be`null`. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets#) | min(a, b), i. e. the smaller of every inset on every side is taken for the result. This value cannot be`null`. |

### of

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun of(r: Rect?): Insets
```

Return an Insets instance with the appropriate values.

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `r` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect)?:the rectangle from which to take the values This value may be`null`. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets#) | an Insets instance with the appropriate values This value cannot be`null`. |

### of

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun of(
    left: Int, 
    top: Int, 
    right: Int, 
    bottom: Int
): Insets
```

Return an Insets instance with the appropriate values.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------|
| `left` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the left inset |
| `top` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the top inset |
| `right` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the right inset |
| --- | --- |
| `bottom` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the bottom inset |

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets#) | Insets instance with the appropriate values This value cannot be`null`. |

### subtract

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun subtract(
    a: Insets, 
    b: Insets
): Insets
```

Subtract two Insets.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------------------------------|
| `a` | [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets#):The minuend. This value cannot be`null`. |
| `b` | [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets#):The subtrahend. This value cannot be`null`. |

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets#) | a - b, i. e. all insets on every side are subtracted from each other. This value cannot be`null`. |

### toString

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    out: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<Insets!>
```  

### NONE

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NONE: Insets
```  

### bottom

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val bottom: Int
```  

### left

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val left: Int
```  

### right

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val right: Int
```  

### top

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val top: Int
```
