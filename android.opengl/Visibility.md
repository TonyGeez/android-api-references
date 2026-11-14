# Visibility

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Visibility

Kotlin| [Java](Visibility.md) 
| --- | --- |

```
open class Visibility
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.opengl.Visibility](Visibility.md) |

A collection of utility methods for computing the visibility of triangle meshes.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------|---|
| [Visibility](Visibility.md))`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [computeBoundingSphere](Visibility.md))`(`positions:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `positionsOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `positionsCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `sphere:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `sphereOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Compute a bounding sphere for a set of points. |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [frustumCullSpheres](Visibility.md))`(`mvp:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `mvpOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `spheres:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `spheresOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `spheresCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `results:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`, `resultsOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `resultsCapacity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Given an OpenGL ES ModelView-Projection matrix (which implicitly describes a frustum) and a list of spheres, determine which spheres intersect the frustum. |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [visibilityTest](Visibility.md))`(`ws:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `wsOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `positions:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `positionsOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `indices:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `indicesOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `indexCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Test whether a given triangle mesh is visible on the screen. |
| --- | --- |

## Public constructors

### Visibility

```
Visibility()
```

## Public methods

### computeBoundingSphere

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun computeBoundingSphere(
    positions: FloatArray!, 
    positionsOffset: Int, 
    positionsCount: Int, 
    sphere: FloatArray!, 
    sphereOffset: Int
): Unit
```

Compute a bounding sphere for a set of points. It is approximately the minimal bounding sphere of an axis-aligned box that bounds the points.

| Parameters ||
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| `positions` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:positions in x, y, z triples |
| `positionsOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):offset into positions array |
| `positionsCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):number of position triples to process |
| --- | --- |
| `sphere` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:array containing the output as (x, y, z, r) |
| `sphereOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):offset where the sphere data will be written |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if positions is null, positionsOffset \< 0, positionsOffset \> positions.length - positionsCount, sphere is null, sphereOffset \< 0, sphereOffset \> sphere.length - 4. |

### frustumCullSpheres

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun frustumCullSpheres(
    mvp: FloatArray!, 
    mvpOffset: Int, 
    spheres: FloatArray!, 
    spheresOffset: Int, 
    spheresCount: Int, 
    results: IntArray!, 
    resultsOffset: Int, 
    resultsCapacity: Int
): Int
```

Given an OpenGL ES ModelView-Projection matrix (which implicitly describes a frustum) and a list of spheres, determine which spheres intersect the frustum.

A ModelView-Projection matrix can be computed by multiplying the a Projection matrix by the a ModelView matrix (in that order.). There are several possible ways to obtain the current ModelView and Projection matrices. The most generally applicable way is to keep track of the current matrices in application code. If that is not convenient, there are two optional OpenGL ES extensions which may be used to read the current matrices from OpenGL ES:

- GL10Ext.glQueryMatrixxOES
- GL11.GL_MODELVIEW_MATRIX_FLOAT_AS_INT_BITS_OES and GL_PROJECTION_MATRIX_FLOAT_AS_INT_BITS_OES

The problem with reading back the matrices is that your application will only work with devices that support the extension(s) that it uses.

A frustum is a six-sided truncated pyramid that defines the portion of world space that is visible in the view.

Spheres are described as four floating point values: x, y, z, and r, in world-space coordinates. R is the radius of the sphere.

<br />

| Parameters ||
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mvp` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:a float array containing the mode-view-projection matrix |
| `mvpOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The offset of the mvp data within the mvp array. |
| `spheres` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:a float array containing the sphere data. |
| --- | --- |
| `spheresOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):an offset into the sphere array where the sphere data starts |
| `spheresCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of spheres to cull. |
| `results` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!:an integer array containing the indices of the spheres that are either contained entirely within or intersect the frustum. |
| --- | --- |
| `resultsOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):an offset into the results array where the results start. |
| `resultsCapacity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of array elements available for storing results. |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of spheres that intersected the frustum. Can be larger than resultsCapacity, in which case only the first resultsCapacity results are written into the results array. |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if mvp is null, mvpOffset \< 0, mvpOffset \> mvp.length - 16, spheres is null, spheresOffset \< 0, spheresOffset \> spheres.length - sphereCount, results is null, resultsOffset \< 0, resultsOffset \> results.length - resultsCapacity. |

### visibilityTest

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun visibilityTest(
    ws: FloatArray!, 
    wsOffset: Int, 
    positions: FloatArray!, 
    positionsOffset: Int, 
    indices: CharArray!, 
    indicesOffset: Int, 
    indexCount: Int
): Int
```

Test whether a given triangle mesh is visible on the screen. The mesh is specified as an indexed triangle list.

| Parameters ||
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ws` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:the world space to screen space transform matrix, as an OpenGL column matrix. |
| `wsOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):an index into the ws array where the data starts. |
| `positions` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:the vertex positions (x, y, z). |
| --- | --- |
| `positionsOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index in the positions array where the data starts. |
| `indices` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:the indices of the triangle list. The indices are expressed as chars because they are unsigned 16-bit values. |
| `indicesOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index in the indices array where the index data starts. |
| --- | --- |
| `indexCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of indices in use. Typically a multiple of three. If not a multiple of three, the remaining one or two indices will be ignored. |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | 2 if all of the mesh is visible, 1 if some part of the mesh is visible, 0 if no part is visible. |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if ws is null, wsOffset \< 0, positions is null, positionsOffset \< 0, indices is null, indicesOffset \< 0, indicesOffset \> indices.length - indexCount |
