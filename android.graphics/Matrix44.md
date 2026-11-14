# Matrix44

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Matrix44

Kotlin| [Java](../android/graphics/Matrix44.md) 
| --- | --- |

```
open class Matrix44
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.Matrix44](../android/graphics/Matrix44.md) |

The Matrix44 class holds a 4x4 matrix for transforming coordinates. It is similar to [Matrix](../android/graphics/Matrix.md), and should be used when you want to manipulate the canvas in 3D. Values are kept in row-major order. The values and operations are treated as column vectors.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Matrix44](../android/graphics/Matrix44.md))`()` The default Matrix44 constructor will instantiate an identity matrix. |
| [Matrix44](../android/graphics/Matrix44.md))`(`mat:` ` [Matrix](../android/graphics/Matrix.md)`)` Creates and returns a Matrix44 by taking the 3x3 Matrix and placing it on the 0 of the z-axis by setting row`2`and column`2`to the identity as seen in the following operation: ```kotlin [ a b c ] [ a b 0 c ] [ d e f ] -> [ d e 0 f ] [ g h i ] [ 0 0 1 0 ] [ g h 0 i ] ``` <br /> |

| Public methods ||
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Matrix44](../android/graphics/Matrix44.md) | [concat](../android/graphics/Matrix44.md))`(`b:` ` [Matrix44](../android/graphics/Matrix44.md)`)` Multiplies \`this\` matrix (A) and provided Matrix (B) in the order of A \* B. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/graphics/Matrix44.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [get](../android/graphics/Matrix44.md))`(`row:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `col:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Gets the value at the matrix's row and column. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getValues](../android/graphics/Matrix44.md))`(`dst:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)`)` Copies matrix values into the provided array in row-major order. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/graphics/Matrix44.md))`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [invert](../android/graphics/Matrix44.md))`()` Inverts the Matrix44, then return true if successful, false if unable to invert. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isIdentity](../android/graphics/Matrix44.md))`()` Returns true if Matrix44 is equal to identity matrix. |
| open [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html) | [map](../android/graphics/Matrix44.md))`(`x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `z:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `w:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Multiplies (x, y, z, w) vector by the Matrix44, then returns the new (x, y, z, w). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [map](../android/graphics/Matrix44.md))`(`x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `z:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `w:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `dst:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)`)` Multiplies (x, y, z, w) vector by the Matrix44, then returns the new (x, y, z, w). |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reset](../android/graphics/Matrix44.md))`()` Sets the Matrix44 to the identity matrix. |
| open [Matrix44](../android/graphics/Matrix44.md) | [rotate](../android/graphics/Matrix44.md))`(`deg:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `xComp:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `yComp:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `zComp:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Applies a rotation around a given axis, then returns self. |
| open [Matrix44](../android/graphics/Matrix44.md) | [scale](../android/graphics/Matrix44.md))`(`x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `z:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Applies scaling factors to \`this\` Matrix44, then returns self. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [set](../android/graphics/Matrix44.md))`(`row:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `col:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `val:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets the value at the matrix's row and column to the provided value. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setValues](../android/graphics/Matrix44.md))`(`src:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)`)` Replaces the Matrix's values with the values in the provided array. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/graphics/Matrix44.md))`()` <br /> |
| --- | --- |
| open [Matrix44](../android/graphics/Matrix44.md) | [translate](../android/graphics/Matrix44.md))`(`x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `z:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Applies a translation to \`this\` Matrix44, then returns self. |

## Public constructors

### Matrix44

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Matrix44()
```

The default Matrix44 constructor will instantiate an identity matrix. 

### Matrix44

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Matrix44(mat: Matrix)
```

Creates and returns a Matrix44 by taking the 3x3 Matrix and placing it on the 0 of the z-axis by setting row`2`and column`2`to the identity as seen in the following operation: 

```kotlin
[ a b c ]      [ a b 0 c ]
  [ d e f ]  ->  [ d e 0 f ]
  [ g h i ]      [ 0 0 1 0 ]
                 [ g h 0 i ]
  
```

<br />

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mat` | [Matrix](../android/graphics/Matrix.md):A 3x3 Matrix to be converted (original Matrix will not be changed) This value cannot be`null`. |

## Public methods

### concat

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun concat(b: Matrix44): Matrix44
```

Multiplies \`this\` matrix (A) and provided Matrix (B) in the order of A \* B. The result is saved in \`this\` Matrix.

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `b` | [Matrix44](../android/graphics/Matrix44.md):The second Matrix in the concatenation operation This value cannot be`null`. |

| Return ||
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [Matrix44](../android/graphics/Matrix44.md) | A reference to this Matrix, which can be used to chain Matrix operations This value cannot be`null`. |

### equals

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### get

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun get(
    row: Int, 
    col: Int
): Float
```

Gets the value at the matrix's row and column.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `row` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):An integer from 0 to 3 indicating the row of the value to get Value is between 0 and 3 inclusive |
| `col` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):An integer from 0 to 3 indicating the column of the value to get Value is between 0 and 3 inclusive |

### getValues

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getValues(dst: FloatArray): Unit
```

Copies matrix values into the provided array in row-major order.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dst` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html):The float array where values will be copied, must be of length 16 This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|----------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the destination float array is not of length 16 |

### hashCode

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### invert

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun invert(): Boolean
```

Inverts the Matrix44, then return true if successful, false if unable to invert.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`on success,`false`otherwise |

### isIdentity

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isIdentity(): Boolean
```

Returns true if Matrix44 is equal to identity matrix. 

### map

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun map(
    x: Float, 
    y: Float, 
    z: Float, 
    w: Float
): FloatArray
```

Multiplies (x, y, z, w) vector by the Matrix44, then returns the new (x, y, z, w). Users should set`w`to 1 to indicate the coordinates are normalized.

| Return ||
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html) | An array of length 4 that represents the x, y, z, w (where w is perspective) value after multiplying x, y, z, 1 by the matrix This value cannot be`null`. |

### map

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun map(
    x: Float, 
    y: Float, 
    z: Float, 
    w: Float, 
    dst: FloatArray
): Unit
```

Multiplies (x, y, z, w) vector by the Matrix44, then returns the new (x, y, z, w). Users should set`w`to 1 to indicate the coordinates are normalized.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------|
| `dst` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html):This value cannot be`null`. |

### reset

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun reset(): Unit
```

Sets the Matrix44 to the identity matrix. 

### rotate

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun rotate(
    deg: Float, 
    xComp: Float, 
    yComp: Float, 
    zComp: Float
): Matrix44
```

Applies a rotation around a given axis, then returns self.`x`,`y`,`z`represent the axis by which to rotate around. For example, pass in`1, 0, 0`to rotate around the x-axis. The axis provided will be normalized.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------|
| `deg` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Amount in degrees to rotate the matrix about the x-axis |
| `xComp` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):X component of the rotation axis |
| `yComp` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Y component of the rotation axis |
| --- | --- |
| `zComp` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Z component of the rotation axis |

| Return ||
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [Matrix44](../android/graphics/Matrix44.md) | A reference to this Matrix, which can be used to chain Matrix operations This value cannot be`null`. |

### scale

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun scale(
    x: Float, 
    y: Float, 
    z: Float
): Matrix44
```

Applies scaling factors to \`this\` Matrix44, then returns self. Pass 1s for no change.

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------------------|
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Scaling factor for the x-axis |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Scaling factor for the y-axis |
| `z` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Scaling factor for the z-axis |
| --- | --- |

| Return ||
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [Matrix44](../android/graphics/Matrix44.md) | A reference to this Matrix, which can be used to chain Matrix operations This value cannot be`null`. |

### set

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun set(
    row: Int, 
    col: Int, 
    val: Float
): Unit
```

Sets the value at the matrix's row and column to the provided value.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `row` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):An integer from 0 to 3 indicating the row of the value to change Value is between 0 and 3 inclusive |
| `col` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):An integer from 0 to 3 indicating the column of the value to change Value is between 0 and 3 inclusive |
| `val` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The value the element at the specified index will be set to |
| --- | --- |

### setValues

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setValues(src: FloatArray): Unit
```

Replaces the Matrix's values with the values in the provided array.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `src` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html):A float array of length 16. Floats are treated in row-major order This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|----------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the destination float array is not of length 16 |

### toString

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### translate

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun translate(
    x: Float, 
    y: Float, 
    z: Float
): Matrix44
```

Applies a translation to \`this\` Matrix44, then returns self.

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------------|
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Translation for the x-axis |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Translation for the y-axis |
| `z` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Translation for the z-axis |
| --- | --- |

| Return ||
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [Matrix44](../android/graphics/Matrix44.md) | A reference to this Matrix, which can be used to chain Matrix operations This value cannot be`null`. |
