# Matrix

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Matrix

Kotlin| [Java](../android/graphics/Matrix.md) 
| --- | --- |

```
open class Matrix
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.Matrix](../android/graphics/Matrix.md) |

The Matrix class holds a 3x3 matrix for transforming coordinates.

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [ScaleToFit](../android/graphics/Matrix.ScaleToFit.md) Controls how the src rect should align into the dst rect for setRectToRect(). |

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MPERSP_0](../android/graphics/Matrix.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MPERSP_1](../android/graphics/Matrix.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MPERSP_2](../android/graphics/Matrix.md) <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MSCALE_X](../android/graphics/Matrix.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MSCALE_Y](../android/graphics/Matrix.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MSKEW_X](../android/graphics/Matrix.md) <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MSKEW_Y](../android/graphics/Matrix.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MTRANS_X](../android/graphics/Matrix.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MTRANS_Y](../android/graphics/Matrix.md) <br /> |
| --- | --- |

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Matrix](../android/graphics/Matrix.md))`()` Create an identity matrix |
| [Matrix](../android/graphics/Matrix.md))`(`src:` ` [Matrix](../android/graphics/Matrix.md)!`)` Create a matrix that is a (deep) copy of src |

| Public methods ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dump](../android/graphics/Matrix.md))`(`pw:` ` [PrintWriter](../java/io/PrintWriter.md)`)` Dumps a human-readable shortened string of the matrix into the given stream |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/graphics/Matrix.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Returns true iff obj is a Matrix and its values equal our values. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getValues](../android/graphics/Matrix.md))`(`values:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`)` Copy 9 values from the matrix into the array. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/graphics/Matrix.md))`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [invert](../android/graphics/Matrix.md))`(`inverse:` ` [Matrix](../android/graphics/Matrix.md)!`)` If this matrix can be inverted, return true and if inverse is not null, set inverse to be the inverse of this matrix. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAffine](../android/graphics/Matrix.md))`()` Gets whether this matrix is affine. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isIdentity](../android/graphics/Matrix.md))`()` Returns true if the matrix is identity. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [mapPoints](../android/graphics/Matrix.md))`(`pts:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`)` Apply this matrix to the array of 2D points, and write the transformed points back into the array |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [mapPoints](../android/graphics/Matrix.md))`(`dst:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `src:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`)` Apply this matrix to the array of 2D points specified by src, and write the transformed points into the array of points specified by dst. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [mapPoints](../android/graphics/Matrix.md))`(`dst:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `dstIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `src:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `srcIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `pointCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Apply this matrix to the array of 2D points specified by src, and write the transformed points into the array of points specified by dst. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [mapRadius](../android/graphics/Matrix.md))`(`radius:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Return the mean radius of a circle after it has been mapped by this matrix. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [mapRect](../android/graphics/Matrix.md))`(`rect:` ` [RectF](../android/graphics/RectF.md)!`)` Apply this matrix to the rectangle, and write the transformed rectangle back into it. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [mapRect](../android/graphics/Matrix.md))`(`dst:` ` [RectF](../android/graphics/RectF.md)!`, `src:` ` [RectF](../android/graphics/RectF.md)!`)` Apply this matrix to the src rectangle, and write the transformed rectangle into dst. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [mapVectors](../android/graphics/Matrix.md))`(`vecs:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`)` Apply this matrix to the array of 2D vectors, and write the transformed vectors back into the array. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [mapVectors](../android/graphics/Matrix.md))`(`dst:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `src:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`)` Apply this matrix to the array of 2D vectors specified by src, and write the transformed vectors into the array of vectors specified by dst. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [mapVectors](../android/graphics/Matrix.md))`(`dst:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `dstIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `src:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `srcIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `vectorCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Apply this matrix to the array of 2D vectors specified by src, and write the transformed vectors into the array of vectors specified by dst. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [postConcat](../android/graphics/Matrix.md))`(`other:` ` [Matrix](../android/graphics/Matrix.md)!`)` Postconcats the matrix with the specified matrix. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [postRotate](../android/graphics/Matrix.md))`(`degrees:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Postconcats the matrix with the specified rotation. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [postRotate](../android/graphics/Matrix.md))`(`degrees:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `px:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `py:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Postconcats the matrix with the specified rotation. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [postScale](../android/graphics/Matrix.md))`(`sx:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `sy:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Postconcats the matrix with the specified scale. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [postScale](../android/graphics/Matrix.md))`(`sx:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `sy:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `px:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `py:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Postconcats the matrix with the specified scale. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [postSkew](../android/graphics/Matrix.md))`(`kx:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `ky:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Postconcats the matrix with the specified skew. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [postSkew](../android/graphics/Matrix.md))`(`kx:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `ky:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `px:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `py:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Postconcats the matrix with the specified skew. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [postTranslate](../android/graphics/Matrix.md))`(`dx:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `dy:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Postconcats the matrix with the specified translation. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [preConcat](../android/graphics/Matrix.md))`(`other:` ` [Matrix](../android/graphics/Matrix.md)!`)` Preconcats the matrix with the specified matrix. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [preRotate](../android/graphics/Matrix.md))`(`degrees:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Preconcats the matrix with the specified rotation. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [preRotate](../android/graphics/Matrix.md))`(`degrees:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `px:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `py:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Preconcats the matrix with the specified rotation. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [preScale](../android/graphics/Matrix.md))`(`sx:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `sy:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Preconcats the matrix with the specified scale. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [preScale](../android/graphics/Matrix.md))`(`sx:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `sy:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `px:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `py:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Preconcats the matrix with the specified scale. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [preSkew](../android/graphics/Matrix.md))`(`kx:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `ky:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Preconcats the matrix with the specified skew. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [preSkew](../android/graphics/Matrix.md))`(`kx:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `ky:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `px:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `py:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Preconcats the matrix with the specified skew. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [preTranslate](../android/graphics/Matrix.md))`(`dx:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `dy:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Preconcats the matrix with the specified translation. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [rectStaysRect](../android/graphics/Matrix.md))`()` Returns true if will map a rectangle to another rectangle. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reset](../android/graphics/Matrix.md))`()` Set the matrix to identity |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [set](../android/graphics/Matrix.md))`(`src:` ` [Matrix](../android/graphics/Matrix.md)!`)` (deep) copy the src matrix into this matrix. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setConcat](../android/graphics/Matrix.md))`(`a:` ` [Matrix](../android/graphics/Matrix.md)!`, `b:` ` [Matrix](../android/graphics/Matrix.md)!`)` Set the matrix to the concatenation of the two specified matrices and return true. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setPolyToPoly](../android/graphics/Matrix.md))`(`src:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `srcIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dst:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `dstIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `pointCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the matrix such that the specified src points would map to the specified dst points. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setRectToRect](../android/graphics/Matrix.md))`(`src:` ` [RectF](../android/graphics/RectF.md)!`, `dst:` ` [RectF](../android/graphics/RectF.md)!`, `stf:` ` [Matrix.ScaleToFit](../android/graphics/Matrix.ScaleToFit.md)!`)` Set the matrix to the scale and translate values that map the source rectangle to the destination rectangle, returning true if the result can be represented. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRotate](../android/graphics/Matrix.md))`(`degrees:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Set the matrix to rotate about (0,0) by the specified number of degrees. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRotate](../android/graphics/Matrix.md))`(`degrees:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `px:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `py:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Set the matrix to rotate by the specified number of degrees, with a pivot point at (px, py). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setScale](../android/graphics/Matrix.md))`(`sx:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `sy:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Set the matrix to scale by sx and sy. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setScale](../android/graphics/Matrix.md))`(`sx:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `sy:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `px:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `py:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Set the matrix to scale by sx and sy, with a pivot point at (px, py). |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSinCos](../android/graphics/Matrix.md))`(`sinValue:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `cosValue:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Set the matrix to rotate by the specified sine and cosine values. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSinCos](../android/graphics/Matrix.md))`(`sinValue:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `cosValue:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `px:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `py:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Set the matrix to rotate by the specified sine and cosine values, with a pivot point at (px, py). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSkew](../android/graphics/Matrix.md))`(`kx:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `ky:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Set the matrix to skew by sx and sy. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSkew](../android/graphics/Matrix.md))`(`kx:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `ky:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `px:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `py:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Set the matrix to skew by sx and sy, with a pivot point at (px, py). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTranslate](../android/graphics/Matrix.md))`(`dx:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `dy:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Set the matrix to translate by (dx, dy). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setValues](../android/graphics/Matrix.md))`(`values:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`)` Copy 9 values from the array into the matrix. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toShortString](../android/graphics/Matrix.md))`()` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/graphics/Matrix.md))`()` <br /> |

| Properties ||
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Matrix](../android/graphics/Matrix.md) | [IDENTITY_MATRIX](../android/graphics/Matrix.md) The identity matrix. |

## Constants

### MPERSP_0

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MPERSP_0: Int
```  

 Value: 6

### MPERSP_1

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MPERSP_1: Int
```  

 Value: 7

### MPERSP_2

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MPERSP_2: Int
```  

 Value: 8

### MSCALE_X

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MSCALE_X: Int
```  

 Value: 0

### MSCALE_Y

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MSCALE_Y: Int
```  

 Value: 4

### MSKEW_X

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MSKEW_X: Int
```  

 Value: 1

### MSKEW_Y

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MSKEW_Y: Int
```  

 Value: 3

### MTRANS_X

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MTRANS_X: Int
```  

 Value: 2

### MTRANS_Y

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MTRANS_Y: Int
```  

 Value: 5

## Public constructors

### Matrix

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Matrix()
```

Create an identity matrix 

### Matrix

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Matrix(src: Matrix!)
```

Create a matrix that is a (deep) copy of src

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------------|
| `src` | [Matrix](../android/graphics/Matrix.md)!:The matrix to copy into this matrix |

## Public methods

### dump

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun dump(pw: PrintWriter): Unit
```

Dumps a human-readable shortened string of the matrix into the given stream

| Parameters ||
|------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pw` | [PrintWriter](../java/io/PrintWriter.md):The [PrintWriter](../java/io/PrintWriter.md) into which the string representation of the matrix will be written. This value cannot be`null`. |

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

Returns true iff obj is a Matrix and its values equal our values.

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getValues

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getValues(values: FloatArray!): Unit
```

Copy 9 values from the matrix into the array. 

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### invert

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun invert(inverse: Matrix!): Boolean
```

If this matrix can be inverted, return true and if inverse is not null, set inverse to be the inverse of this matrix. If this matrix cannot be inverted, ignore inverse and return false. 

### isAffine

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isAffine(): Boolean
```

Gets whether this matrix is affine. An affine matrix preserves straight lines and has no perspective.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Whether the matrix is affine. |

### isIdentity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isIdentity(): Boolean
```

Returns true if the matrix is identity. This maybe faster than testing if (getType() == 0) 

### mapPoints

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun mapPoints(pts: FloatArray!): Unit
```

Apply this matrix to the array of 2D points, and write the transformed points back into the array

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pts` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:The array \[x0, y0, x1, y1, ...\] of points to transform. |

### mapPoints

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun mapPoints(
    dst: FloatArray!, 
    src: FloatArray!
): Unit
```

Apply this matrix to the array of 2D points specified by src, and write the transformed points into the array of points specified by dst. The two arrays represent their "points" as pairs of floats \[x, y\].

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------------|
| `dst` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:The array of dst points (x,y pairs) |
| `src` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:The array of src points (x,y pairs) |

### mapPoints

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun mapPoints(
    dst: FloatArray!, 
    dstIndex: Int, 
    src: FloatArray!, 
    srcIndex: Int, 
    pointCount: Int
): Unit
```

Apply this matrix to the array of 2D points specified by src, and write the transformed points into the array of points specified by dst. The two arrays represent their "points" as pairs of floats \[x, y\].

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------|
| `dst` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:The array of dst points (x,y pairs) |
| `dstIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index of the first \[x,y\] pair of dst floats |
| `src` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:The array of src points (x,y pairs) |
| --- | --- |
| `srcIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index of the first \[x,y\] pair of src floats |
| `pointCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The number of points (x,y pairs) to transform |

### mapRadius

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun mapRadius(radius: Float): Float
```

Return the mean radius of a circle after it has been mapped by this matrix. NOTE: in perspective this value assumes the circle has its center at the origin. 

### mapRect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun mapRect(rect: RectF!): Boolean
```

Apply this matrix to the rectangle, and write the transformed rectangle back into it. This is accomplished by transforming the 4 corners of rect, and then setting it to the bounds of those points

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------|
| `rect` | [RectF](../android/graphics/RectF.md)!:The rectangle to transform. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | the result of calling rectStaysRect() |

### mapRect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun mapRect(
    dst: RectF!, 
    src: RectF!
): Boolean
```

Apply this matrix to the src rectangle, and write the transformed rectangle into dst. This is accomplished by transforming the 4 corners of src, and then setting dst to the bounds of those points.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------------|
| `dst` | [RectF](../android/graphics/RectF.md)!:Where the transformed rectangle is written. |
| `src` | [RectF](../android/graphics/RectF.md)!:The original rectangle to be transformed. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | the result of calling rectStaysRect() |

### mapVectors

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun mapVectors(vecs: FloatArray!): Unit
```

Apply this matrix to the array of 2D vectors, and write the transformed vectors back into the array. Note: this method does not apply the translation associated with the matrix. Use[Matrix.mapPoints(float[])](https://developer.android.com/reference/kotlin/android/graphics/Matrix#mapPoints(kotlin.FloatArray))if you want the translation to be applied.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| `vecs` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:The array \[x0, y0, x1, y1, ...\] of vectors to transform. |

### mapVectors

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun mapVectors(
    dst: FloatArray!, 
    src: FloatArray!
): Unit
```

Apply this matrix to the array of 2D vectors specified by src, and write the transformed vectors into the array of vectors specified by dst. The two arrays represent their "vectors" as pairs of floats \[x, y\]. Note: this method does not apply the translation associated with the matrix. Use[Matrix.mapPoints(float[], float[])](https://developer.android.com/reference/kotlin/android/graphics/Matrix#mapPoints(kotlin.FloatArray,%20kotlin.FloatArray))if you want the translation to be applied.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------------|
| `dst` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:The array of dst vectors (x,y pairs) |
| `src` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:The array of src vectors (x,y pairs) |

### mapVectors

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun mapVectors(
    dst: FloatArray!, 
    dstIndex: Int, 
    src: FloatArray!, 
    srcIndex: Int, 
    vectorCount: Int
): Unit
```

Apply this matrix to the array of 2D vectors specified by src, and write the transformed vectors into the array of vectors specified by dst. The two arrays represent their "vectors" as pairs of floats \[x, y\]. Note: this method does not apply the translation associated with the matrix. Use[Matrix.mapPoints(float[], int, float[], int, int)](https://developer.android.com/reference/kotlin/android/graphics/Matrix#mapPoints(kotlin.FloatArray,%20kotlin.Int,%20kotlin.FloatArray,%20kotlin.Int,%20kotlin.Int))if you want the translation to be applied.

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------|
| `dst` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:The array of dst vectors (x,y pairs) |
| `dstIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index of the first \[x,y\] pair of dst floats |
| `src` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:The array of src vectors (x,y pairs) |
| --- | --- |
| `srcIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index of the first \[x,y\] pair of src floats |
| `vectorCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The number of vectors (x,y pairs) to transform |

### postConcat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun postConcat(other: Matrix!): Boolean
```

Postconcats the matrix with the specified matrix. M' = other \* M 

### postRotate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun postRotate(degrees: Float): Boolean
```

Postconcats the matrix with the specified rotation. M' = R(degrees) \* M 

### postRotate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun postRotate(
    degrees: Float, 
    px: Float, 
    py: Float
): Boolean
```

Postconcats the matrix with the specified rotation. M' = R(degrees, px, py) \* M 

### postScale

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun postScale(
    sx: Float, 
    sy: Float
): Boolean
```

Postconcats the matrix with the specified scale. M' = S(sx, sy) \* M 

### postScale

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun postScale(
    sx: Float, 
    sy: Float, 
    px: Float, 
    py: Float
): Boolean
```

Postconcats the matrix with the specified scale. M' = S(sx, sy, px, py) \* M 

### postSkew

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun postSkew(
    kx: Float, 
    ky: Float
): Boolean
```

Postconcats the matrix with the specified skew. M' = K(kx, ky) \* M 

### postSkew

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun postSkew(
    kx: Float, 
    ky: Float, 
    px: Float, 
    py: Float
): Boolean
```

Postconcats the matrix with the specified skew. M' = K(kx, ky, px, py) \* M 

### postTranslate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun postTranslate(
    dx: Float, 
    dy: Float
): Boolean
```

Postconcats the matrix with the specified translation. M' = T(dx, dy) \* M 

### preConcat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun preConcat(other: Matrix!): Boolean
```

Preconcats the matrix with the specified matrix. M' = M \* other 

### preRotate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun preRotate(degrees: Float): Boolean
```

Preconcats the matrix with the specified rotation. M' = M \* R(degrees) 

### preRotate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun preRotate(
    degrees: Float, 
    px: Float, 
    py: Float
): Boolean
```

Preconcats the matrix with the specified rotation. M' = M \* R(degrees, px, py) 

### preScale

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun preScale(
    sx: Float, 
    sy: Float
): Boolean
```

Preconcats the matrix with the specified scale. M' = M \* S(sx, sy) 

### preScale

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun preScale(
    sx: Float, 
    sy: Float, 
    px: Float, 
    py: Float
): Boolean
```

Preconcats the matrix with the specified scale. M' = M \* S(sx, sy, px, py) 

### preSkew

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun preSkew(
    kx: Float, 
    ky: Float
): Boolean
```

Preconcats the matrix with the specified skew. M' = M \* K(kx, ky) 

### preSkew

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun preSkew(
    kx: Float, 
    ky: Float, 
    px: Float, 
    py: Float
): Boolean
```

Preconcats the matrix with the specified skew. M' = M \* K(kx, ky, px, py) 

### preTranslate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun preTranslate(
    dx: Float, 
    dy: Float
): Boolean
```

Preconcats the matrix with the specified translation. M' = M \* T(dx, dy) 

### rectStaysRect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun rectStaysRect(): Boolean
```

Returns true if will map a rectangle to another rectangle. This can be true if the matrix is identity, scale-only, or rotates a multiple of 90 degrees. 

### reset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun reset(): Unit
```

Set the matrix to identity 

### set

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun set(src: Matrix!): Unit
```

(deep) copy the src matrix into this matrix. If src is null, reset this matrix to the identity matrix. 

### setConcat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setConcat(
    a: Matrix!, 
    b: Matrix!
): Boolean
```

Set the matrix to the concatenation of the two specified matrices and return true.

Either of the two matrices may also be the target matrix, that is`matrixA.setConcat(matrixA, matrixB);`is valid.

In [android.os.Build.VERSION_CODES#GINGERBREAD_MR1](../android/os/Build.VERSION_CODES.md) and below, this function returns true only if the result can be represented. In [android.os.Build.VERSION_CODES#HONEYCOMB](../android/os/Build.VERSION_CODES.md) and above, it always returns true. 

### setPolyToPoly

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPolyToPoly(
    src: FloatArray!, 
    srcIndex: Int, 
    dst: FloatArray!, 
    dstIndex: Int, 
    pointCount: Int
): Boolean
```

Set the matrix such that the specified src points would map to the specified dst points. The "points" are represented as an array of floats, order \[x0, y0, x1, y1, ...\], where each "point" is 2 float values.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------|
| `src` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:The array of src \[x,y\] pairs (points) |
| `srcIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Index of the first pair of src values |
| `dst` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:The array of dst \[x,y\] pairs (points) |
| --- | --- |
| `dstIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Index of the first pair of dst values |
| `pointCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The number of pairs/points to be used. Must be \[0..4\] |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the matrix was set to the specified transformation |

### setRectToRect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setRectToRect(
    src: RectF!, 
    dst: RectF!, 
    stf: Matrix.ScaleToFit!
): Boolean
```

Set the matrix to the scale and translate values that map the source rectangle to the destination rectangle, returning true if the result can be represented.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------------------|
| `src` | [RectF](../android/graphics/RectF.md)!:the source rectangle to map from. |
| `dst` | [RectF](../android/graphics/RectF.md)!:the destination rectangle to map to. |
| `stf` | [Matrix.ScaleToFit](../android/graphics/Matrix.ScaleToFit.md)!:the ScaleToFit option |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the matrix can be represented by the rectangle mapping. |

### setRotate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setRotate(degrees: Float): Unit
```

Set the matrix to rotate about (0,0) by the specified number of degrees. 

### setRotate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setRotate(
    degrees: Float, 
    px: Float, 
    py: Float
): Unit
```

Set the matrix to rotate by the specified number of degrees, with a pivot point at (px, py). The pivot point is the coordinate that should remain unchanged by the specified transformation. 

### setScale

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setScale(
    sx: Float, 
    sy: Float
): Unit
```

Set the matrix to scale by sx and sy. 

### setScale

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setScale(
    sx: Float, 
    sy: Float, 
    px: Float, 
    py: Float
): Unit
```

Set the matrix to scale by sx and sy, with a pivot point at (px, py). The pivot point is the coordinate that should remain unchanged by the specified transformation. 

### setSinCos

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSinCos(
    sinValue: Float, 
    cosValue: Float
): Unit
```

Set the matrix to rotate by the specified sine and cosine values. 

### setSinCos

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSinCos(
    sinValue: Float, 
    cosValue: Float, 
    px: Float, 
    py: Float
): Unit
```

Set the matrix to rotate by the specified sine and cosine values, with a pivot point at (px, py). The pivot point is the coordinate that should remain unchanged by the specified transformation. 

### setSkew

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSkew(
    kx: Float, 
    ky: Float
): Unit
```

Set the matrix to skew by sx and sy. 

### setSkew

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSkew(
    kx: Float, 
    ky: Float, 
    px: Float, 
    py: Float
): Unit
```

Set the matrix to skew by sx and sy, with a pivot point at (px, py). The pivot point is the coordinate that should remain unchanged by the specified transformation. 

### setTranslate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTranslate(
    dx: Float, 
    dy: Float
): Unit
```

Set the matrix to translate by (dx, dy). 

### setValues

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setValues(values: FloatArray!): Unit
```

Copy 9 values from the array into the matrix. Depending on the implementation of Matrix, these may be transformed into 16.16 integers in the Matrix, such that a subsequent call to getValues() will not yield exactly the same values. 

### toShortString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toShortString(): String!
```  

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

## Properties

### IDENTITY_MATRIX

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val IDENTITY_MATRIX: Matrix
```

The identity matrix. Multiplying by another matrix`M`returns`M`. This matrix is immutable, and attempting to modify it will throw an [IllegalStateException](../java/lang/IllegalStateException.md).
