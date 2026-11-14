# PathMeasure

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PathMeasure

Kotlin| [Java](https://developer.android.com/reference/android/graphics/PathMeasure "View this page in Java") 
| --- | --- |

```
open class PathMeasure
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.PathMeasure](https://developer.android.com/reference/kotlin/android/graphics/PathMeasure#) |

## Summary

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [POSITION_MATRIX_FLAG](https://developer.android.com/reference/kotlin/android/graphics/PathMeasure#POSITION_MATRIX_FLAG:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TANGENT_MATRIX_FLAG](https://developer.android.com/reference/kotlin/android/graphics/PathMeasure#TANGENT_MATRIX_FLAG:kotlin.Int) <br /> |

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PathMeasure](https://developer.android.com/reference/kotlin/android/graphics/PathMeasure#PathMeasure())`()` Create an empty PathMeasure object. |
| [PathMeasure](https://developer.android.com/reference/kotlin/android/graphics/PathMeasure#PathMeasure(android.graphics.Path,%20kotlin.Boolean))`(`path:` ` [Path](https://developer.android.com/reference/kotlin/android/graphics/Path)!`, `forceClosed:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Create a PathMeasure object associated with the specified path object (already created and specified). |

| Public methods ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getLength](https://developer.android.com/reference/kotlin/android/graphics/PathMeasure#getLength())`()` Return the total length of the current contour, or 0 if no path is associated with this measure object. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getMatrix](https://developer.android.com/reference/kotlin/android/graphics/PathMeasure#getMatrix(kotlin.Float,%20android.graphics.Matrix,%20kotlin.Int))`(`distance:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `matrix:` ` [Matrix](https://developer.android.com/reference/kotlin/android/graphics/Matrix)!`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Pins distance to 0 \<= distance \<= getLength(), and then computes the corresponding matrix. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getPosTan](https://developer.android.com/reference/kotlin/android/graphics/PathMeasure#getPosTan(kotlin.Float,%20kotlin.FloatArray,%20kotlin.FloatArray))`(`distance:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `pos:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `tan:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`)` Pins distance to 0 \<= distance \<= getLength(), and then computes the corresponding position and tangent. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getSegment](https://developer.android.com/reference/kotlin/android/graphics/PathMeasure#getSegment(kotlin.Float,%20kotlin.Float,%20android.graphics.Path,%20kotlin.Boolean))`(`startD:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `stopD:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `dst:` ` [Path](https://developer.android.com/reference/kotlin/android/graphics/Path)!`, `startWithMoveTo:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Given a start and stop distance, return in dst the intervening segment(s). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isClosed](https://developer.android.com/reference/kotlin/android/graphics/PathMeasure#isClosed())`()` Return true if the current contour is closed() |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [nextContour](https://developer.android.com/reference/kotlin/android/graphics/PathMeasure#nextContour())`()` Move to the next contour in the path. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPath](https://developer.android.com/reference/kotlin/android/graphics/PathMeasure#setPath(android.graphics.Path,%20kotlin.Boolean))`(`path:` ` [Path](https://developer.android.com/reference/kotlin/android/graphics/Path)!`, `forceClosed:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Assign a new path, or null to have none. |

| Protected methods ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](https://developer.android.com/reference/kotlin/android/graphics/PathMeasure#finalize())`()` <br /> |

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
| `path` | [Path](https://developer.android.com/reference/kotlin/android/graphics/Path)!:The path that will be measured by this object |
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
| `matrix` | [Matrix](https://developer.android.com/reference/kotlin/android/graphics/Matrix)!:Allocated by the caller, this is set to the transformation associated with the position and tangent at the specified distance |
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

On [android.os.Build.VERSION_CODES#KITKAT](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#KITKAT:kotlin.Int) and earlier releases, the resulting path may not display on a hardware-accelerated Canvas. A simple workaround is to add a single operation to this path, such as`dst.rLineTo(0, 0)`. 

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
