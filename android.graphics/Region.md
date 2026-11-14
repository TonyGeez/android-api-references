# Region

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Region

Kotlin| [Java](../android/graphics/Region.md) 
| --- | --- |

```
open class Region : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.Region](../android/graphics/Region.md) |

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------|
| | [Op](../android/graphics/Region.Op.md) <br /> |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Region](../android/graphics/Region.md))`()` Create an empty region |
| [Region](../android/graphics/Region.md))`(`r:` ` [Rect](../android/graphics/Rect.md)`)` Return a region set to the specified rectangle |
| [Region](../android/graphics/Region.md))`(`region:` ` [Region](../android/graphics/Region.md)`)` Return a copy of the specified region |
| [Region](../android/graphics/Region.md))`(`left:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `top:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `right:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bottom:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return a region set to the specified rectangle |

| Public methods ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [contains](../android/graphics/Region.md))`(`x:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `y:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return true if the region contains the specified point |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/graphics/Region.md))`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/graphics/Region.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| --- | --- |
| open [Path](../android/graphics/Path.md) | [getBoundaryPath](../android/graphics/Region.md))`()` Return the boundary of the region as a new Path. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getBoundaryPath](../android/graphics/Region.md))`(`path:` ` [Path](../android/graphics/Path.md)`)` Set the path to the boundary of the region. |
| open [Rect](../android/graphics/Rect.md) | [getBounds](../android/graphics/Region.md))`()` Return a new Rect set to the bounds of the region. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getBounds](../android/graphics/Region.md))`(`r:` ` [Rect](../android/graphics/Rect.md)`)` Set the Rect to the bounds of the region. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isComplex](../android/graphics/Region.md))`()` Return true if the region contains more than one rectangle |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](../android/graphics/Region.md))`()` Return true if this region is empty |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRect](../android/graphics/Region.md))`()` Return true if the region contains a single rectangle |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [op](../android/graphics/Region.md))`(`rect:` ` [Rect](../android/graphics/Rect.md)`, `region:` ` [Region](../android/graphics/Region.md)`, `op:` ` [Region.Op](../android/graphics/Region.Op.md)`)` Set this region to the result of performing the Op on the specified rect and region. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [op](../android/graphics/Region.md))`(`r:` ` [Rect](../android/graphics/Rect.md)`, `op:` ` [Region.Op](../android/graphics/Region.Op.md)`)` Perform the specified Op on this region and the specified rect. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [op](../android/graphics/Region.md))`(`region1:` ` [Region](../android/graphics/Region.md)`, `region2:` ` [Region](../android/graphics/Region.md)`, `op:` ` [Region.Op](../android/graphics/Region.Op.md)`)` Set this region to the result of performing the Op on the specified regions. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [op](../android/graphics/Region.md))`(`region:` ` [Region](../android/graphics/Region.md)`, `op:` ` [Region.Op](../android/graphics/Region.Op.md)`)` Perform the specified Op on this region and the specified region. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [op](../android/graphics/Region.md))`(`left:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `top:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `right:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bottom:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `op:` ` [Region.Op](../android/graphics/Region.Op.md)`)` Perform the specified Op on this region and the specified rect. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [quickContains](../android/graphics/Region.md))`(`r:` ` [Rect](../android/graphics/Rect.md)`)` Return true if the region is a single rectangle (not complex) and it contains the specified rectangle. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [quickContains](../android/graphics/Region.md))`(`left:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `top:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `right:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bottom:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return true if the region is a single rectangle (not complex) and it contains the specified rectangle. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [quickReject](../android/graphics/Region.md))`(`r:` ` [Rect](../android/graphics/Rect.md)`)` Return true if the region is empty, or if the specified rectangle does not intersect the region. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [quickReject](../android/graphics/Region.md))`(`rgn:` ` [Region](../android/graphics/Region.md)!`)` Return true if the region is empty, or if the specified region does not intersect the region. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [quickReject](../android/graphics/Region.md))`(`left:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `top:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `right:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bottom:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return true if the region is empty, or if the specified rectangle does not intersect the region. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [set](../android/graphics/Region.md))`(`r:` ` [Rect](../android/graphics/Rect.md)`)` Set the region to the specified rectangle |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [set](../android/graphics/Region.md))`(`region:` ` [Region](../android/graphics/Region.md)`)` Set the region to the specified region. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [set](../android/graphics/Region.md))`(`left:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `top:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `right:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bottom:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the region to the specified rectangle |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEmpty](../android/graphics/Region.md))`()` Set the region to the empty region |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setPath](../android/graphics/Region.md))`(`path:` ` [Path](../android/graphics/Path.md)`, `clip:` ` [Region](../android/graphics/Region.md)`)` Set the region to the area described by the path and clip. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/graphics/Region.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [translate](../android/graphics/Region.md))`(`dx:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dy:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Translate the region by \[dx, dy\]. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [translate](../android/graphics/Region.md))`(`dx:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dy:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dst:` ` [Region](../android/graphics/Region.md)!`)` Set the dst region to the result of translating this region by \[dx, dy\]. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [union](../android/graphics/Region.md))`(`r:` ` [Rect](../android/graphics/Rect.md)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/graphics/Region.md))`(`p:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Write the region and its pixels to the parcel. |
| --- | --- |

| Protected methods ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](../android/graphics/Region.md))`()` <br /> |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [Region](../android/graphics/Region.md)!\> | [CREATOR](../android/graphics/Region.md) <br /> |

## Public constructors

### Region

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Region()
```

Create an empty region 

### Region

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Region(r: Rect)
```

Return a region set to the specified rectangle

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------|
| `r` | [Rect](../android/graphics/Rect.md):This value cannot be`null`. |

### Region

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Region(region: Region)
```

Return a copy of the specified region

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------|
| `region` | [Region](../android/graphics/Region.md):This value cannot be`null`. |

### Region

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Region(
    left: Int, 
    top: Int, 
    right: Int, 
    bottom: Int)
```

Return a region set to the specified rectangle

## Public methods

### contains

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun contains(
    x: Int, 
    y: Int
): Boolean
```

Return true if the region contains the specified point 

### describeContents

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun describeContents(): Int
```

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

### getBoundaryPath

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getBoundaryPath(): Path
```

Return the boundary of the region as a new Path. If the region is empty, the path will also be empty.

| Return ||
|------------------------------------------------------------------------------|-----------------------------|
| [Path](../android/graphics/Path.md) | This value cannot be`null`. |

### getBoundaryPath

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getBoundaryPath(path: Path): Boolean
```

Set the path to the boundary of the region. If the region is empty, the path will also be empty.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------|
| `path` | [Path](../android/graphics/Path.md):This value cannot be`null`. |

### getBounds

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getBounds(): Rect
```

Return a new Rect set to the bounds of the region. If the region is empty, the Rect will be set to \[0, 0, 0, 0\]

| Return ||
|------------------------------------------------------------------------------|-----------------------------|
| [Rect](../android/graphics/Rect.md) | This value cannot be`null`. |

### getBounds

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getBounds(r: Rect): Boolean
```

Set the Rect to the bounds of the region. If the region is empty, the Rect will be set to \[0, 0, 0, 0\]

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------|
| `r` | [Rect](../android/graphics/Rect.md):This value cannot be`null`. |

### isComplex

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isComplex(): Boolean
```

Return true if the region contains more than one rectangle 

### isEmpty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isEmpty(): Boolean
```

Return true if this region is empty 

### isRect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isRect(): Boolean
```

Return true if the region contains a single rectangle 

### op

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun op(
    rect: Rect, 
    region: Region, 
    op: Region.Op
): Boolean
```

Set this region to the result of performing the Op on the specified rect and region. Return true if the result is not empty.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------|
| `rect` | [Rect](../android/graphics/Rect.md):This value cannot be`null`. |
| `region` | [Region](../android/graphics/Region.md):This value cannot be`null`. |
| `op` | [Region.Op](../android/graphics/Region.Op.md):This value cannot be`null`. |
| --- | --- |

### op

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun op(
    r: Rect, 
    op: Region.Op
): Boolean
```

Perform the specified Op on this region and the specified rect. Return true if the result of the op is not empty.

| Parameters ||
|------|--------------------------------------------------------------------------------------------------------------------|
| `r` | [Rect](../android/graphics/Rect.md):This value cannot be`null`. |
| `op` | [Region.Op](../android/graphics/Region.Op.md):This value cannot be`null`. |

### op

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun op(
    region1: Region, 
    region2: Region, 
    op: Region.Op
): Boolean
```

Set this region to the result of performing the Op on the specified regions. Return true if the result is not empty.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------|
| `region1` | [Region](../android/graphics/Region.md):This value cannot be`null`. |
| `region2` | [Region](../android/graphics/Region.md):This value cannot be`null`. |
| `op` | [Region.Op](../android/graphics/Region.Op.md):This value cannot be`null`. |
| --- | --- |

### op

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun op(
    region: Region, 
    op: Region.Op
): Boolean
```

Perform the specified Op on this region and the specified region. Return true if the result of the op is not empty.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------|
| `region` | [Region](../android/graphics/Region.md):This value cannot be`null`. |
| `op` | [Region.Op](../android/graphics/Region.Op.md):This value cannot be`null`. |

### op

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun op(
    left: Int, 
    top: Int, 
    right: Int, 
    bottom: Int, 
    op: Region.Op
): Boolean
```

Perform the specified Op on this region and the specified rect. Return true if the result of the op is not empty.

| Parameters ||
|------|--------------------------------------------------------------------------------------------------------------------|
| `op` | [Region.Op](../android/graphics/Region.Op.md):This value cannot be`null`. |

### quickContains

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun quickContains(r: Rect): Boolean
```

Return true if the region is a single rectangle (not complex) and it contains the specified rectangle. Returning false is not a guarantee that the rectangle is not contained by this region, but return true is a guarantee that the rectangle is contained by this region.

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------|
| `r` | [Rect](../android/graphics/Rect.md):This value cannot be`null`. |

### quickContains

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun quickContains(
    left: Int, 
    top: Int, 
    right: Int, 
    bottom: Int
): Boolean
```

Return true if the region is a single rectangle (not complex) and it contains the specified rectangle. Returning false is not a guarantee that the rectangle is not contained by this region, but return true is a guarantee that the rectangle is contained by this region. 

### quickReject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun quickReject(r: Rect): Boolean
```

Return true if the region is empty, or if the specified rectangle does not intersect the region. Returning false is not a guarantee that they intersect, but returning true is a guarantee that they do not.

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------|
| `r` | [Rect](../android/graphics/Rect.md):This value cannot be`null`. |

### quickReject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun quickReject(rgn: Region!): Boolean
```

Return true if the region is empty, or if the specified region does not intersect the region. Returning false is not a guarantee that they intersect, but returning true is a guarantee that they do not. 

### quickReject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun quickReject(
    left: Int, 
    top: Int, 
    right: Int, 
    bottom: Int
): Boolean
```

Return true if the region is empty, or if the specified rectangle does not intersect the region. Returning false is not a guarantee that they intersect, but returning true is a guarantee that they do not. 

### set

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun set(r: Rect): Boolean
```

Set the region to the specified rectangle

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------|
| `r` | [Rect](../android/graphics/Rect.md):This value cannot be`null`. |

### set

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun set(region: Region): Boolean
```

Set the region to the specified region.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------|
| `region` | [Region](../android/graphics/Region.md):This value cannot be`null`. |

### set

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun set(
    left: Int, 
    top: Int, 
    right: Int, 
    bottom: Int
): Boolean
```

Set the region to the specified rectangle 

### setEmpty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setEmpty(): Unit
```

Set the region to the empty region 

### setPath

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPath(
    path: Path, 
    clip: Region
): Boolean
```

Set the region to the area described by the path and clip. Return true if the resulting region is non-empty. This produces a region that is identical to the pixels that would be drawn by the path (with no antialiasing).

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------|
| `path` | [Path](../android/graphics/Path.md):This value cannot be`null`. |
| `clip` | [Region](../android/graphics/Region.md):This value cannot be`null`. |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### translate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun translate(
    dx: Int, 
    dy: Int
): Unit
```

Translate the region by \[dx, dy\]. If the region is empty, do nothing. 

### translate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun translate(
    dx: Int, 
    dy: Int, 
    dst: Region!
): Unit
```

Set the dst region to the result of translating this region by \[dx, dy\]. If this region is empty, then dst will be set to empty. 

### union

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun union(r: Rect): Boolean
```

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------|
| `r` | [Rect](../android/graphics/Rect.md):This value cannot be`null`. |

### writeToParcel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeToParcel(
    p: Parcel, 
    flags: Int
): Unit
```

Write the region and its pixels to the parcel. The region can be rebuilt from the parcel by calling CREATOR.createFromParcel().

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |
| `p` | [Parcel](../android/os/Parcel.md):Parcel object to write the region data into |
| --- | --- |

## Protected methods

### finalize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun finalize(): Unit
```

| Exceptions ||
|-----------------------|-------------------------------------|
| `java.lang.Throwable` | the`Exception`raised by this method |

## Properties

### CREATOR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<Region!>
```
