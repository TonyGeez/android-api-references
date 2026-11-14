# Rect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Rect

Kotlin | [Java](https://developer.android.com/reference/android/graphics/Rect "View this page in Java") 

```
class Rect : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.graphics.Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect#) |

Rect holds four integer coordinates for a rectangle. The rectangle is represented by the coordinates of its 4 edges (left, top, right bottom). These fields can be accessed directly. Use width() and height() to retrieve the rectangle's width and height. Note: most methods do not check to see that the coordinates are sorted correctly (i.e. left \<= right and top \<= bottom).

Note that the right and bottom coordinates are exclusive. This means a Rect being drawn untransformed onto a [android.graphics.Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas) will draw into the column and row described by its left and top coordinates, but not those of its bottom and right.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect#Rect())`()` Create a new empty Rect. |
| [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect#Rect(android.graphics.Rect))`(`r:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect#)?`)` Create a new rectangle, initialized with the values in the specified rectangle (which is left unmodified). |
| [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect#Rect(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`left:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `top:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `right:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bottom:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create a new rectangle with the specified coordinates. |

| Public methods ||
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [centerX](https://developer.android.com/reference/kotlin/android/graphics/Rect#centerX())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [centerY](https://developer.android.com/reference/kotlin/android/graphics/Rect#centerY())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [contains](https://developer.android.com/reference/kotlin/android/graphics/Rect#contains(android.graphics.Rect))`(`r:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect#)`)` Returns true iff the specified rectangle r is inside or equal to this rectangle. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [contains](https://developer.android.com/reference/kotlin/android/graphics/Rect#contains(kotlin.Int,%20kotlin.Int))`(`x:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `y:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns true if (x,y) is inside the rectangle. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [contains](https://developer.android.com/reference/kotlin/android/graphics/Rect#contains(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`left:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `top:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `right:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bottom:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns true iff the 4 specified sides of a rectangle are inside or equal to this rectangle. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/graphics/Rect#describeContents())`()` Parcelable interface methods |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/graphics/Rect#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [exactCenterX](https://developer.android.com/reference/kotlin/android/graphics/Rect#exactCenterX())`()` <br /> |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [exactCenterY](https://developer.android.com/reference/kotlin/android/graphics/Rect#exactCenterY())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [flattenToString](https://developer.android.com/reference/kotlin/android/graphics/Rect#flattenToString())`()` Return a string representation of the rectangle in a well-defined format. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/graphics/Rect#hashCode())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [height](https://developer.android.com/reference/kotlin/android/graphics/Rect#height())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [inset](https://developer.android.com/reference/kotlin/android/graphics/Rect#inset(android.graphics.Insets))`(`insets:` ` [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets)`)` Insets the rectangle on all sides specified by the dimensions of `insets`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [inset](https://developer.android.com/reference/kotlin/android/graphics/Rect#inset(kotlin.Int,%20kotlin.Int))`(`dx:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dy:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Inset the rectangle by (dx,dy). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [inset](https://developer.android.com/reference/kotlin/android/graphics/Rect#inset(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`left:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `top:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `right:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bottom:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Insets the rectangle on all sides specified by the insets. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [intersect](https://developer.android.com/reference/kotlin/android/graphics/Rect#intersect(android.graphics.Rect))`(`r:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect#)`)` If the specified rectangle intersects this rectangle, return true and set this rectangle to that intersection, otherwise return false and do not change this rectangle. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [intersect](https://developer.android.com/reference/kotlin/android/graphics/Rect#intersect(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`left:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `top:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `right:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bottom:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` If the rectangle specified by left,top,right,bottom intersects this rectangle, return true and set this rectangle to that intersection, otherwise return false and do not change this rectangle. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [intersects](https://developer.android.com/reference/kotlin/android/graphics/Rect#intersects(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`left:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `top:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `right:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bottom:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns true if this rectangle intersects the specified rectangle. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [intersects](https://developer.android.com/reference/kotlin/android/graphics/Rect#intersects(android.graphics.Rect,%20android.graphics.Rect))`(`a:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect#)`, `b:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect#)`)` Returns true iff the two specified rectangles intersect. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](https://developer.android.com/reference/kotlin/android/graphics/Rect#isEmpty())`()` Returns true if the rectangle is empty (left \>= right or top \>= bottom) |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [offset](https://developer.android.com/reference/kotlin/android/graphics/Rect#offset(kotlin.Int,%20kotlin.Int))`(`dx:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dy:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Offset the rectangle by adding dx to its left and right coordinates, and adding dy to its top and bottom coordinates. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [offsetTo](https://developer.android.com/reference/kotlin/android/graphics/Rect#offsetTo(kotlin.Int,%20kotlin.Int))`(`newLeft:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newTop:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Offset the rectangle to a specific (left, top) position, keeping its width and height the same. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [readFromParcel](https://developer.android.com/reference/kotlin/android/graphics/Rect#readFromParcel(android.os.Parcel))`(`in:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`)` Set the rectangle's coordinates from the data stored in the specified parcel. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [set](https://developer.android.com/reference/kotlin/android/graphics/Rect#set(android.graphics.Rect))`(`src:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect#)`)` Copy the coordinates from src into this rectangle. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [set](https://developer.android.com/reference/kotlin/android/graphics/Rect#set(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`left:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `top:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `right:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bottom:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the rectangle's coordinates to the specified values. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEmpty](https://developer.android.com/reference/kotlin/android/graphics/Rect#setEmpty())`()` Set the rectangle to (0,0,0,0) |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setIntersect](https://developer.android.com/reference/kotlin/android/graphics/Rect#setIntersect(android.graphics.Rect,%20android.graphics.Rect))`(`a:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect#)`, `b:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect#)`)` If rectangles a and b intersect, return true and set this rectangle to that intersection, otherwise return false and do not change this rectangle. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sort](https://developer.android.com/reference/kotlin/android/graphics/Rect#sort())`()` Swap top/bottom or left/right if there are flipped (i.e. left \> right and/or top \> bottom). |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toShortString](https://developer.android.com/reference/kotlin/android/graphics/Rect#toShortString())`()` Return a string representation of the rectangle in a compact form. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/graphics/Rect#toString())`()` <br /> |
| static [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect#)? | [unflattenFromString](https://developer.android.com/reference/kotlin/android/graphics/Rect#unflattenFromString(kotlin.String))`(`str:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Returns a Rect from a string of the form returned by [flattenToString](https://developer.android.com/reference/kotlin/android/graphics/Rect#flattenToString()), or null if the string is not of that form. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [union](https://developer.android.com/reference/kotlin/android/graphics/Rect#union(android.graphics.Rect))`(`r:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect#)`)` Update this Rect to enclose itself and the specified rectangle. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [union](https://developer.android.com/reference/kotlin/android/graphics/Rect#union(kotlin.Int,%20kotlin.Int))`(`x:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `y:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Update this Rect to enclose itself and the \[x,y\] coordinate. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [union](https://developer.android.com/reference/kotlin/android/graphics/Rect#union(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`left:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `top:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `right:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bottom:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Update this Rect to enclose itself and the specified rectangle. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [width](https://developer.android.com/reference/kotlin/android/graphics/Rect#width())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/graphics/Rect#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`out:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Write this rectangle to the specified parcel. |

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/graphics/Rect#CREATOR:android.os.Parcelable.Creator) <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [bottom](https://developer.android.com/reference/kotlin/android/graphics/Rect#bottom:kotlin.Int) <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [left](https://developer.android.com/reference/kotlin/android/graphics/Rect#left:kotlin.Int) <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [right](https://developer.android.com/reference/kotlin/android/graphics/Rect#right:kotlin.Int) <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [top](https://developer.android.com/reference/kotlin/android/graphics/Rect#top:kotlin.Int) <br /> |

## Public constructors

### Rect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Rect()
```

Create a new empty Rect. All coordinates are initialized to 0. 

### Rect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Rect(r: Rect?)
```

Create a new rectangle, initialized with the values in the specified rectangle (which is left unmodified).

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `r` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect#)?: The rectangle whose coordinates are copied into the new rectangle. This value may be `null`. |

### Rect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Rect(
    left: Int, 
    top: Int, 
    right: Int, 
    bottom: Int)
```

Create a new rectangle with the specified coordinates. Note: no range checking is performed, so the caller must ensure that left \<= right and top \<= bottom.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------|
| `left` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The X coordinate of the left side of the rectangle |
| `top` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The Y coordinate of the top of the rectangle |
| `right` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The X coordinate of the right side of the rectangle |
| `bottom` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The Y coordinate of the bottom of the rectangle |

## Public methods

### centerX

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun centerX(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the horizontal center of the rectangle. If the computed value is fractional, this method returns the largest integer that is less than the computed value. |

### centerY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun centerY(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the vertical center of the rectangle. If the computed value is fractional, this method returns the largest integer that is less than the computed value. |

### contains

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun contains(r: Rect): Boolean
```

Returns true iff the specified rectangle r is inside or equal to this rectangle. An empty rectangle never contains another rectangle.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `r` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect#): The rectangle being tested for containment. This value cannot be `null`. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true iff the specified rectangle r is inside or equal to this rectangle |

### contains

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun contains(
    x: Int, 
    y: Int
): Boolean
```

Returns true if (x,y) is inside the rectangle. The left and top are considered to be inside, while the right and bottom are not. This means that for a x,y to be contained: left \<= x \< right and top \<= y \< bottom. An empty rectangle never contains any point.

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------------------------------------|
| `x` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The X coordinate of the point being tested for containment |
| `y` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The Y coordinate of the point being tested for containment |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true iff (x,y) are contained by the rectangle, where containment means left \<= x \< right and top \<= y \< bottom |

### contains

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun contains(
    left: Int, 
    top: Int, 
    right: Int, 
    bottom: Int
): Boolean
```

Returns true iff the 4 specified sides of a rectangle are inside or equal to this rectangle. i.e. is this rectangle a superset of the specified rectangle. An empty rectangle never contains another rectangle.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------|
| `left` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The left side of the rectangle being tested for containment |
| `top` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The top of the rectangle being tested for containment |
| `right` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The right side of the rectangle being tested for containment |
| `bottom` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The bottom of the rectangle being tested for containment |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true iff the 4 specified sides of a rectangle are inside or equal to this rectangle |

### describeContents

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

Parcelable interface methods

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true` if this object is the same as the obj argument; `false` otherwise. |

### exactCenterX

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun exactCenterX(): Float
```

| Return ||
|--------------------------------------------------------------------------------|----------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | the exact horizontal center of the rectangle as a float. |

### exactCenterY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun exactCenterY(): Float
```

| Return ||
|--------------------------------------------------------------------------------|--------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | the exact vertical center of the rectangle as a float. |

### flattenToString

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun flattenToString(): String
```

Return a string representation of the rectangle in a well-defined format.

You can later recover the Rect from this string through [unflattenFromString(java.lang.String)](https://developer.android.com/reference/kotlin/android/graphics/Rect#unflattenFromString(kotlin.String)).

| Return ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | Returns a new String of the form "left top right bottom" This value cannot be `null`. |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### height

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun height(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the rectangle's height. This does not check for a valid rectangle (i.e. top \<= bottom) so the result may be negative. |

### inset

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun inset(insets: Insets): Unit
```

Insets the rectangle on all sides specified by the dimensions of `insets`.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `insets` | [Insets](https://developer.android.com/reference/kotlin/android/graphics/Insets): The insets to inset the rect by. This value cannot be `null`. |

### inset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun inset(
    dx: Int, 
    dy: Int
): Unit
```

Inset the rectangle by (dx,dy). If dx is positive, then the sides are moved inwards, making the rectangle narrower. If dx is negative, then the sides are moved outwards, making the rectangle wider. The same holds true for dy and the top and bottom.

| Parameters ||
|------|------------------------------------------------------------------------------------------------------------------------------------------|
| `dx` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The amount to add(subtract) from the rectangle's left(right) |
| `dy` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The amount to add(subtract) from the rectangle's top(bottom) |

### inset

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun inset(
    left: Int, 
    top: Int, 
    right: Int, 
    bottom: Int
): Unit
```

Insets the rectangle on all sides specified by the insets.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------|
| `left` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The amount to add from the rectangle's left |
| `top` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The amount to add from the rectangle's top |
| `right` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The amount to subtract from the rectangle's right |
| `bottom` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The amount to subtract from the rectangle's bottom |

### intersect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun intersect(r: Rect): Boolean
```

If the specified rectangle intersects this rectangle, return true and set this rectangle to that intersection, otherwise return false and do not change this rectangle. No check is performed to see if either rectangle is empty. To just test for intersection, use intersects()

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `r` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect#): The rectangle being intersected with this rectangle. This value cannot be `null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the specified rectangle and this rectangle intersect (and this rectangle is then set to that intersection) else return false and do not change this rectangle. |

### intersect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun intersect(
    left: Int, 
    top: Int, 
    right: Int, 
    bottom: Int
): Boolean
```

If the rectangle specified by left,top,right,bottom intersects this rectangle, return true and set this rectangle to that intersection, otherwise return false and do not change this rectangle. No check is performed to see if either rectangle is empty. Note: To just test for intersection, use [intersects(android.graphics.Rect,android.graphics.Rect)](https://developer.android.com/reference/kotlin/android/graphics/Rect#intersects(android.graphics.Rect,%20android.graphics.Rect)).

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `left` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The left side of the rectangle being intersected with this rectangle |
| `top` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The top of the rectangle being intersected with this rectangle |
| `right` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The right side of the rectangle being intersected with this rectangle. |
| `bottom` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The bottom of the rectangle being intersected with this rectangle. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the specified rectangle and this rectangle intersect (and this rectangle is then set to that intersection) else return false and do not change this rectangle. |

### intersects

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun intersects(
    left: Int, 
    top: Int, 
    right: Int, 
    bottom: Int
): Boolean
```

Returns true if this rectangle intersects the specified rectangle. In no event is this rectangle modified. No check is performed to see if either rectangle is empty. To record the intersection, use intersect() or setIntersect().

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `left` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The left side of the rectangle being tested for intersection |
| `top` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The top of the rectangle being tested for intersection |
| `right` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The right side of the rectangle being tested for intersection |
| `bottom` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The bottom of the rectangle being tested for intersection |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true iff the specified rectangle intersects this rectangle. In no event is this rectangle modified. |

### intersects

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun intersects(
    a: Rect, 
    b: Rect
): Boolean
```

Returns true iff the two specified rectangles intersect. In no event are either of the rectangles modified. To record the intersection, use [intersect(android.graphics.Rect)](https://developer.android.com/reference/kotlin/android/graphics/Rect#intersect(android.graphics.Rect)) or [setIntersect(android.graphics.Rect,android.graphics.Rect)](https://developer.android.com/reference/kotlin/android/graphics/Rect#setIntersect(android.graphics.Rect,%20android.graphics.Rect)).

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `a` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect#): The first rectangle being tested for intersection This value cannot be `null`. |
| `b` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect#): The second rectangle being tested for intersection This value cannot be `null`. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true iff the two specified rectangles intersect. In no event are either of the rectangles modified. |

### isEmpty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isEmpty(): Boolean
```

Returns true if the rectangle is empty (left \>= right or top \>= bottom) 

### offset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun offset(
    dx: Int, 
    dy: Int
): Unit
```

Offset the rectangle by adding dx to its left and right coordinates, and adding dy to its top and bottom coordinates.

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `dx` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The amount to add to the rectangle's left and right coordinates |
| `dy` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The amount to add to the rectangle's top and bottom coordinates |

### offsetTo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun offsetTo(
    newLeft: Int, 
    newTop: Int
): Unit
```

Offset the rectangle to a specific (left, top) position, keeping its width and height the same.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------|
| `newLeft` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new "left" coordinate for the rectangle |
| `newTop` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new "top" coordinate for the rectangle |

### readFromParcel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun readFromParcel(in: Parcel): Unit
```

Set the rectangle's coordinates from the data stored in the specified parcel. To write a rectangle to a parcel, call writeToParcel().

| Parameters ||
|------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `in` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#): The parcel to read the rectangle's coordinates from This value cannot be `null`. |

### set

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun set(src: Rect): Unit
```

Copy the coordinates from src into this rectangle.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `src` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect#): The rectangle whose coordinates are copied into this rectangle. This value cannot be `null`. |

### set

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun set(
    left: Int, 
    top: Int, 
    right: Int, 
    bottom: Int
): Unit
```

Set the rectangle's coordinates to the specified values. Note: no range checking is performed, so it is up to the caller to ensure that left \<= right and top \<= bottom.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------|
| `left` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The X coordinate of the left side of the rectangle |
| `top` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The Y coordinate of the top of the rectangle |
| `right` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The X coordinate of the right side of the rectangle |
| `bottom` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The Y coordinate of the bottom of the rectangle |

### setEmpty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setEmpty(): Unit
```

Set the rectangle to (0,0,0,0) 

### setIntersect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setIntersect(
    a: Rect, 
    b: Rect
): Boolean
```

If rectangles a and b intersect, return true and set this rectangle to that intersection, otherwise return false and do not change this rectangle. No check is performed to see if either rectangle is empty. To just test for intersection, use intersects()

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `a` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect#): The first rectangle being intersected with This value cannot be `null`. |
| `b` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect#): The second rectangle being intersected with This value cannot be `null`. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true iff the two specified rectangles intersect. If they do, set this rectangle to that intersection. If they do not, return false and do not change this rectangle. |

### sort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun sort(): Unit
```

Swap top/bottom or left/right if there are flipped (i.e. left \> right and/or top \> bottom). This can be called if the edges are computed separately, and may have crossed over each other. If the edges are already correct (i.e. left \<= right and top \<= bottom) then nothing is done. 

### toShortString

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toShortString(): String
```

Return a string representation of the rectangle in a compact form.

| Return ||
|----------------------------------------------------------------------------------|------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be `null`. |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### unflattenFromString

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun unflattenFromString(str: String?): Rect?
```

Returns a Rect from a string of the form returned by [flattenToString](https://developer.android.com/reference/kotlin/android/graphics/Rect#flattenToString()), or null if the string is not of that form.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------|
| `str` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |

### union

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun union(r: Rect): Unit
```

Update this Rect to enclose itself and the specified rectangle. If the specified rectangle is empty, nothing is done. If this rectangle is empty it is set to the specified rectangle.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `r` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect#): The rectangle being unioned with this rectangle This value cannot be `null`. |

### union

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun union(
    x: Int, 
    y: Int
): Unit
```

Update this Rect to enclose itself and the \[x,y\] coordinate. There is no check to see that this rectangle is non-empty.

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------------------------------------|
| `x` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The x coordinate of the point to add to the rectangle |
| `y` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The y coordinate of the point to add to the rectangle |

### union

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun union(
    left: Int, 
    top: Int, 
    right: Int, 
    bottom: Int
): Unit
```

Update this Rect to enclose itself and the specified rectangle. If the specified rectangle is empty, nothing is done. If this rectangle is empty it is set to the specified rectangle.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| `left` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The left edge being unioned with this rectangle |
| `top` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The top edge being unioned with this rectangle |
| `right` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The right edge being unioned with this rectangle |
| `bottom` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The bottom edge being unioned with this rectangle |

### width

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun width(): Int
```

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the rectangle's width. This does not check for a valid rectangle (i.e. left \<= right) so the result may be negative. |

### writeToParcel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    out: Parcel, 
    flags: Int
): Unit
```

Write this rectangle to the specified parcel. To restore a rectangle from a parcel, use readFromParcel()

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either `0` or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |
| `out` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#): The parcel to write the rectangle's coordinates into |

## Properties

### CREATOR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<Rect!>
```  

### bottom

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var bottom: Int
```  

### left

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var left: Int
```  

### right

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var right: Int
```  

### top

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var top: Int
```
