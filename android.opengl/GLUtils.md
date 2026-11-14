# GLUtils

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GLUtils

Kotlin| [Java](GLUtils.md) 
| --- | --- |

```
class GLUtils
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.opengl.GLUtils](GLUtils.md) |

Utility class to help bridging OpenGL ES and Android APIs.

## Summary

| Public methods ||
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getEGLErrorString](GLUtils.md))`(`error:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return a string for the EGL error code, or the hex representation if the error is unknown. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getInternalFormat](GLUtils.md))`(`bitmap:` ` [Bitmap](../android.graphics/Bitmap.md)!`)` return the internal format as defined by OpenGL ES of the supplied bitmap. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](GLUtils.md))`(`bitmap:` ` [Bitmap](../android.graphics/Bitmap.md)!`)` Return the type as defined by OpenGL ES of the supplied bitmap, if there is one. |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [texImage2D](GLUtils.md))`(`target:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `level:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bitmap:` ` [Bitmap](../android.graphics/Bitmap.md)!`, `border:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` A version of texImage2D that determines the internalFormat and type automatically. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [texImage2D](GLUtils.md))`(`target:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `level:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `internalformat:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bitmap:` ` [Bitmap](../android.graphics/Bitmap.md)!`, `border:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Calls glTexImage2D() on the current OpenGL context. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [texImage2D](GLUtils.md))`(`target:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `level:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `internalformat:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bitmap:` ` [Bitmap](../android.graphics/Bitmap.md)!`, `type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `border:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` A version of texImage2D() that takes an explicit type parameter as defined by the OpenGL ES specification. |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [texSubImage2D](GLUtils.md))`(`target:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `level:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `xoffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `yoffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bitmap:` ` [Bitmap](../android.graphics/Bitmap.md)!`)` Calls glTexSubImage2D() on the current OpenGL context. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [texSubImage2D](GLUtils.md))`(`target:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `level:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `xoffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `yoffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bitmap:` ` [Bitmap](../android.graphics/Bitmap.md)!`, `format:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` A version of texSubImage2D() that takes an explicit type parameter as defined by the OpenGL ES specification. |

## Public methods

### getEGLErrorString

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getEGLErrorString(error: Int): String!
```

Return a string for the EGL error code, or the hex representation if the error is unknown.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------|
| `error` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The EGL error to convert into a String. |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | An error string corresponding to the EGL error code. |

### getInternalFormat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInternalFormat(bitmap: Bitmap!): Int
```

return the internal format as defined by OpenGL ES of the supplied bitmap.

| Parameters ||
|----------|------------------------------------------------------------------------------------------|
| `bitmap` | [Bitmap](../android.graphics/Bitmap.md)!: |

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the internal format of the bitmap. |

### getType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getType(bitmap: Bitmap!): Int
```

Return the type as defined by OpenGL ES of the supplied bitmap, if there is one. If the bitmap is stored in a compressed format, it may not have a valid OpenGL ES type.

| Parameters ||
|----------|------------------------------------------------------------------------------------------|
| `bitmap` | [Bitmap](../android.graphics/Bitmap.md)!: |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the OpenGL ES type of the bitmap. |

| Exceptions ||
|--------------------------------------|-------------------------------------|
| `java.lang.IllegalArgumentException` | if the bitmap does not have a type. |

### texImage2D

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun texImage2D(
    target: Int, 
    level: Int, 
    bitmap: Bitmap!, 
    border: Int
): Unit
```

A version of texImage2D that determines the internalFormat and type automatically.

| Parameters ||
|----------|------------------------------------------------------------------------------------------|
| `target` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): |
| `level` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): |
| `bitmap` | [Bitmap](../android.graphics/Bitmap.md)!: |
| --- | --- |
| `border` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): |

### texImage2D

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun texImage2D(
    target: Int, 
    level: Int, 
    internalformat: Int, 
    bitmap: Bitmap!, 
    border: Int
): Unit
```

Calls glTexImage2D() on the current OpenGL context. If no context is current the behavior is the same as calling glTexImage2D() with no current context, that is, eglGetError() will return the appropriate error. Unlike glTexImage2D() bitmap cannot be null and will raise an exception in that case. All other parameters are identical to those used for glTexImage2D(). NOTE: this method doesn't change GL_UNPACK_ALIGNMENT, you must make sure to set it properly according to the supplied bitmap. Whether or not bitmap can have non power of two dimensions depends on the current OpenGL context. Always check glGetError() some time after calling this method, just like when using OpenGL directly.

| Parameters ||
|------------------|------------------------------------------------------------------------------------------|
| `target` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): |
| `level` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): |
| `internalformat` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): |
| --- | --- |
| `bitmap` | [Bitmap](../android.graphics/Bitmap.md)!: |
| `border` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): |

### texImage2D

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun texImage2D(
    target: Int, 
    level: Int, 
    internalformat: Int, 
    bitmap: Bitmap!, 
    type: Int, 
    border: Int
): Unit
```

A version of texImage2D() that takes an explicit type parameter as defined by the OpenGL ES specification. The actual type and internalformat of the bitmap must be compatible with the specified type and internalformat parameters.

| Parameters ||
|------------------|------------------------------------------------------------------------------------------|
| `target` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): |
| `level` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): |
| `internalformat` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): |
| --- | --- |
| `bitmap` | [Bitmap](../android.graphics/Bitmap.md)!: |
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): |
| `border` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): |
| --- | --- |

### texSubImage2D

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun texSubImage2D(
    target: Int, 
    level: Int, 
    xoffset: Int, 
    yoffset: Int, 
    bitmap: Bitmap!
): Unit
```

Calls glTexSubImage2D() on the current OpenGL context. If no context is current the behavior is the same as calling glTexSubImage2D() with no current context, that is, eglGetError() will return the appropriate error. Unlike glTexSubImage2D() bitmap cannot be null and will raise an exception in that case. All other parameters are identical to those used for glTexSubImage2D(). NOTE: this method doesn't change GL_UNPACK_ALIGNMENT, you must make sure to set it properly according to the supplied bitmap. Whether or not bitmap can have non power of two dimensions depends on the current OpenGL context. Always check glGetError() some time after calling this method, just like when using OpenGL directly.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------|
| `target` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): |
| `level` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): |
| `xoffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): |
| --- | --- |
| `yoffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): |
| `bitmap` | [Bitmap](../android.graphics/Bitmap.md)!: |

### texSubImage2D

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun texSubImage2D(
    target: Int, 
    level: Int, 
    xoffset: Int, 
    yoffset: Int, 
    bitmap: Bitmap!, 
    format: Int, 
    type: Int
): Unit
```

A version of texSubImage2D() that takes an explicit type parameter as defined by the OpenGL ES specification.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------|
| `target` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): |
| `level` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): |
| `xoffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): |
| --- | --- |
| `yoffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): |
| `bitmap` | [Bitmap](../android.graphics/Bitmap.md)!: |
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): |
| --- | --- |
