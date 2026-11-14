# Matrix

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Matrix

Kotlin| [Java](Matrix.md) 
| --- | --- |

```
open class Matrix
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.opengl.Matrix](Matrix.md) |

Matrix math utilities. These methods operate on OpenGL ES format matrices and vectors stored in float arrays.

Matrices are 4 x 4 column-vector matrices stored in column-major order: 

```kotlin
m[offset +  0] m[offset +  4] m[offset +  8] m[offset + 12]
   m[offset +  1] m[offset +  5] m[offset +  9] m[offset + 13]
   m[offset +  2] m[offset +  6] m[offset + 10] m[offset + 14]
   m[offset +  3] m[offset +  7] m[offset + 11] m[offset + 15]
```
Vectors are 4 x 1 column vectors stored in order: 

```kotlin
v[offset + 0]
  v[offset + 1]
  v[offset + 2]
  v[offset + 3]
```

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------|---|
| [Matrix](Matrix.md))`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [frustumM](Matrix.md))`(`m:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `left:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `right:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `bottom:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `top:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `near:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `far:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Defines a projection matrix in terms of six clip planes. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [invertM](Matrix.md))`(`mInv:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `mInvOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `m:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `mOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Inverts a 4 x 4 matrix. |
| openstatic [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [length](Matrix.md))`(`x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `z:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Computes the length of a vector. |
| --- | --- |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [multiplyMM](Matrix.md))`(`result:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `resultOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `lhs:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `lhsOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `rhs:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `rhsOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Multiplies two 4x4 matrices together and stores the result in a third 4x4 matrix. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [multiplyMV](Matrix.md))`(`resultVec:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `resultVecOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `lhsMat:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `lhsMatOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `rhsVec:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `rhsVecOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Multiplies a 4 element vector by a 4x4 matrix and stores the result in a 4-element column vector. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [orthoM](Matrix.md))`(`m:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `mOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `left:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `right:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `bottom:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `top:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `near:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `far:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Computes an orthographic projection matrix. |
| --- | --- |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [perspectiveM](Matrix.md))`(`m:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `fovy:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `aspect:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `zNear:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `zFar:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Defines a projection matrix in terms of a field of view angle, an aspect ratio, and z clip planes. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [rotateM](Matrix.md))`(`m:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `mOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `a:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `z:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Rotates matrix m in place by angle a (in degrees) around the axis (x, y, z). |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [rotateM](Matrix.md))`(`rm:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `rmOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `m:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `mOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `a:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `z:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Rotates matrix m by angle a (in degrees) around the axis (x, y, z). |
| --- | --- |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [scaleM](Matrix.md))`(`m:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `mOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `z:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Scales matrix m in place by sx, sy, and sz. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [scaleM](Matrix.md))`(`sm:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `smOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `m:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `mOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `z:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Scales matrix m by x, y, and z, putting the result in sm. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setIdentityM](Matrix.md))`(`sm:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `smOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets matrix m to the identity matrix. |
| --- | --- |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLookAtM](Matrix.md))`(`rm:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `rmOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `eyeX:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `eyeY:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `eyeZ:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `centerX:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `centerY:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `centerZ:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `upX:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `upY:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `upZ:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Defines a viewing transformation in terms of an eye point, a center of view, and an up vector. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRotateEulerM](Matrix.md))`(`rm:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `rmOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `z:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Converts Euler angles to a rotation matrix. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRotateEulerM2](Matrix.md))`(`rm:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)`, `rmOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `z:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Converts Euler angles to a rotation matrix. |
| --- | --- |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRotateM](Matrix.md))`(`rm:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `rmOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `a:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `z:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Creates a matrix for rotation by angle a (in degrees) around the axis (x, y, z). |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [translateM](Matrix.md))`(`m:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `mOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `z:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Translates matrix m by x, y, and z in place. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [translateM](Matrix.md))`(`tm:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `tmOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `m:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `mOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `z:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Translates matrix m by x, y, and z, putting the result in tm. |
| --- | --- |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [transposeM](Matrix.md))`(`mTrans:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `mTransOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `m:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `mOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Transposes a 4 x 4 matrix. |

## Public constructors

### Matrix

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Matrix()
```

**Deprecated:** *All methods are static, do not instantiate this class.*

## Public methods

### frustumM

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun frustumM(
    m: FloatArray!, 
    offset: Int, 
    left: Float, 
    right: Float, 
    bottom: Float, 
    top: Float, 
    near: Float, 
    far: Float
): Unit
```

Defines a projection matrix in terms of six clip planes.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| `m` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:the float array that holds the output perspective matrix |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the offset into float array m where the perspective matrix data is written |
| `left` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): |
| --- | --- |
| `right` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): |
| `bottom` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): |
| `top` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): |
| --- | --- |
| `near` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): |
| `far` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): |

### invertM

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun invertM(
    mInv: FloatArray!, 
    mInvOffset: Int, 
    m: FloatArray!, 
    mOffset: Int
): Boolean
```

Inverts a 4 x 4 matrix.

mInv and m must not overlap.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `mInv` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:the array that holds the output inverted matrix |
| `mInvOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):an offset into mInv where the inverted matrix is stored. |
| `m` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:the input array |
| --- | --- |
| `mOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):an offset into m where the input matrix is stored. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the matrix could be inverted, false if it could not. |

### length

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun length(
    x: Float, 
    y: Float, 
    z: Float
): Float
```

Computes the length of a vector.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------|
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):x coordinate of a vector |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):y coordinate of a vector |
| `z` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):z coordinate of a vector |
| --- | --- |

| Return ||
|--------------------------------------------------------------------------------|------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | the length of a vector |

### multiplyMM

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun multiplyMM(
    result: FloatArray!, 
    resultOffset: Int, 
    lhs: FloatArray!, 
    lhsOffset: Int, 
    rhs: FloatArray!, 
    rhsOffset: Int
): Unit
```

Multiplies two 4x4 matrices together and stores the result in a third 4x4 matrix. In matrix notation: result = lhs x rhs. Due to the way matrix multiplication works, the result matrix will have the same effect as first multiplying by the rhs matrix, then multiplying by the lhs matrix. This is the opposite of what you might expect.

The same float array may be passed for result, lhs, and/or rhs. This operation is expected to do the correct thing if the result elements overlap with either of the lhs or rhs elements.

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `result` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:The float array that holds the result. |
| `resultOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The offset into the result array where the result is stored. |
| `lhs` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:The float array that holds the left-hand-side matrix. |
| --- | --- |
| `lhsOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The offset into the lhs array where the lhs is stored |
| `rhs` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:The float array that holds the right-hand-side matrix. |
| `rhsOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The offset into the rhs array where the rhs is stored. |
| --- | --- |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | under any of the following conditions: result, lhs, or rhs are null; resultOffset + 16 \> result.length or lhsOffset + 16 \> lhs.length or rhsOffset + 16 \> rhs.length; resultOffset \< 0 or lhsOffset \< 0 or rhsOffset \< 0 |

### multiplyMV

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun multiplyMV(
    resultVec: FloatArray!, 
    resultVecOffset: Int, 
    lhsMat: FloatArray!, 
    lhsMatOffset: Int, 
    rhsVec: FloatArray!, 
    rhsVecOffset: Int
): Unit
```

Multiplies a 4 element vector by a 4x4 matrix and stores the result in a 4-element column vector. In matrix notation: result = lhs x rhs

The same float array may be passed for resultVec, lhsMat, and/or rhsVec. This operation is expected to do the correct thing if the result elements overlap with either of the lhs or rhs elements.

| Parameters ||
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `resultVec` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:The float array that holds the result vector. |
| `resultVecOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The offset into the result array where the result vector is stored. |
| `lhsMat` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:The float array that holds the left-hand-side matrix. |
| --- | --- |
| `lhsMatOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The offset into the lhs array where the lhs is stored |
| `rhsVec` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:The float array that holds the right-hand-side vector. |
| `rhsVecOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The offset into the rhs vector where the rhs vector is stored. |
| --- | --- |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | under any of the following conditions: resultVec, lhsMat, or rhsVec are null; resultVecOffset + 4 \> resultVec.length or lhsMatOffset + 16 \> lhsMat.length or rhsVecOffset + 4 \> rhsVec.length; resultVecOffset \< 0 or lhsMatOffset \< 0 or rhsVecOffset \< 0 |

### orthoM

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun orthoM(
    m: FloatArray!, 
    mOffset: Int, 
    left: Float, 
    right: Float, 
    bottom: Float, 
    top: Float, 
    near: Float, 
    far: Float
): Unit
```

Computes an orthographic projection matrix.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------|
| `m` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:returns the result |
| `mOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): |
| `left` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): |
| --- | --- |
| `right` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): |
| `bottom` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): |
| `top` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): |
| --- | --- |
| `near` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): |
| `far` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): |

### perspectiveM

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun perspectiveM(
    m: FloatArray!, 
    offset: Int, 
    fovy: Float, 
    aspect: Float, 
    zNear: Float, 
    zFar: Float
): Unit
```

Defines a projection matrix in terms of a field of view angle, an aspect ratio, and z clip planes.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| `m` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:the float array that holds the perspective matrix |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the offset into float array m where the perspective matrix data is written |
| `fovy` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):field of view in y direction, in degrees |
| --- | --- |
| `aspect` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):width to height aspect ratio of the viewport |
| `zNear` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): |
| `zFar` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): |
| --- | --- |

### rotateM

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun rotateM(
    m: FloatArray!, 
    mOffset: Int, 
    a: Float, 
    x: Float, 
    y: Float, 
    z: Float
): Unit
```

Rotates matrix m in place by angle a (in degrees) around the axis (x, y, z).

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------|
| `m` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:source matrix |
| `mOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index into m where the matrix starts |
| `a` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):angle to rotate in degrees |
| --- | --- |
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):X axis component |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Y axis component |
| `z` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Z axis component |
| --- | --- |

### rotateM

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun rotateM(
    rm: FloatArray!, 
    rmOffset: Int, 
    m: FloatArray!, 
    mOffset: Int, 
    a: Float, 
    x: Float, 
    y: Float, 
    z: Float
): Unit
```

Rotates matrix m by angle a (in degrees) around the axis (x, y, z).

m and rm must not overlap.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------|
| `rm` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:returns the result |
| `rmOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index into rm where the result matrix starts |
| `m` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:source matrix |
| --- | --- |
| `mOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index into m where the source matrix starts |
| `a` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):angle to rotate in degrees |
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):X axis component |
| --- | --- |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Y axis component |
| `z` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Z axis component |

### scaleM

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun scaleM(
    m: FloatArray!, 
    mOffset: Int, 
    x: Float, 
    y: Float, 
    z: Float
): Unit
```

Scales matrix m in place by sx, sy, and sz.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------|
| `m` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:matrix to scale |
| `mOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index into m where the matrix starts |
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):scale factor x |
| --- | --- |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):scale factor y |
| `z` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):scale factor z |

### scaleM

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun scaleM(
    sm: FloatArray!, 
    smOffset: Int, 
    m: FloatArray!, 
    mOffset: Int, 
    x: Float, 
    y: Float, 
    z: Float
): Unit
```

Scales matrix m by x, y, and z, putting the result in sm.

m and sm must not overlap.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------|
| `sm` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:returns the result |
| `smOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index into sm where the result matrix starts |
| `m` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:source matrix |
| --- | --- |
| `mOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index into m where the source matrix starts |
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):scale factor x |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):scale factor y |
| --- | --- |
| `z` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):scale factor z |

### setIdentityM

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun setIdentityM(
    sm: FloatArray!, 
    smOffset: Int
): Unit
```

Sets matrix m to the identity matrix.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------|
| `sm` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:returns the result |
| `smOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index into sm where the result matrix starts |

### setLookAtM

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun setLookAtM(
    rm: FloatArray!, 
    rmOffset: Int, 
    eyeX: Float, 
    eyeY: Float, 
    eyeZ: Float, 
    centerX: Float, 
    centerY: Float, 
    centerZ: Float, 
    upX: Float, 
    upY: Float, 
    upZ: Float
): Unit
```

Defines a viewing transformation in terms of an eye point, a center of view, and an up vector.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------|
| `rm` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:returns the result |
| `rmOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index into rm where the result matrix starts |
| `eyeX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):eye point X |
| --- | --- |
| `eyeY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):eye point Y |
| `eyeZ` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):eye point Z |
| `centerX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):center of view X |
| --- | --- |
| `centerY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):center of view Y |
| `centerZ` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):center of view Z |
| `upX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):up vector X |
| --- | --- |
| `upY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):up vector Y |
| `upZ` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):up vector Z |

### setRotateEulerM

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun setRotateEulerM(
    rm: FloatArray!, 
    rmOffset: Int, 
    x: Float, 
    y: Float, 
    z: Float
): Unit
```

**Deprecated:** *This method is incorrect around the y axis. This method is deprecated and replaced (below) by setRotateEulerM2 which behaves correctly*

Converts Euler angles to a rotation matrix.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------|
| `rm` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:returns the result |
| `rmOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index into rm where the result matrix starts |
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):angle of rotation, in degrees |
| --- | --- |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):is broken, do not use |
| `z` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):angle of rotation, in degrees |

### setRotateEulerM2

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun setRotateEulerM2(
    rm: FloatArray, 
    rmOffset: Int, 
    x: Float, 
    y: Float, 
    z: Float
): Unit
```

Converts Euler angles to a rotation matrix.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------|
| `rm` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html):returns the result |
| `rmOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index into rm where the result matrix starts |
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):angle of rotation, in degrees |
| --- | --- |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):angle of rotation, in degrees |
| `z` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):angle of rotation, in degrees |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if rm is null; or if rmOffset + 16 \> rm.length; rmOffset \< 0 |

### setRotateM

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun setRotateM(
    rm: FloatArray!, 
    rmOffset: Int, 
    a: Float, 
    x: Float, 
    y: Float, 
    z: Float
): Unit
```

Creates a matrix for rotation by angle a (in degrees) around the axis (x, y, z).

An optimized path will be used for rotation about a major axis (e.g. x=1.0f y=0.0f z=0.0f).

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------|
| `rm` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:returns the result |
| `rmOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index into rm where the result matrix starts |
| `a` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):angle to rotate in degrees |
| --- | --- |
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):X axis component |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Y axis component |
| `z` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Z axis component |
| --- | --- |

### translateM

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun translateM(
    m: FloatArray!, 
    mOffset: Int, 
    x: Float, 
    y: Float, 
    z: Float
): Unit
```

Translates matrix m by x, y, and z in place.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------|
| `m` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:matrix |
| `mOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index into m where the matrix starts |
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):translation factor x |
| --- | --- |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):translation factor y |
| `z` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):translation factor z |

### translateM

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun translateM(
    tm: FloatArray!, 
    tmOffset: Int, 
    m: FloatArray!, 
    mOffset: Int, 
    x: Float, 
    y: Float, 
    z: Float
): Unit
```

Translates matrix m by x, y, and z, putting the result in tm.

m and tm must not overlap.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------|
| `tm` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:returns the result |
| `tmOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index into sm where the result matrix starts |
| `m` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:source matrix |
| --- | --- |
| `mOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index into m where the source matrix starts |
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):translation factor x |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):translation factor y |
| --- | --- |
| `z` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):translation factor z |

### transposeM

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun transposeM(
    mTrans: FloatArray!, 
    mTransOffset: Int, 
    m: FloatArray!, 
    mOffset: Int
): Unit
```

Transposes a 4 x 4 matrix.

mTrans and m must not overlap.

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `mTrans` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:the array that holds the output transposed matrix |
| `mTransOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):an offset into mTrans where the transposed matrix is stored. |
| `m` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:the input array |
| --- | --- |
| `mOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):an offset into m where the input matrix is stored. |
