# Matrix3f

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Matrix3f

Kotlin| [Java](Matrix3f.md) 
| --- | --- |

```
open class Matrix3f
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.renderscript.Matrix3f](Matrix3f.md) |

| **This class was deprecated in API level 31.**
|
| Renderscript has been deprecated in API level 31. Please refer to the [migration guide](https://developer.android.com/guide/topics/renderscript/migration-guide) for the proposed alternatives.

Class for exposing the native RenderScript rs_matrix3x3 type back to the Android system.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Matrix3f](Matrix3f.md))`()` Creates a new identity 3x3 matrix |
| [Matrix3f](Matrix3f.md))`(`dataArray:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`)` Creates a new matrix and sets its values from the given parameter |

| Public methods ||
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [get](Matrix3f.md))`(`x:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `y:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value for a given row and column |
| open [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)! | [getArray](Matrix3f.md))`()` Return a reference to the internal array representing matrix values. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [load](Matrix3f.md))`(`src:` ` [Matrix3f](Matrix3f.md)!`)` Sets the values of the matrix to those of the parameter |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [loadIdentity](Matrix3f.md))`()` Sets the matrix values to identity |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [loadMultiply](Matrix3f.md))`(`lhs:` ` [Matrix3f](Matrix3f.md)!`, `rhs:` ` [Matrix3f](Matrix3f.md)!`)` Sets current values to be the result of multiplying two given matrices |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [loadRotate](Matrix3f.md))`(`rot:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Makes the upper 2x2 a rotation matrix of the given angle |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [loadRotate](Matrix3f.md))`(`rot:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `z:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets current values to be a rotation matrix of certain angle about a given axis |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [loadScale](Matrix3f.md))`(`x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Makes the upper 2x2 a scale matrix of given dimensions |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [loadScale](Matrix3f.md))`(`x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `z:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets current values to be a scale matrix of given dimensions |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [loadTranslate](Matrix3f.md))`(`x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets current values to be a translation matrix of given dimensions |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [multiply](Matrix3f.md))`(`rhs:` ` [Matrix3f](Matrix3f.md)!`)` Post-multiplies the current matrix by a given parameter |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [rotate](Matrix3f.md))`(`rot:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Modifies the upper 2x2 of the current matrix by post-multiplying it with a rotation matrix of given angle |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [rotate](Matrix3f.md))`(`rot:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `z:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Modifies the current matrix by post-multiplying it with a rotation matrix of certain angle about a given axis |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [scale](Matrix3f.md))`(`x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Modifies the upper 2x2 of the current matrix by post-multiplying it with a scale matrix of given dimensions |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [scale](Matrix3f.md))`(`x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `z:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Modifies the current matrix by post-multiplying it with a scale matrix of given dimensions |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [set](Matrix3f.md))`(`x:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `y:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `v:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets the value for a given row and column |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [translate](Matrix3f.md))`(`x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Modifies the current matrix by post-multiplying it with a translation matrix of given dimensions |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [transpose](Matrix3f.md))`()` Sets the current matrix to its transpose |
| --- | --- |

## Public constructors

### Matrix3f

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Matrix3f()
```

Creates a new identity 3x3 matrix 

### Matrix3f

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Matrix3f(dataArray: FloatArray!)
```

Creates a new matrix and sets its values from the given parameter

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `dataArray` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:values to set the matrix to, must be 9 floats long |

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
open fun load(src: Matrix3f!): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the values of the matrix to those of the parameter

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------|
| `src` | [Matrix3f](Matrix3f.md)!:matrix to load the values from |

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
    lhs: Matrix3f!, 
    rhs: Matrix3f!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets current values to be the result of multiplying two given matrices

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------|
| `lhs` | [Matrix3f](Matrix3f.md)!:left hand side matrix |
| `rhs` | [Matrix3f](Matrix3f.md)!:right hand side matrix |

### loadRotate

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun loadRotate(rot: Float): Unit
```

**Deprecated:** *Deprecated in Java.*

Makes the upper 2x2 a rotation matrix of the given angle

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------|
| `rot` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):rotation angle |

### loadRotate

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun loadRotate(
    rot: Float, 
    x: Float, 
    y: Float, 
    z: Float
): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets current values to be a rotation matrix of certain angle about a given axis

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------|
| `rot` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):angle of rotation |
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):rotation axis x |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):rotation axis y |
| --- | --- |
| `z` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):rotation axis z |

### loadScale

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun loadScale(
    x: Float, 
    y: Float
): Unit
```

**Deprecated:** *Deprecated in Java.*

Makes the upper 2x2 a scale matrix of given dimensions

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------|
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):scale component x |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):scale component y |

### loadScale

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun loadScale(
    x: Float, 
    y: Float, 
    z: Float
): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets current values to be a scale matrix of given dimensions

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------|
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):scale component x |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):scale component y |
| `z` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):scale component z |
| --- | --- |

### loadTranslate

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun loadTranslate(
    x: Float, 
    y: Float
): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets current values to be a translation matrix of given dimensions

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------------|
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):translation component x |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):translation component y |

### multiply

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun multiply(rhs: Matrix3f!): Unit
```

**Deprecated:** *Deprecated in Java.*

Post-multiplies the current matrix by a given parameter

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------|
| `rhs` | [Matrix3f](Matrix3f.md)!:right hand side to multiply by |

### rotate

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun rotate(rot: Float): Unit
```

**Deprecated:** *Deprecated in Java.*

Modifies the upper 2x2 of the current matrix by post-multiplying it with a rotation matrix of given angle

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------|
| `rot` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):angle of rotation |

### rotate

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun rotate(
    rot: Float, 
    x: Float, 
    y: Float, 
    z: Float
): Unit
```

**Deprecated:** *Deprecated in Java.*

Modifies the current matrix by post-multiplying it with a rotation matrix of certain angle about a given axis

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------|
| `rot` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):angle of rotation |
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):rotation axis x |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):rotation axis y |
| --- | --- |
| `z` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):rotation axis z |

### scale

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun scale(
    x: Float, 
    y: Float
): Unit
```

**Deprecated:** *Deprecated in Java.*

Modifies the upper 2x2 of the current matrix by post-multiplying it with a scale matrix of given dimensions

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------|
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):scale component x |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):scale component y |

### scale

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun scale(
    x: Float, 
    y: Float, 
    z: Float
): Unit
```

**Deprecated:** *Deprecated in Java.*

Modifies the current matrix by post-multiplying it with a scale matrix of given dimensions

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------|
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):scale component x |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):scale component y |
| `z` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):scale component z |
| --- | --- |

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

### translate

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun translate(
    x: Float, 
    y: Float
): Unit
```

**Deprecated:** *Deprecated in Java.*

Modifies the current matrix by post-multiplying it with a translation matrix of given dimensions

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------------|
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):translation component x |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):translation component y |

### transpose

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun transpose(): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the current matrix to its transpose
