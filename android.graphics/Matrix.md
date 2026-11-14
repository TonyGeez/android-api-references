# Matrix

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Matrix

Kotlin| [Java](https://developer.android.com/reference/android/graphics/Matrix "View this page in Java") 
| --- | --- |

```
open class Matrix
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.Matrix](https://developer.android.com/reference/kotlin/android/graphics/Matrix#) |

The Matrix class holds a 3x3 matrix for transforming coordinates.

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [ScaleToFit](https://developer.android.com/reference/kotlin/android/graphics/Matrix.ScaleToFit) Controls how the src rect should align into the dst rect for setRectToRect(). |

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MPERSP_0](https://developer.android.com/reference/kotlin/android/graphics/Matrix#MPERSP_0:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MPERSP_1](https://developer.android.com/reference/kotlin/android/graphics/Matrix#MPERSP_1:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MPERSP_2](https://developer.android.com/reference/kotlin/android/graphics/Matrix#MPERSP_2:kotlin.Int) <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MSCALE_X](https://developer.android.com/reference/kotlin/android/graphics/Matrix#MSCALE_X:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MSCALE_Y](https://developer.android.com/reference/kotlin/android/graphics/Matrix#MSCALE_Y:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MSKEW_X](https://developer.android.com/reference/kotlin/android/graphics/Matrix#MSKEW_X:kotlin.Int) <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MSKEW_Y](https://developer.android.com/reference/kotlin/android/graphics/Matrix#MSKEW_Y:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MTRANS_X](https://developer.android.com/reference/kotlin/android/graphics/Matrix#MTRANS_X:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MTRANS_Y](https://developer.android.com/reference/kotlin/android/graphics/Matrix#MTRANS_Y:kotlin.Int) <br /> |
| --- | --- |

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Matrix](https://developer.android.com/reference/kotlin/android/graphics/Matrix#Matrix())`()` Create an identity matrix |
| [Matrix](https://developer.android.com/reference/kotlin/android/graphics/Matrix#Matrix(android.graphics.Matrix))`(`src:` ` [Matrix](https://developer.android.com/reference/kotlin/android/graphics/Matrix#)!`)` Create a matrix that is a (deep) copy of src |

| Public methods ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dump](https://developer.android.com/reference/kotlin/android/graphics/Matrix#dump(java.io.PrintWriter))`(`pw:` ` [PrintWriter](https://developer.android.com/reference/kotlin/java/io/PrintWriter.html#)`)` Dumps a human-readable shortened string of the matrix into the given stream |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/graphics/Matrix#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Returns true iff obj is a Matrix and its values equal our values. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getValues](https://developer.android.com/reference/kotlin/android/graphics/Matrix#getValues(kotlin.FloatArray))`(`values:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`)` Copy 9 values from the matrix into the array. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/graphics/Matrix#hashCode())`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [invert](https://developer.android.com/reference/kotlin/android/graphics/Matrix#invert(android.graphics.Matrix))`(`inverse:` ` [Matrix](https://developer.android.com/reference/kotlin/android/graphics/Matrix#)!`)` If this matrix can be inverted, return true and if inverse is not null, set inverse to be the inverse of this matrix. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAffine](https://developer.android.com/reference/kotlin/android/graphics/Matrix#isAffine())`()` Gets whether this matrix is affine. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isIdentity](https://developer.android.com/reference/kotlin/android/graphics/Matrix#isIdentity())`()` Returns true if the matrix is identity. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [mapPoints](https://developer.android.com/reference/kotlin/android/graphics/Matrix#mapPoints(kotlin.FloatArray))`(`pts:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`)` Apply this matrix to the array of 2D points, and write the transformed points back into the array |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [mapPoints](https://developer.android.com/reference/kotlin/android/graphics/Matrix#mapPoints(kotlin.FloatArray,%20kotlin.FloatArray))`(`dst:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `src:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`)` Apply this matrix to the array of 2D points specified by src, and write the transformed points into the array of points specified by dst. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [mapPoints](https://developer.android.com/reference/kotlin/android/graphics/Matrix#mapPoints(kotlin.FloatArray,%20kotlin.Int,%20kotlin.FloatArray,%20kotlin.Int,%20kotlin.Int))`(`dst:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `dstIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `src:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `srcIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `pointCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Apply this matrix to the array of 2D points specified by src, and write the transformed points into the array of points specified by dst. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [mapRadius](https://developer.android.com/reference/kotlin/android/graphics/Matrix#mapRadius(kotlin.Float))`(`radius:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Return the mean radius of a circle after it has been mapped by this matrix. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [mapRect](https://developer.android.com/reference/kotlin/android/graphics/Matrix#mapRect(android.graphics.RectF))`(`rect:` ` [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF)!`)` Apply this matrix to the rectangle, and write the transformed rectangle back into it. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [mapRect](https://developer.android.com/reference/kotlin/android/graphics/Matrix#mapRect(android.graphics.RectF,%20android.graphics.RectF))`(`dst:` ` [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF)!`, `src:` ` [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF)!`)` Apply this matrix to the src rectangle, and write the transformed rectangle into dst. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [mapVectors](https://developer.android.com/reference/kotlin/android/graphics/Matrix#mapVectors(kotlin.FloatArray))`(`vecs:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`)` Apply this matrix to the array of 2D vectors, and write the transformed vectors back into the array. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [mapVectors](https://developer.android.com/reference/kotlin/android/graphics/Matrix#mapVectors(kotlin.FloatArray,%20kotlin.FloatArray))`(`dst:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `src:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`)` Apply this matrix to the array of 2D vectors specified by src, and write the transformed vectors into the array of vectors specified by dst. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [mapVectors](https://developer.android.com/reference/kotlin/android/graphics/Matrix#mapVectors(kotlin.FloatArray,%20kotlin.Int,%20kotlin.FloatArray,%20kotlin.Int,%20kotlin.Int))`(`dst:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `dstIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `src:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `srcIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `vectorCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Apply this matrix to the array of 2D vectors specified by src, and write the transformed vectors into the array of vectors specified by dst. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [postConcat](https://developer.android.com/reference/kotlin/android/graphics/Matrix#postConcat(android.graphics.Matrix))`(`other:` ` [Matrix](https://developer.android.com/reference/kotlin/android/graphics/Matrix#)!`)` Postconcats the matrix with the specified matrix. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [postRotate](https://developer.android.com/reference/kotlin/android/graphics/Matrix#postRotate(kotlin.Float))`(`degrees:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Postconcats the matrix with the specified rotation. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [postRotate](https://developer.android.com/reference/kotlin/android/graphics/Matrix#postRotate(kotlin.Float,%20kotlin.Float,%20kotlin.Float))`(`degrees:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `px:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `py:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Postconcats the matrix with the specified rotation. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [postScale](https://developer.android.com/reference/kotlin/android/graphics/Matrix#postScale(kotlin.Float,%20kotlin.Float))`(`sx:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `sy:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Postconcats the matrix with the specified scale. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [postScale](https://developer.android.com/reference/kotlin/android/graphics/Matrix#postScale(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float))`(`sx:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `sy:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `px:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `py:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Postconcats the matrix with the specified scale. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [postSkew](https://developer.android.com/reference/kotlin/android/graphics/Matrix#postSkew(kotlin.Float,%20kotlin.Float))`(`kx:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `ky:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Postconcats the matrix with the specified skew. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [postSkew](https://developer.android.com/reference/kotlin/android/graphics/Matrix#postSkew(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float))`(`kx:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `ky:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `px:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `py:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Postconcats the matrix with the specified skew. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [postTranslate](https://developer.android.com/reference/kotlin/android/graphics/Matrix#postTranslate(kotlin.Float,%20kotlin.Float))`(`dx:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `dy:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Postconcats the matrix with the specified translation. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [preConcat](https://developer.android.com/reference/kotlin/android/graphics/Matrix#preConcat(android.graphics.Matrix))`(`other:` ` [Matrix](https://developer.android.com/reference/kotlin/android/graphics/Matrix#)!`)` Preconcats the matrix with the specified matrix. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [preRotate](https://developer.android.com/reference/kotlin/android/graphics/Matrix#preRotate(kotlin.Float))`(`degrees:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Preconcats the matrix with the specified rotation. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [preRotate](https://developer.android.com/reference/kotlin/android/graphics/Matrix#preRotate(kotlin.Float,%20kotlin.Float,%20kotlin.Float))`(`degrees:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `px:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `py:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Preconcats the matrix with the specified rotation. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [preScale](https://developer.android.com/reference/kotlin/android/graphics/Matrix#preScale(kotlin.Float,%20kotlin.Float))`(`sx:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `sy:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Preconcats the matrix with the specified scale. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [preScale](https://developer.android.com/reference/kotlin/android/graphics/Matrix#preScale(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float))`(`sx:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `sy:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `px:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `py:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Preconcats the matrix with the specified scale. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [preSkew](https://developer.android.com/reference/kotlin/android/graphics/Matrix#preSkew(kotlin.Float,%20kotlin.Float))`(`kx:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `ky:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Preconcats the matrix with the specified skew. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [preSkew](https://developer.android.com/reference/kotlin/android/graphics/Matrix#preSkew(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float))`(`kx:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `ky:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `px:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `py:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Preconcats the matrix with the specified skew. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [preTranslate](https://developer.android.com/reference/kotlin/android/graphics/Matrix#preTranslate(kotlin.Float,%20kotlin.Float))`(`dx:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `dy:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Preconcats the matrix with the specified translation. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [rectStaysRect](https://developer.android.com/reference/kotlin/android/graphics/Matrix#rectStaysRect())`()` Returns true if will map a rectangle to another rectangle. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reset](https://developer.android.com/reference/kotlin/android/graphics/Matrix#reset())`()` Set the matrix to identity |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [set](https://developer.android.com/reference/kotlin/android/graphics/Matrix#set(android.graphics.Matrix))`(`src:` ` [Matrix](https://developer.android.com/reference/kotlin/android/graphics/Matrix#)!`)` (deep) copy the src matrix into this matrix. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setConcat](https://developer.android.com/reference/kotlin/android/graphics/Matrix#setConcat(android.graphics.Matrix,%20android.graphics.Matrix))`(`a:` ` [Matrix](https://developer.android.com/reference/kotlin/android/graphics/Matrix#)!`, `b:` ` [Matrix](https://developer.android.com/reference/kotlin/android/graphics/Matrix#)!`)` Set the matrix to the concatenation of the two specified matrices and return true. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setPolyToPoly](https://developer.android.com/reference/kotlin/android/graphics/Matrix#setPolyToPoly(kotlin.FloatArray,%20kotlin.Int,%20kotlin.FloatArray,%20kotlin.Int,%20kotlin.Int))`(`src:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `srcIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dst:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `dstIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `pointCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the matrix such that the specified src points would map to the specified dst points. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setRectToRect](https://developer.android.com/reference/kotlin/android/graphics/Matrix#setRectToRect(android.graphics.RectF,%20android.graphics.RectF,%20android.graphics.Matrix.ScaleToFit))`(`src:` ` [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF)!`, `dst:` ` [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF)!`, `stf:` ` [Matrix.ScaleToFit](https://developer.android.com/reference/kotlin/android/graphics/Matrix.ScaleToFit)!`)` Set the matrix to the scale and translate values that map the source rectangle to the destination rectangle, returning true if the result can be represented. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRotate](https://developer.android.com/reference/kotlin/android/graphics/Matrix#setRotate(kotlin.Float))`(`degrees:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Set the matrix to rotate about (0,0) by the specified number of degrees. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRotate](https://developer.android.com/reference/kotlin/android/graphics/Matrix#setRotate(kotlin.Float,%20kotlin.Float,%20kotlin.Float))`(`degrees:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `px:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `py:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Set the matrix to rotate by the specified number of degrees, with a pivot point at (px, py). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setScale](https://developer.android.com/reference/kotlin/android/graphics/Matrix#setScale(kotlin.Float,%20kotlin.Float))`(`sx:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `sy:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Set the matrix to scale by sx and sy. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setScale](https://developer.android.com/reference/kotlin/android/graphics/Matrix#setScale(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float))`(`sx:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `sy:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `px:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `py:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Set the matrix to scale by sx and sy, with a pivot point at (px, py). |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSinCos](https://developer.android.com/reference/kotlin/android/graphics/Matrix#setSinCos(kotlin.Float,%20kotlin.Float))`(`sinValue:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `cosValue:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Set the matrix to rotate by the specified sine and cosine values. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSinCos](https://developer.android.com/reference/kotlin/android/graphics/Matrix#setSinCos(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float))`(`sinValue:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `cosValue:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `px:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `py:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Set the matrix to rotate by the specified sine and cosine values, with a pivot point at (px, py). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSkew](https://developer.android.com/reference/kotlin/android/graphics/Matrix#setSkew(kotlin.Float,%20kotlin.Float))`(`kx:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `ky:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Set the matrix to skew by sx and sy. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSkew](https://developer.android.com/reference/kotlin/android/graphics/Matrix#setSkew(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float))`(`kx:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `ky:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `px:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `py:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Set the matrix to skew by sx and sy, with a pivot point at (px, py). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTranslate](https://developer.android.com/reference/kotlin/android/graphics/Matrix#setTranslate(kotlin.Float,%20kotlin.Float))`(`dx:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `dy:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Set the matrix to translate by (dx, dy). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setValues](https://developer.android.com/reference/kotlin/android/graphics/Matrix#setValues(kotlin.FloatArray))`(`values:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`)` Copy 9 values from the array into the matrix. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toShortString](https://developer.android.com/reference/kotlin/android/graphics/Matrix#toShortString())`()` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/graphics/Matrix#toString())`()` <br /> |

| Properties ||
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Matrix](https://developer.android.com/reference/kotlin/android/graphics/Matrix#) | [IDENTITY_MATRIX](https://developer.android.com/reference/kotlin/android/graphics/Matrix#IDENTITY_MATRIX:android.graphics.Matrix) The identity matrix. |

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
| `src` | [Matrix](https://developer.android.com/reference/kotlin/android/graphics/Matrix#)!:The matrix to copy into this matrix |

## Public methods

### dump

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun dump(pw: PrintWriter): Unit
```

Dumps a human-readable shortened string of the matrix into the given stream

| Parameters ||
|------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pw` | [PrintWriter](https://developer.android.com/reference/kotlin/java/io/PrintWriter.html#):The [PrintWriter](https://developer.android.com/reference/kotlin/java/io/PrintWriter.html#) into which the string representation of the matrix will be written. This value cannot be`null`. |

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
| `rect` | [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF)!:The rectangle to transform. |

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
| `dst` | [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF)!:Where the transformed rectangle is written. |
| `src` | [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF)!:The original rectangle to be transformed. |

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

In [android.os.Build.VERSION_CODES#GINGERBREAD_MR1](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#GINGERBREAD_MR1:kotlin.Int) and below, this function returns true only if the result can be represented. In [android.os.Build.VERSION_CODES#HONEYCOMB](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#HONEYCOMB:kotlin.Int) and above, it always returns true. 

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
| `src` | [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF)!:the source rectangle to map from. |
| `dst` | [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF)!:the destination rectangle to map to. |
| `stf` | [Matrix.ScaleToFit](https://developer.android.com/reference/kotlin/android/graphics/Matrix.ScaleToFit)!:the ScaleToFit option |
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

The identity matrix. Multiplying by another matrix`M`returns`M`. This matrix is immutable, and attempting to modify it will throw an [IllegalStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#).
