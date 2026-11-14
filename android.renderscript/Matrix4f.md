# Matrix4f

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Matrix4f

Kotlin| [Java](../android/renderscript/Matrix4f.md) 
| --- | --- |

```
open class Matrix4f
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.renderscript.Matrix4f](../android/renderscript/Matrix4f.md) |

| **This class was deprecated in API level 31.**
|
| Renderscript has been deprecated in API level 31. Please refer to the [migration guide](https://developer.android.com/guide/topics/renderscript/migration-guide) for the proposed alternatives.

Class for exposing the native RenderScript rs_matrix4x4 type back to the Android system.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Matrix4f](../android/renderscript/Matrix4f.md))`()` Creates a new identity 4x4 matrix |
| [Matrix4f](../android/renderscript/Matrix4f.md))`(`dataArray:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`)` Creates a new matrix and sets its values from the given parameter |

| Public methods ||
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [get](../android/renderscript/Matrix4f.md))`(`x:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `y:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value for a given row and column |
| open [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)! | [getArray](../android/renderscript/Matrix4f.md))`()` Return a reference to the internal array representing matrix values. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [inverse](../android/renderscript/Matrix4f.md))`()` Sets the current matrix to its inverse |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [inverseTranspose](../android/renderscript/Matrix4f.md))`()` Sets the current matrix to its inverse transpose |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [load](../android/renderscript/Matrix4f.md))`(`src:` ` [Matrix4f](../android/renderscript/Matrix4f.md)!`)` Sets the values of the matrix to those of the parameter |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [loadFrustum](../android/renderscript/Matrix4f.md))`(`l:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `r:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `b:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `t:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `n:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `f:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets current values to be a perspective projection matrix |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [loadIdentity](../android/renderscript/Matrix4f.md))`()` Sets the matrix values to identity |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [loadMultiply](../android/renderscript/Matrix4f.md))`(`lhs:` ` [Matrix4f](../android/renderscript/Matrix4f.md)!`, `rhs:` ` [Matrix4f](../android/renderscript/Matrix4f.md)!`)` Sets current values to be the result of multiplying two given matrices |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [loadOrtho](../android/renderscript/Matrix4f.md))`(`l:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `r:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `b:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `t:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `n:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `f:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Set current values to be an orthographic projection matrix |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [loadOrthoWindow](../android/renderscript/Matrix4f.md))`(`w:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `h:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set current values to be an orthographic projection matrix with the right and bottom clipping planes set to the given values. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [loadPerspective](../android/renderscript/Matrix4f.md))`(`fovy:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `aspect:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `near:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `far:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets current values to be a perspective projection matrix |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [loadProjectionNormalized](../android/renderscript/Matrix4f.md))`(`w:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `h:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Helper function to set the current values to a perspective projection matrix with aspect ratio defined by the parameters and (near, far), (bottom, top) mapping to (-1, 1) at z = 0 |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [loadRotate](../android/renderscript/Matrix4f.md))`(`rot:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `z:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets current values to be a rotation matrix of certain angle about a given axis |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [loadScale](../android/renderscript/Matrix4f.md))`(`x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `z:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets current values to be a scale matrix of given dimensions |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [loadTranslate](../android/renderscript/Matrix4f.md))`(`x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `z:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets current values to be a translation matrix of given dimensions |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [multiply](../android/renderscript/Matrix4f.md))`(`rhs:` ` [Matrix4f](../android/renderscript/Matrix4f.md)!`)` Post-multiplies the current matrix by a given parameter |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [rotate](../android/renderscript/Matrix4f.md))`(`rot:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `z:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Modifies the current matrix by post-multiplying it with a rotation matrix of certain angle about a given axis |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [scale](../android/renderscript/Matrix4f.md))`(`x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `z:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Modifies the current matrix by post-multiplying it with a scale matrix of given dimensions |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [set](../android/renderscript/Matrix4f.md))`(`x:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `y:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `v:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets the value for a given row and column |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [translate](../android/renderscript/Matrix4f.md))`(`x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `z:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Modifies the current matrix by post-multiplying it with a translation matrix of given dimensions |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [transpose](../android/renderscript/Matrix4f.md))`()` Sets the current matrix to its transpose |
| --- | --- |

## Public constructors

### Matrix4f

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Matrix4f()
```

Creates a new identity 4x4 matrix 

### Matrix4f

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Matrix4f(dataArray: FloatArray!)
```

Creates a new matrix and sets its values from the given parameter

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `dataArray` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:values to set the matrix to, must be 16 floats long |

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

### inverse

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun inverse(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Sets the current matrix to its inverse 

### inverseTranspose

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun inverseTranspose(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Sets the current matrix to its inverse transpose 

### load

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun load(src: Matrix4f!): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the values of the matrix to those of the parameter

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------|
| `src` | [Matrix4f](../android/renderscript/Matrix4f.md)!:matrix to load the values from |

### loadFrustum

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun loadFrustum(
    l: Float, 
    r: Float, 
    b: Float, 
    t: Float, 
    n: Float, 
    f: Float
): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets current values to be a perspective projection matrix

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------------------------------------------|
| `l` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):location of the left vertical clipping plane |
| `r` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):location of the right vertical clipping plane |
| `b` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):location of the bottom horizontal clipping plane |
| --- | --- |
| `t` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):location of the top horizontal clipping plane |
| `n` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):location of the near clipping plane, must be positive |
| `f` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):location of the far clipping plane, must be positive |
| --- | --- |

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
    lhs: Matrix4f!, 
    rhs: Matrix4f!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets current values to be the result of multiplying two given matrices

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------|
| `lhs` | [Matrix4f](../android/renderscript/Matrix4f.md)!:left hand side matrix |
| `rhs` | [Matrix4f](../android/renderscript/Matrix4f.md)!:right hand side matrix |

### loadOrtho

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun loadOrtho(
    l: Float, 
    r: Float, 
    b: Float, 
    t: Float, 
    n: Float, 
    f: Float
): Unit
```

**Deprecated:** *Deprecated in Java.*

Set current values to be an orthographic projection matrix

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------------------------|
| `l` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):location of the left vertical clipping plane |
| `r` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):location of the right vertical clipping plane |
| `b` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):location of the bottom horizontal clipping plane |
| --- | --- |
| `t` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):location of the top horizontal clipping plane |
| `n` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):location of the near clipping plane |
| `f` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):location of the far clipping plane |
| --- | --- |

### loadOrthoWindow

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun loadOrthoWindow(
    w: Int, 
    h: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

Set current values to be an orthographic projection matrix with the right and bottom clipping planes set to the given values. Left and top clipping planes are set to 0. Near and far are set to -1, 1 respectively

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------------------------------|
| `w` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):location of the right vertical clipping plane |
| `h` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):location of the bottom horizontal clipping plane |

### loadPerspective

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun loadPerspective(
    fovy: Float, 
    aspect: Float, 
    near: Float, 
    far: Float
): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets current values to be a perspective projection matrix

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------|
| `fovy` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):vertical field of view angle in degrees |
| `aspect` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):aspect ratio of the screen |
| `near` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):near cliping plane, must be positive |
| --- | --- |
| `far` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):far clipping plane, must be positive |

### loadProjectionNormalized

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun loadProjectionNormalized(
    w: Int, 
    h: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

Helper function to set the current values to a perspective projection matrix with aspect ratio defined by the parameters and (near, far), (bottom, top) mapping to (-1, 1) at z = 0

| Parameters ||
|-----|------------------------------------------------------------------------------------------|
| `w` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):screen width |
| `h` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):screen height |

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
    y: Float, 
    z: Float
): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets current values to be a translation matrix of given dimensions

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------------|
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):translation component x |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):translation component y |
| `z` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):translation component z |
| --- | --- |

### multiply

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun multiply(rhs: Matrix4f!): Unit
```

**Deprecated:** *Deprecated in Java.*

Post-multiplies the current matrix by a given parameter

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------|
| `rhs` | [Matrix4f](../android/renderscript/Matrix4f.md)!:right hand side to multiply by |

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
    y: Float, 
    z: Float
): Unit
```

**Deprecated:** *Deprecated in Java.*

Modifies the current matrix by post-multiplying it with a translation matrix of given dimensions

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------------|
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):translation component x |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):translation component y |
| `z` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):translation component z |
| --- | --- |

### transpose

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun transpose(): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the current matrix to its transpose
