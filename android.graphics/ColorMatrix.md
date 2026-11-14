# ColorMatrix

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ColorMatrix

Kotlin| [Java](ColorMatrix.md) 
| --- | --- |

```
open class ColorMatrix
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.ColorMatrix](ColorMatrix.md) |

4x5 matrix for transforming the color and alpha components of a Bitmap. The matrix can be passed as single array, and is treated as follows: 

```kotlin
[ a, b, c, d, e,
     f, g, h, i, j,
     k, l, m, n, o,
     p, q, r, s, t ]
```

<br />

When applied to a color`[R, G, B, A]`, the resulting color is computed as: 

```kotlin
R' = a*R + b*G + c*B + d*A + e;
    G' = f*R + g*G + h*B + i*A + j;
    B' = k*R + l*G + m*B + n*A + o;
    A' = p*R + q*G + r*B + s*A + t;
```

That resulting color`[R', G', B', A']`then has each channel clamped to the`0`to`255`range.

The sample ColorMatrix below inverts incoming colors by scaling each channel by`-1`, and then shifting the result up by`255`to remain in the standard color space. 

```kotlin
[ -1, 0, 0, 0, 255,
      0, -1, 0, 0, 255,
      0, 0, -1, 0, 255,
      0, 0, 0, 1, 0 ]
```

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ColorMatrix](ColorMatrix.md))`()` Create a new colormatrix initialized to identity (as if reset() had been called). |
| [ColorMatrix](ColorMatrix.md))`(`src:` ` [ColorMatrix](ColorMatrix.md)!`)` Create a new colormatrix initialized with the specified colormatrix. |
| [ColorMatrix](ColorMatrix.md))`(`src:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`)` Create a new colormatrix initialized with the specified array of values. |

| Public methods ||
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](ColorMatrix.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)! | [getArray](ColorMatrix.md))`()` Return the array of floats representing this colormatrix. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [postConcat](ColorMatrix.md))`(`postmatrix:` ` [ColorMatrix](ColorMatrix.md)!`)` Concat this colormatrix with the specified postmatrix. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [preConcat](ColorMatrix.md))`(`prematrix:` ` [ColorMatrix](ColorMatrix.md)!`)` Concat this colormatrix with the specified prematrix. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reset](ColorMatrix.md))`()` Set this colormatrix to identity: ```kotlin [ 1 0 0 0 0 - red vector 0 1 0 0 0 - green vector 0 0 1 0 0 - blue vector 0 0 0 1 0 ] - alpha vector ``` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [set](ColorMatrix.md))`(`src:` ` [ColorMatrix](ColorMatrix.md)!`)` Assign the src colormatrix into this matrix, copying all of its values. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [set](ColorMatrix.md))`(`src:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`)` Assign the array of floats into this matrix, copying all of its values. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setConcat](ColorMatrix.md))`(`matA:` ` [ColorMatrix](ColorMatrix.md)!`, `matB:` ` [ColorMatrix](ColorMatrix.md)!`)` Set this colormatrix to the concatenation of the two specified colormatrices, such that the resulting colormatrix has the same effect as applying matB and then applying matA. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRGB2YUV](ColorMatrix.md))`()` Set the matrix to convert RGB to YUV |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRotate](ColorMatrix.md))`(`axis:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `degrees:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Set the rotation on a color axis by the specified values. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSaturation](ColorMatrix.md))`(`sat:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Set the matrix to affect the saturation of colors. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setScale](ColorMatrix.md))`(`rScale:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `gScale:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `bScale:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `aScale:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Set this colormatrix to scale by the specified values. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setYUV2RGB](ColorMatrix.md))`()` Set the matrix to convert from YUV to RGB |

## Public constructors

### ColorMatrix

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ColorMatrix()
```

Create a new colormatrix initialized to identity (as if reset() had been called). 

### ColorMatrix

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ColorMatrix(src: ColorMatrix!)
```

Create a new colormatrix initialized with the specified colormatrix. 

### ColorMatrix

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ColorMatrix(src: FloatArray!)
```

Create a new colormatrix initialized with the specified array of values.

## Public methods

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

### getArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getArray(): FloatArray!
```

Return the array of floats representing this colormatrix. 

### postConcat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun postConcat(postmatrix: ColorMatrix!): Unit
```

Concat this colormatrix with the specified postmatrix.

This is logically the same as calling setConcat(postmatrix, this); 

### preConcat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun preConcat(prematrix: ColorMatrix!): Unit
```

Concat this colormatrix with the specified prematrix.

This is logically the same as calling setConcat(this, prematrix); 

### reset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun reset(): Unit
```

Set this colormatrix to identity: 

```kotlin
[ 1 0 0 0 0   - red vector
    0 1 0 0 0   - green vector
    0 0 1 0 0   - blue vector
    0 0 0 1 0 ] - alpha vector
  
```

<br />

### set

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun set(src: ColorMatrix!): Unit
```

Assign the src colormatrix into this matrix, copying all of its values. 

### set

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun set(src: FloatArray!): Unit
```

Assign the array of floats into this matrix, copying all of its values. 

### setConcat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setConcat(
    matA: ColorMatrix!, 
    matB: ColorMatrix!
): Unit
```

Set this colormatrix to the concatenation of the two specified colormatrices, such that the resulting colormatrix has the same effect as applying matB and then applying matA.

It is legal for either matA or matB to be the same colormatrix as this. 

### setRGB2YUV

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setRGB2YUV(): Unit
```

Set the matrix to convert RGB to YUV 

### setRotate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setRotate(
    axis: Int, 
    degrees: Float
): Unit
```

Set the rotation on a color axis by the specified values.

`axis=0`correspond to a rotation around the RED color`axis=1`correspond to a rotation around the GREEN color`axis=2`correspond to a rotation around the BLUE color 

### setSaturation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSaturation(sat: Float): Unit
```

Set the matrix to affect the saturation of colors.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------------------------------|
| `sat` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):A value of 0 maps the color to gray-scale. 1 is identity. |

### setScale

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setScale(
    rScale: Float, 
    gScale: Float, 
    bScale: Float, 
    aScale: Float
): Unit
```

Set this colormatrix to scale by the specified values. 

### setYUV2RGB

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setYUV2RGB(): Unit
```

Set the matrix to convert from YUV to RGB
