# RectF

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RectF

Kotlin| [Java](../android/graphics/RectF.md) 
| --- | --- |

```
open class RectF : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.RectF](../android/graphics/RectF.md) |

RectF holds four float coordinates for a rectangle. The rectangle is represented by the coordinates of its 4 edges (left, top, right, bottom). These fields can be accessed directly. Use width() and height() to retrieve the rectangle's width and height. Note: most methods do not check to see that the coordinates are sorted correctly (i.e. left \<= right and top \<= bottom).

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [RectF](../android/graphics/RectF.md))`()` Create a new empty RectF. |
| [RectF](../android/graphics/RectF.md))`(`r:` ` [Rect](../android/graphics/Rect.md)?`)` <br /> |
| [RectF](../android/graphics/RectF.md))`(`r:` ` [RectF](../android/graphics/RectF.md)?`)` Create a new rectangle, initialized with the values in the specified rectangle (which is left unmodified). |
| [RectF](../android/graphics/RectF.md))`(`left:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `top:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `right:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `bottom:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Create a new rectangle with the specified coordinates. |

| Public methods ||
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [centerX](../android/graphics/RectF.md))`()` <br /> |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [centerY](../android/graphics/RectF.md))`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [contains](../android/graphics/RectF.md))`(`r:` ` [RectF](../android/graphics/RectF.md)`)` Returns true iff the specified rectangle r is inside or equal to this rectangle. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [contains](../android/graphics/RectF.md))`(`x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Returns true if (x,y) is inside the rectangle. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [contains](../android/graphics/RectF.md))`(`left:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `top:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `right:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `bottom:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Returns true iff the 4 specified sides of a rectangle are inside or equal to this rectangle. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/graphics/RectF.md))`()` Parcelable interface methods |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/graphics/RectF.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/graphics/RectF.md))`()` <br /> |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [height](../android/graphics/RectF.md))`()` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [inset](../android/graphics/RectF.md))`(`dx:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `dy:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Inset the rectangle by (dx,dy). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [intersect](../android/graphics/RectF.md))`(`r:` ` [RectF](../android/graphics/RectF.md)`)` If the specified rectangle intersects this rectangle, return true and set this rectangle to that intersection, otherwise return false and do not change this rectangle. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [intersect](../android/graphics/RectF.md))`(`left:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `top:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `right:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `bottom:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` If the rectangle specified by left,top,right,bottom intersects this rectangle, return true and set this rectangle to that intersection, otherwise return false and do not change this rectangle. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [intersects](../android/graphics/RectF.md))`(`left:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `top:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `right:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `bottom:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Returns true if this rectangle intersects the specified rectangle. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [intersects](../android/graphics/RectF.md))`(`a:` ` [RectF](../android/graphics/RectF.md)`, `b:` ` [RectF](../android/graphics/RectF.md)`)` Returns true iff the two specified rectangles intersect. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](../android/graphics/RectF.md))`()` Returns true if the rectangle is empty (left \>= right or top \>= bottom) |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [offset](../android/graphics/RectF.md))`(`dx:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `dy:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Offset the rectangle by adding dx to its left and right coordinates, and adding dy to its top and bottom coordinates. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [offsetTo](../android/graphics/RectF.md))`(`newLeft:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `newTop:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Offset the rectangle to a specific (left, top) position, keeping its width and height the same. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [readFromParcel](../android/graphics/RectF.md))`(`in:` ` [Parcel](../android/os/Parcel.md)`)` Set the rectangle's coordinates from the data stored in the specified parcel. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [round](../android/graphics/RectF.md))`(`dst:` ` [Rect](../android/graphics/Rect.md)`)` Set the dst integer Rect by rounding this rectangle's coordinates to their nearest integer values. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [roundOut](../android/graphics/RectF.md))`(`dst:` ` [Rect](../android/graphics/Rect.md)`)` Set the dst integer Rect by rounding "out" this rectangle, choosing the floor of top and left, and the ceiling of right and bottom. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [set](../android/graphics/RectF.md))`(`src:` ` [Rect](../android/graphics/Rect.md)`)` Copy the coordinates from src into this rectangle. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [set](../android/graphics/RectF.md))`(`src:` ` [RectF](../android/graphics/RectF.md)`)` Copy the coordinates from src into this rectangle. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [set](../android/graphics/RectF.md))`(`left:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `top:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `right:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `bottom:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Set the rectangle's coordinates to the specified values. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEmpty](../android/graphics/RectF.md))`()` Set the rectangle to (0,0,0,0) |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setIntersect](../android/graphics/RectF.md))`(`a:` ` [RectF](../android/graphics/RectF.md)`, `b:` ` [RectF](../android/graphics/RectF.md)`)` If rectangles a and b intersect, return true and set this rectangle to that intersection, otherwise return false and do not change this rectangle. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sort](../android/graphics/RectF.md))`()` Swap top/bottom or left/right if there are flipped (i.e. left \> right and/or top \> bottom). |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toShortString](../android/graphics/RectF.md))`()` Return a string representation of the rectangle in a compact form. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/graphics/RectF.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [union](../android/graphics/RectF.md))`(`r:` ` [RectF](../android/graphics/RectF.md)`)` Update this Rect to enclose itself and the specified rectangle. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [union](../android/graphics/RectF.md))`(`x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Update this Rect to enclose itself and the \[x,y\] coordinate. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [union](../android/graphics/RectF.md))`(`left:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `top:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `right:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `bottom:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Update this Rect to enclose itself and the specified rectangle. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [width](../android/graphics/RectF.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/graphics/RectF.md))`(`out:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Write this rectangle to the specified parcel. |
| --- | --- |

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [RectF](../android/graphics/RectF.md)!\> | [CREATOR](../android/graphics/RectF.md) <br /> |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [bottom](../android/graphics/RectF.md) <br /> |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [left](../android/graphics/RectF.md) <br /> |
| --- | --- |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [right](../android/graphics/RectF.md) <br /> |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [top](../android/graphics/RectF.md) <br /> |

## Public constructors

### RectF

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
RectF()
```

Create a new empty RectF. All coordinates are initialized to 0. 

### RectF

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
RectF(r: Rect?)
```

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------------|
| `r` | [Rect](../android/graphics/Rect.md)?:This value may be`null`. |

### RectF

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
RectF(r: RectF?)
```

Create a new rectangle, initialized with the values in the specified rectangle (which is left unmodified).

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `r` | [RectF](../android/graphics/RectF.md)?:The rectangle whose coordinates are copied into the new rectangle. This value may be`null`. |

### RectF

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
RectF(
    left: Float, 
    top: Float, 
    right: Float, 
    bottom: Float)
```

Create a new rectangle with the specified coordinates. Note: no range checking is performed, so the caller must ensure that left \<= right and top \<= bottom.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------|
| `left` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The X coordinate of the left side of the rectangle |
| `top` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The Y coordinate of the top of the rectangle |
| `right` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The X coordinate of the right side of the rectangle |
| --- | --- |
| `bottom` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The Y coordinate of the bottom of the rectangle |

## Public methods

### centerX

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun centerX(): Float
```

| Return ||
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | the horizontal center of the rectangle. This does not check for a valid rectangle (i.e. left \<= right) |

### centerY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun centerY(): Float
```

| Return ||
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | the vertical center of the rectangle. This does not check for a valid rectangle (i.e. top \<= bottom) |

### contains

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun contains(r: RectF): Boolean
```

Returns true iff the specified rectangle r is inside or equal to this rectangle. An empty rectangle never contains another rectangle.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `r` | [RectF](../android/graphics/RectF.md):The rectangle being tested for containment. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true iff the specified rectangle r is inside or equal to this rectangle |

### contains

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun contains(
    x: Float, 
    y: Float
): Boolean
```

Returns true if (x,y) is inside the rectangle. The left and top are considered to be inside, while the right and bottom are not. This means that for a x,y to be contained: left \<= x \< right and top \<= y \< bottom. An empty rectangle never contains any point.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------------------------------------------|
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The X coordinate of the point being tested for containment |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The Y coordinate of the point being tested for containment |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true iff (x,y) are contained by the rectangle, where containment means left \<= x \< right and top \<= y \< bottom |

### contains

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun contains(
    left: Float, 
    top: Float, 
    right: Float, 
    bottom: Float
): Boolean
```

Returns true iff the 4 specified sides of a rectangle are inside or equal to this rectangle. i.e. is this rectangle a superset of the specified rectangle. An empty rectangle never contains another rectangle.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `left` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The left side of the rectangle being tested for containment |
| `top` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The top of the rectangle being tested for containment |
| `right` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The right side of the rectangle being tested for containment |
| --- | --- |
| `bottom` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The bottom of the rectangle being tested for containment |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true iff the 4 specified sides of a rectangle are inside or equal to this rectangle |

### describeContents

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun describeContents(): Int
```

Parcelable interface methods

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### height

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun height(): Float
```

| Return ||
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | the rectangle's height. This does not check for a valid rectangle (i.e. top \<= bottom) so the result may be negative. |

### inset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun inset(
    dx: Float, 
    dy: Float
): Unit
```

Inset the rectangle by (dx,dy). If dx is positive, then the sides are moved inwards, making the rectangle narrower. If dx is negative, then the sides are moved outwards, making the rectangle wider. The same holds true for dy and the top and bottom.

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `dx` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The amount to add(subtract) from the rectangle's left(right) |
| `dy` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The amount to add(subtract) from the rectangle's top(bottom) |

### intersect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun intersect(r: RectF): Boolean
```

If the specified rectangle intersects this rectangle, return true and set this rectangle to that intersection, otherwise return false and do not change this rectangle. No check is performed to see if either rectangle is empty. To just test for intersection, use intersects()

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `r` | [RectF](../android/graphics/RectF.md):The rectangle being intersected with this rectangle. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the specified rectangle and this rectangle intersect (and this rectangle is then set to that intersection) else return false and do not change this rectangle. |

### intersect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun intersect(
    left: Float, 
    top: Float, 
    right: Float, 
    bottom: Float
): Boolean
```

If the rectangle specified by left,top,right,bottom intersects this rectangle, return true and set this rectangle to that intersection, otherwise return false and do not change this rectangle. No check is performed to see if either rectangle is empty. Note: To just test for intersection, use intersects()

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| `left` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The left side of the rectangle being intersected with this rectangle |
| `top` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The top of the rectangle being intersected with this rectangle |
| `right` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The right side of the rectangle being intersected with this rectangle. |
| --- | --- |
| `bottom` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The bottom of the rectangle being intersected with this rectangle. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the specified rectangle and this rectangle intersect (and this rectangle is then set to that intersection) else return false and do not change this rectangle. |

### intersects

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun intersects(
    left: Float, 
    top: Float, 
    right: Float, 
    bottom: Float
): Boolean
```

Returns true if this rectangle intersects the specified rectangle. In no event is this rectangle modified. No check is performed to see if either rectangle is empty. To record the intersection, use intersect() or setIntersect().

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `left` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The left side of the rectangle being tested for intersection |
| `top` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The top of the rectangle being tested for intersection |
| `right` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The right side of the rectangle being tested for intersection |
| --- | --- |
| `bottom` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The bottom of the rectangle being tested for intersection |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true iff the specified rectangle intersects this rectangle. In no event is this rectangle modified. |

### intersects

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun intersects(
    a: RectF, 
    b: RectF
): Boolean
```

Returns true iff the two specified rectangles intersect. In no event are either of the rectangles modified. To record the intersection, use intersect() or setIntersect().

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `a` | [RectF](../android/graphics/RectF.md):The first rectangle being tested for intersection This value cannot be`null`. |
| `b` | [RectF](../android/graphics/RectF.md):The second rectangle being tested for intersection This value cannot be`null`. |

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
open fun offset(
    dx: Float, 
    dy: Float
): Unit
```

Offset the rectangle by adding dx to its left and right coordinates, and adding dy to its top and bottom coordinates.

| Parameters ||
|------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `dx` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The amount to add to the rectangle's left and right coordinates |
| `dy` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The amount to add to the rectangle's top and bottom coordinates |

### offsetTo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun offsetTo(
    newLeft: Float, 
    newTop: Float
): Unit
```

Offset the rectangle to a specific (left, top) position, keeping its width and height the same.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------|
| `newLeft` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The new "left" coordinate for the rectangle |
| `newTop` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The new "top" coordinate for the rectangle |

### readFromParcel

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun readFromParcel(in: Parcel): Unit
```

Set the rectangle's coordinates from the data stored in the specified parcel. To write a rectangle to a parcel, call writeToParcel().

| Parameters ||
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `in` | [Parcel](../android/os/Parcel.md):The parcel to read the rectangle's coordinates from This value cannot be`null`. |

### round

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun round(dst: Rect): Unit
```

Set the dst integer Rect by rounding this rectangle's coordinates to their nearest integer values.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------|
| `dst` | [Rect](../android/graphics/Rect.md):This value cannot be`null`. |

### roundOut

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun roundOut(dst: Rect): Unit
```

Set the dst integer Rect by rounding "out" this rectangle, choosing the floor of top and left, and the ceiling of right and bottom.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------|
| `dst` | [Rect](../android/graphics/Rect.md):This value cannot be`null`. |

### set

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun set(src: Rect): Unit
```

Copy the coordinates from src into this rectangle.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `src` | [Rect](../android/graphics/Rect.md):The rectangle whose coordinates are copied into this rectangle. This value cannot be`null`. |

### set

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun set(src: RectF): Unit
```

Copy the coordinates from src into this rectangle.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `src` | [RectF](../android/graphics/RectF.md):The rectangle whose coordinates are copied into this rectangle. This value cannot be`null`. |

### set

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun set(
    left: Float, 
    top: Float, 
    right: Float, 
    bottom: Float
): Unit
```

Set the rectangle's coordinates to the specified values. Note: no range checking is performed, so it is up to the caller to ensure that left \<= right and top \<= bottom.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------|
| `left` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The X coordinate of the left side of the rectangle |
| `top` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The Y coordinate of the top of the rectangle |
| `right` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The X coordinate of the right side of the rectangle |
| --- | --- |
| `bottom` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The Y coordinate of the bottom of the rectangle |

### setEmpty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setEmpty(): Unit
```

Set the rectangle to (0,0,0,0) 

### setIntersect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setIntersect(
    a: RectF, 
    b: RectF
): Boolean
```

If rectangles a and b intersect, return true and set this rectangle to that intersection, otherwise return false and do not change this rectangle. No check is performed to see if either rectangle is empty. To just test for intersection, use intersects()

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `a` | [RectF](../android/graphics/RectF.md):The first rectangle being intersected with This value cannot be`null`. |
| `b` | [RectF](../android/graphics/RectF.md):The second rectangle being intersected with This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true iff the two specified rectangles intersect. If they do, set this rectangle to that intersection. If they do not, return false and do not change this rectangle. |

### sort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun sort(): Unit
```

Swap top/bottom or left/right if there are flipped (i.e. left \> right and/or top \> bottom). This can be called if the edges are computed separately, and may have crossed over each other. If the edges are already correct (i.e. left \<= right and top \<= bottom) then nothing is done. 

### toShortString

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toShortString(): String
```

Return a string representation of the rectangle in a compact form.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### union

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun union(r: RectF): Unit
```

Update this Rect to enclose itself and the specified rectangle. If the specified rectangle is empty, nothing is done. If this rectangle is empty it is set to the specified rectangle.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `r` | [RectF](../android/graphics/RectF.md):The rectangle being unioned with this rectangle This value cannot be`null`. |

### union

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun union(
    x: Float, 
    y: Float
): Unit
```

Update this Rect to enclose itself and the \[x,y\] coordinate. There is no check to see that this rectangle is non-empty.

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------------------------------------------|
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The x coordinate of the point to add to the rectangle |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The y coordinate of the point to add to the rectangle |

### union

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun union(
    left: Float, 
    top: Float, 
    right: Float, 
    bottom: Float
): Unit
```

Update this Rect to enclose itself and the specified rectangle. If the specified rectangle is empty, nothing is done. If this rectangle is empty it is set to the specified rectangle.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------|
| `left` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The left edge being unioned with this rectangle |
| `top` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The top edge being unioned with this rectangle |
| `right` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The right edge being unioned with this rectangle |
| --- | --- |
| `bottom` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The bottom edge being unioned with this rectangle |

### width

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun width(): Float
```

| Return ||
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | the rectangle's width. This does not check for a valid rectangle (i.e. left \<= right) so the result may be negative. |

### writeToParcel

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeToParcel(
    out: Parcel, 
    flags: Int
): Unit
```

Write this rectangle to the specified parcel. To restore a rectangle from a parcel, use readFromParcel()

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |
| `out` | [Parcel](../android/os/Parcel.md):The parcel to write the rectangle's coordinates into |
| --- | --- |

## Properties

### CREATOR

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<RectF!>
```  

### bottom

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var bottom: Float
```  

### left

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var left: Float
```  

### right

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var right: Float
```  

### top

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var top: Float
```
