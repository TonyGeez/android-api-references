# Matrix2f

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Matrix2f

Kotlin| [Java](https://developer.android.com/reference/android/renderscript/Matrix2f "View this page in Java") 
| --- | --- |

```
open class Matrix2f
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.renderscript.Matrix2f](https://developer.android.com/reference/kotlin/android/renderscript/Matrix2f#) |

| **This class was deprecated in API level 31.**
|
| Renderscript has been deprecated in API level 31. Please refer to the [migration guide](https://developer.android.com/guide/topics/renderscript/migration-guide) for the proposed alternatives.

Class for exposing the native RenderScript rs_matrix2x2 type back to the Android system.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Matrix2f](https://developer.android.com/reference/kotlin/android/renderscript/Matrix2f#Matrix2f())`()` Creates a new identity 2x2 matrix |
| [Matrix2f](https://developer.android.com/reference/kotlin/android/renderscript/Matrix2f#Matrix2f(kotlin.FloatArray))`(`dataArray:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`)` Creates a new matrix and sets its values from the given parameter |

| Public methods ||
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [get](https://developer.android.com/reference/kotlin/android/renderscript/Matrix2f#get(kotlin.Int,%20kotlin.Int))`(`x:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `y:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value for a given row and column |
| open [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)! | [getArray](https://developer.android.com/reference/kotlin/android/renderscript/Matrix2f#getArray())`()` Return a reference to the internal array representing matrix values. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [load](https://developer.android.com/reference/kotlin/android/renderscript/Matrix2f#load(android.renderscript.Matrix2f))`(`src:` ` [Matrix2f](https://developer.android.com/reference/kotlin/android/renderscript/Matrix2f#)!`)` Sets the values of the matrix to those of the parameter |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [loadIdentity](https://developer.android.com/reference/kotlin/android/renderscript/Matrix2f#loadIdentity())`()` Sets the matrix values to identity |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [loadMultiply](https://developer.android.com/reference/kotlin/android/renderscript/Matrix2f#loadMultiply(android.renderscript.Matrix2f,%20android.renderscript.Matrix2f))`(`lhs:` ` [Matrix2f](https://developer.android.com/reference/kotlin/android/renderscript/Matrix2f#)!`, `rhs:` ` [Matrix2f](https://developer.android.com/reference/kotlin/android/renderscript/Matrix2f#)!`)` Sets current values to be the result of multiplying two given matrices |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [loadRotate](https://developer.android.com/reference/kotlin/android/renderscript/Matrix2f#loadRotate(kotlin.Float))`(`rot:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets current values to be a rotation matrix of given angle |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [loadScale](https://developer.android.com/reference/kotlin/android/renderscript/Matrix2f#loadScale(kotlin.Float,%20kotlin.Float))`(`x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets current values to be a scale matrix of given dimensions |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [multiply](https://developer.android.com/reference/kotlin/android/renderscript/Matrix2f#multiply(android.renderscript.Matrix2f))`(`rhs:` ` [Matrix2f](https://developer.android.com/reference/kotlin/android/renderscript/Matrix2f#)!`)` Post-multiplies the current matrix by a given parameter |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [rotate](https://developer.android.com/reference/kotlin/android/renderscript/Matrix2f#rotate(kotlin.Float))`(`rot:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Modifies the current matrix by post-multiplying it with a rotation matrix of given angle |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [scale](https://developer.android.com/reference/kotlin/android/renderscript/Matrix2f#scale(kotlin.Float,%20kotlin.Float))`(`x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Modifies the current matrix by post-multiplying it with a scale matrix of given dimensions |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [set](https://developer.android.com/reference/kotlin/android/renderscript/Matrix2f#set(kotlin.Int,%20kotlin.Int,%20kotlin.Float))`(`x:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `y:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `v:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets the value for a given row and column |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [transpose](https://developer.android.com/reference/kotlin/android/renderscript/Matrix2f#transpose())`()` Sets the current matrix to its transpose |
| --- | --- |

## Public constructors

### Matrix2f

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Matrix2f()
```

Creates a new identity 2x2 matrix 

### Matrix2f

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Matrix2f(dataArray: FloatArray!)
```

Creates a new matrix and sets its values from the given parameter

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `dataArray` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:values to set the matrix to, must be 4 floats long |

## Public methods

### get

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun get(
    x: Int, 
    y: Int
): Float
```

**Deprecated:** *Deprecated in Java.*

Returns the value for a given row and column

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------|
| `x` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):column of the value to return |
| `y` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):row of the value to return |

| Return ||
|--------------------------------------------------------------------------------|-------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | value in the yth row and xth column |

### getArray

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getArray(): FloatArray!
```

**Deprecated:** *Deprecated in Java.*

Return a reference to the internal array representing matrix values. Modifying this array will also change the matrix

| Return ||
|--------------------------------------------------------------------------------------------|----------------------------------------|
| [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)! | internal array representing the matrix |

### load

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun load(src: Matrix2f!): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the values of the matrix to those of the parameter

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------|
| `src` | [Matrix2f](https://developer.android.com/reference/kotlin/android/renderscript/Matrix2f#)!:matrix to load the values from |

### loadIdentity

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun loadIdentity(): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the matrix values to identity 

### loadMultiply

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun loadMultiply(
    lhs: Matrix2f!, 
    rhs: Matrix2f!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets current values to be the result of multiplying two given matrices

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------|
| `lhs` | [Matrix2f](https://developer.android.com/reference/kotlin/android/renderscript/Matrix2f#)!:left hand side matrix |
| `rhs` | [Matrix2f](https://developer.android.com/reference/kotlin/android/renderscript/Matrix2f#)!:right hand side matrix |

### loadRotate

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun loadRotate(rot: Float): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets current values to be a rotation matrix of given angle

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------|
| `rot` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):rotation angle |

### loadScale

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun loadScale(
    x: Float, 
    y: Float
): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets current values to be a scale matrix of given dimensions

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------|
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):scale component x |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):scale component y |

### multiply

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun multiply(rhs: Matrix2f!): Unit
```

**Deprecated:** *Deprecated in Java.*

Post-multiplies the current matrix by a given parameter

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------|
| `rhs` | [Matrix2f](https://developer.android.com/reference/kotlin/android/renderscript/Matrix2f#)!:right hand side to multiply by |

### rotate

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun rotate(rot: Float): Unit
```

**Deprecated:** *Deprecated in Java.*

Modifies the current matrix by post-multiplying it with a rotation matrix of given angle

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------|
| `rot` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):angle of rotation |

### scale

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun scale(
    x: Float, 
    y: Float
): Unit
```

**Deprecated:** *Deprecated in Java.*

Modifies the current matrix by post-multiplying it with a scale matrix of given dimensions

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------|
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):scale component x |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):scale component y |

### set

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun set(
    x: Int, 
    y: Int, 
    v: Float
): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the value for a given row and column

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------|
| `x` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):column of the value to set |
| `y` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):row of the value to set |

### transpose

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun transpose(): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the current matrix to its transpose
