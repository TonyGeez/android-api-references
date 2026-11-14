# GLU

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GLU

Kotlin| [Java](https://developer.android.com/reference/android/opengl/GLU "View this page in Java") 
| --- | --- |

```
open class GLU
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.opengl.GLU](https://developer.android.com/reference/kotlin/android/opengl/GLU#) |

A set of GL utilities inspired by the OpenGL Utility Toolkit.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------|---|
| [GLU](https://developer.android.com/reference/kotlin/android/opengl/GLU#GLU())`()` <br /> |

| Public methods ||
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [gluErrorString](https://developer.android.com/reference/kotlin/android/opengl/GLU#gluErrorString(kotlin.Int))`(`error:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return an error string from a GL or GLU error code. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [gluLookAt](https://developer.android.com/reference/kotlin/android/opengl/GLU#gluLookAt(javax.microedition.khronos.opengles.GL10,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float))`(`gl:` ` [GL10](https://developer.android.com/reference/kotlin/javax/microedition/khronos/opengles/GL10.html#)!`, `eyeX:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `eyeY:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `eyeZ:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `centerX:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `centerY:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `centerZ:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `upX:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `upY:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `upZ:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Define a viewing transformation in terms of an eye point, a center of view, and an up vector. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [gluOrtho2D](https://developer.android.com/reference/kotlin/android/opengl/GLU#gluOrtho2D(javax.microedition.khronos.opengles.GL10,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float))`(`gl:` ` [GL10](https://developer.android.com/reference/kotlin/javax/microedition/khronos/opengles/GL10.html#)!`, `left:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `right:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `bottom:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `top:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Set up a 2D orthographic projection matrix |
| --- | --- |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [gluPerspective](https://developer.android.com/reference/kotlin/android/opengl/GLU#gluPerspective(javax.microedition.khronos.opengles.GL10,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float))`(`gl:` ` [GL10](https://developer.android.com/reference/kotlin/javax/microedition/khronos/opengles/GL10.html#)!`, `fovy:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `aspect:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `zNear:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `zFar:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Set up a perspective projection matrix |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [gluProject](https://developer.android.com/reference/kotlin/android/opengl/GLU#gluProject(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.FloatArray,%20kotlin.Int,%20kotlin.FloatArray,%20kotlin.Int,%20kotlin.IntArray,%20kotlin.Int,%20kotlin.FloatArray,%20kotlin.Int))`(`objX:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `objY:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `objZ:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `model:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `modelOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `project:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `projectOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `view:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`, `viewOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `win:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `winOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Map object coordinates into window coordinates. |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [gluUnProject](https://developer.android.com/reference/kotlin/android/opengl/GLU#gluUnProject(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.FloatArray,%20kotlin.Int,%20kotlin.FloatArray,%20kotlin.Int,%20kotlin.IntArray,%20kotlin.Int,%20kotlin.FloatArray,%20kotlin.Int))`(`winX:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `winY:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `winZ:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `model:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `modelOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `project:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `projectOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `view:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`, `viewOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `obj:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `objOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Map window coordinates to object coordinates. |
| --- | --- |

## Public constructors

### GLU

```
GLU()
```

## Public methods

### gluErrorString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun gluErrorString(error: Int): String!
```

Return an error string from a GL or GLU error code.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------|
| `error` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):- a GL or GLU error code. |

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the error string for the input error code, or NULL if the input was not a valid GL or GLU error code. |

### gluLookAt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun gluLookAt(
    gl: GL10!, 
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

Define a viewing transformation in terms of an eye point, a center of view, and an up vector.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------|
| `gl` | [GL10](https://developer.android.com/reference/kotlin/javax/microedition/khronos/opengles/GL10.html#)!:a GL10 interface |
| `eyeX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):eye point X |
| `eyeY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):eye point Y |
| --- | --- |
| `eyeZ` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):eye point Z |
| `centerX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):center of view X |
| `centerY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):center of view Y |
| --- | --- |
| `centerZ` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):center of view Z |
| `upX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):up vector X |
| `upY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):up vector Y |
| --- | --- |
| `upZ` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):up vector Z |

### gluOrtho2D

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun gluOrtho2D(
    gl: GL10!, 
    left: Float, 
    right: Float, 
    bottom: Float, 
    top: Float
): Unit
```

Set up a 2D orthographic projection matrix

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------|
| `gl` | [GL10](https://developer.android.com/reference/kotlin/javax/microedition/khronos/opengles/GL10.html#)!: |
| `left` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): |
| `right` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): |
| --- | --- |
| `bottom` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): |
| `top` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): |

### gluPerspective

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun gluPerspective(
    gl: GL10!, 
    fovy: Float, 
    aspect: Float, 
    zNear: Float, 
    zFar: Float
): Unit
```

Set up a perspective projection matrix

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `gl` | [GL10](https://developer.android.com/reference/kotlin/javax/microedition/khronos/opengles/GL10.html#)!:a GL10 interface |
| `fovy` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):specifies the field of view angle, in degrees, in the Y direction. |
| `aspect` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):specifies the aspect ration that determins the field of view in the x direction. The aspect ratio is the ratio of x (width) to y (height). |
| --- | --- |
| `zNear` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):specifies the distance from the viewer to the near clipping plane (always positive). |
| `zFar` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):specifies the distance from the viewer to the far clipping plane (always positive). |

### gluProject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun gluProject(
    objX: Float, 
    objY: Float, 
    objZ: Float, 
    model: FloatArray!, 
    modelOffset: Int, 
    project: FloatArray!, 
    projectOffset: Int, 
    view: IntArray!, 
    viewOffset: Int, 
    win: FloatArray!, 
    winOffset: Int
): Int
```

Map object coordinates into window coordinates. gluProject transforms the specified object coordinates into window coordinates using model, proj, and view. The result is stored in win.

Note that you can use the OES_matrix_get extension, if present, to get the current modelView and projection matrices.

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `objX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):object coordinates X |
| `objY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):object coordinates Y |
| `objZ` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):object coordinates Z |
| --- | --- |
| `model` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:the current modelview matrix |
| `modelOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the offset into the model array where the modelview maxtrix data starts. |
| `project` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:the current projection matrix |
| --- | --- |
| `projectOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the offset into the project array where the project matrix data starts. |
| `view` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!:the current view, {x, y, width, height} |
| `viewOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the offset into the view array where the view vector data starts. |
| --- | --- |
| `win` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:the output vector {winX, winY, winZ}, that returns the computed window coordinates. |
| `winOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the offset into the win array where the win vector data starts. |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | A return value of GL_TRUE indicates success, a return value of GL_FALSE indicates failure. |

### gluUnProject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun gluUnProject(
    winX: Float, 
    winY: Float, 
    winZ: Float, 
    model: FloatArray!, 
    modelOffset: Int, 
    project: FloatArray!, 
    projectOffset: Int, 
    view: IntArray!, 
    viewOffset: Int, 
    obj: FloatArray!, 
    objOffset: Int
): Int
```

Map window coordinates to object coordinates. gluUnProject maps the specified window coordinates into object coordinates using model, proj, and view. The result is stored in obj.

Note that you can use the OES_matrix_get extension, if present, to get the current modelView and projection matrices.

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `winX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):window coordinates X |
| `winY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):window coordinates Y |
| `winZ` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):window coordinates Z |
| --- | --- |
| `model` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:the current modelview matrix |
| `modelOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the offset into the model array where the modelview maxtrix data starts. |
| `project` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:the current projection matrix |
| --- | --- |
| `projectOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the offset into the project array where the project matrix data starts. |
| `view` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!:the current view, {x, y, width, height} |
| `viewOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the offset into the view array where the view vector data starts. |
| --- | --- |
| `obj` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:the output vector {objX, objY, objZ, objW}, that returns the computed homogeneous object coordinates. |
| `objOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the offset into the obj array where the obj vector data starts. |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | A return value of GL10.GL_TRUE indicates success, a return value of GL10.GL_FALSE indicates failure. |
