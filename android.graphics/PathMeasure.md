# PathMeasure

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PathMeasure

Kotlin| [Java](../android/graphics/PathMeasure.md) 
| --- | --- |

```
open class PathMeasure
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.PathMeasure](../android/graphics/PathMeasure.md) |

## Summary

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [POSITION_MATRIX_FLAG](../android/graphics/PathMeasure.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TANGENT_MATRIX_FLAG](../android/graphics/PathMeasure.md) <br /> |

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PathMeasure](../android/graphics/PathMeasure.md))`()` Create an empty PathMeasure object. |
| [PathMeasure](../android/graphics/PathMeasure.md))`(`path:` ` [Path](../android/graphics/Path.md)!`, `forceClosed:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Create a PathMeasure object associated with the specified path object (already created and specified). |

| Public methods ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getLength](../android/graphics/PathMeasure.md))`()` Return the total length of the current contour, or 0 if no path is associated with this measure object. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getMatrix](../android/graphics/PathMeasure.md))`(`distance:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `matrix:` ` [Matrix](../android/graphics/Matrix.md)!`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Pins distance to 0 \<= distance \<= getLength(), and then computes the corresponding matrix. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getPosTan](../android/graphics/PathMeasure.md))`(`distance:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `pos:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `tan:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`)` Pins distance to 0 \<= distance \<= getLength(), and then computes the corresponding position and tangent. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getSegment](../android/graphics/PathMeasure.md))`(`startD:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `stopD:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `dst:` ` [Path](../android/graphics/Path.md)!`, `startWithMoveTo:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Given a start and stop distance, return in dst the intervening segment(s). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isClosed](../android/graphics/PathMeasure.md))`()` Return true if the current contour is closed() |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [nextContour](../android/graphics/PathMeasure.md))`()` Move to the next contour in the path. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPath](../android/graphics/PathMeasure.md))`(`path:` ` [Path](../android/graphics/Path.md)!`, `forceClosed:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Assign a new path, or null to have none. |

| Protected methods ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](../android/graphics/PathMeasure.md))`()` <br /> |

## Constants

### POSITION_MATRIX_FLAG

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val POSITION_MATRIX_FLAG: Int
```  

 Value: 1

### TANGENT_MATRIX_FLAG

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TANGENT_MATRIX_FLAG: Int
```  

 Value: 2

## Public constructors

### PathMeasure

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PathMeasure()
```

Create an empty PathMeasure object. To uses this to measure the length of a path, and/or to find the position and tangent along it, call setPath. Note that once a path is associated with the measure object, it is undefined if the path is subsequently modified and the measure object is used. If the path is modified, you must call setPath with the path. 

### PathMeasure

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PathMeasure(
    path: Path!, 
    forceClosed: Boolean)
```

Create a PathMeasure object associated with the specified path object (already created and specified). The measure object can now return the path's length, and the position and tangent of any position along the path. Note that once a path is associated with the measure object, it is undefined if the path is subsequently modified and the measure object is used. If the path is modified, you must call setPath with the path.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `path` | [Path](../android/graphics/Path.md)!:The path that will be measured by this object |
| `forceClosed` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):If true, then the path will be considered as "closed" even if its contour was not explicitly closed. |

## Public methods

### getLength

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLength(): Float
```

Return the total length of the current contour, or 0 if no path is associated with this measure object. 

### getMatrix

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMatrix(
    distance: Float, 
    matrix: Matrix!, 
    flags: Int
): Boolean
```

Pins distance to 0 \<= distance \<= getLength(), and then computes the corresponding matrix. Returns false if there is no path, or a zero-length path was specified, in which case matrix is unchanged.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `distance` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The distance along the associated path |
| `matrix` | [Matrix](../android/graphics/Matrix.md)!:Allocated by the caller, this is set to the transformation associated with the position and tangent at the specified distance |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Specified what aspects should be returned in the matrix. |
| --- | --- |

### getPosTan

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPosTan(
    distance: Float, 
    pos: FloatArray!, 
    tan: FloatArray!
): Boolean
```

Pins distance to 0 \<= distance \<= getLength(), and then computes the corresponding position and tangent. Returns false if there is no path, or a zero-length path was specified, in which case position and tangent are unchanged.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `distance` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The distance along the current contour to sample |
| `pos` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:If not null, returns the sampled position (x==\[0\], y==\[1\]) |
| `tan` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:If not null, returns the sampled tangent (x==\[0\], y==\[1\]) |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | false if there was no path associated with this measure object |

### getSegment

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSegment(
    startD: Float, 
    stopD: Float, 
    dst: Path!, 
    startWithMoveTo: Boolean
): Boolean
```

Given a start and stop distance, return in dst the intervening segment(s). If the segment is zero-length, return false, else return true. startD and stopD are pinned to legal values (0..getLength()). If startD \>= stopD then return false (and leave dst untouched). Begin the segment with a moveTo if startWithMoveTo is true.

On [android.os.Build.VERSION_CODES#KITKAT](../android/os/Build.VERSION_CODES.md) and earlier releases, the resulting path may not display on a hardware-accelerated Canvas. A simple workaround is to add a single operation to this path, such as`dst.rLineTo(0, 0)`. 

### isClosed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isClosed(): Boolean
```

Return true if the current contour is closed() 

### nextContour

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun nextContour(): Boolean
```

Move to the next contour in the path. Return true if one exists, or false if we're done with the path. 

### setPath

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPath(
    path: Path!, 
    forceClosed: Boolean
): Unit
```

Assign a new path, or null to have none.

## Protected methods

### finalize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun finalize(): Unit
```

| Exceptions ||
|-----------------------|-------------------------------------|
| `java.lang.Throwable` | the`Exception`raised by this method |
