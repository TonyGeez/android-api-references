# GLDebugHelper

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GLDebugHelper

Kotlin| [Java](https://developer.android.com/reference/android/opengl/GLDebugHelper "View this page in Java") 

```
open class GLDebugHelper
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.opengl.GLDebugHelper](https://developer.android.com/reference/kotlin/android/opengl/GLDebugHelper#) |

A helper class for debugging OpenGL ES applications. Wraps the supplied GL interface with a new GL interface that adds support for error checking and logging.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONFIG_CHECK_GL_ERROR](https://developer.android.com/reference/kotlin/android/opengl/GLDebugHelper#CONFIG_CHECK_GL_ERROR:kotlin.Int) Check glError() after every call. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONFIG_CHECK_THREAD](https://developer.android.com/reference/kotlin/android/opengl/GLDebugHelper#CONFIG_CHECK_THREAD:kotlin.Int) Check if all calls are on the same thread. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONFIG_LOG_ARGUMENT_NAMES](https://developer.android.com/reference/kotlin/android/opengl/GLDebugHelper#CONFIG_LOG_ARGUMENT_NAMES:kotlin.Int) Print argument names when logging GL Calls. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_WRONG_THREAD](https://developer.android.com/reference/kotlin/android/opengl/GLDebugHelper#ERROR_WRONG_THREAD:kotlin.Int) The Error number used in the GLException that is thrown if CONFIG_CHECK_THREAD is enabled and you call OpenGL ES on the a different thread. |

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------|---|
| [GLDebugHelper](https://developer.android.com/reference/kotlin/android/opengl/GLDebugHelper#GLDebugHelper())`()` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [EGL](https://developer.android.com/reference/kotlin/javax/microedition/khronos/egl/EGL.html#)! | [wrap](https://developer.android.com/reference/kotlin/android/opengl/GLDebugHelper#wrap(javax.microedition.khronos.egl.EGL,%20kotlin.Int,%20java.io.Writer))`(`egl:` ` [EGL](https://developer.android.com/reference/kotlin/javax/microedition/khronos/egl/EGL.html#)!`, `configFlags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `log:` ` [Writer](https://developer.android.com/reference/kotlin/java/io/Writer.html#)!`)` Wrap an existing EGL interface in a new EGL interface that adds support for error checking and/or logging. |
| openstatic [GL](https://developer.android.com/reference/kotlin/javax/microedition/khronos/opengles/GL.html#)! | [wrap](https://developer.android.com/reference/kotlin/android/opengl/GLDebugHelper#wrap(javax.microedition.khronos.opengles.GL,%20kotlin.Int,%20java.io.Writer))`(`gl:` ` [GL](https://developer.android.com/reference/kotlin/javax/microedition/khronos/opengles/GL.html#)!`, `configFlags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `log:` ` [Writer](https://developer.android.com/reference/kotlin/java/io/Writer.html#)!`)` <br /> |

## Constants

### CONFIG_CHECK_GL_ERROR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONFIG_CHECK_GL_ERROR: Int
```

Check glError() after every call. 

 Value: 1

### CONFIG_CHECK_THREAD

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONFIG_CHECK_THREAD: Int
```

Check if all calls are on the same thread. 

 Value: 2

### CONFIG_LOG_ARGUMENT_NAMES

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONFIG_LOG_ARGUMENT_NAMES: Int
```

Print argument names when logging GL Calls. 

 Value: 4

### ERROR_WRONG_THREAD

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_WRONG_THREAD: Int
```

The Error number used in the GLException that is thrown if CONFIG_CHECK_THREAD is enabled and you call OpenGL ES on the a different thread. 

 Value: 28672

## Public constructors

### GLDebugHelper

```
GLDebugHelper()
```

## Public methods

### wrap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun wrap(
    egl: EGL!, 
    configFlags: Int, 
    log: Writer!
): EGL!
```

Wrap an existing EGL interface in a new EGL interface that adds support for error checking and/or logging.

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `egl` | [EGL](https://developer.android.com/reference/kotlin/javax/microedition/khronos/egl/EGL.html#)!:the existing GL interface. Must implement EGL and EGL10. May optionally implement EGL11 as well. |
| `configFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A bitmask of error checking flags. |
| `log` | [Writer](https://developer.android.com/reference/kotlin/java/io/Writer.html#)!:- null to disable logging, non-null to enable logging. |

| Return ||
|-------------------------------------------------------------------------------------------------|----------------------------|
| [EGL](https://developer.android.com/reference/kotlin/javax/microedition/khronos/egl/EGL.html#)! | the wrapped EGL interface. |

### wrap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun wrap(
    gl: GL!, 
    configFlags: Int, 
    log: Writer!
): GL!
```
