# GLDebugHelper

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GLDebugHelper

Kotlin| [Java](GLDebugHelper.md) 
| --- | --- |

```
open class GLDebugHelper
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.opengl.GLDebugHelper](GLDebugHelper.md) |

A helper class for debugging OpenGL ES applications. Wraps the supplied GL interface with a new GL interface that adds support for error checking and logging.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONFIG_CHECK_GL_ERROR](GLDebugHelper.md) Check glError() after every call. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONFIG_CHECK_THREAD](GLDebugHelper.md) Check if all calls are on the same thread. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONFIG_LOG_ARGUMENT_NAMES](GLDebugHelper.md) Print argument names when logging GL Calls. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_WRONG_THREAD](GLDebugHelper.md) The Error number used in the GLException that is thrown if CONFIG_CHECK_THREAD is enabled and you call OpenGL ES on the a different thread. |

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------|---|
| [GLDebugHelper](GLDebugHelper.md))`()` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [EGL](../javax.microedition.khronos.egl/EGL.md)! | [wrap](GLDebugHelper.md))`(`egl:` ` [EGL](../javax.microedition.khronos.egl/EGL.md)!`, `configFlags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `log:` ` [Writer](../java.io/Writer.md)!`)` Wrap an existing EGL interface in a new EGL interface that adds support for error checking and/or logging. |
| openstatic [GL](../javax.microedition.khronos.opengles/GL.md)! | [wrap](GLDebugHelper.md))`(`gl:` ` [GL](../javax.microedition.khronos.opengles/GL.md)!`, `configFlags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `log:` ` [Writer](../java.io/Writer.md)!`)` <br /> |

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
| `egl` | [EGL](../javax.microedition.khronos.egl/EGL.md)!:the existing GL interface. Must implement EGL and EGL10. May optionally implement EGL11 as well. |
| `configFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A bitmask of error checking flags. |
| `log` | [Writer](../java.io/Writer.md)!:- null to disable logging, non-null to enable logging. |
| --- | --- |

| Return ||
|-------------------------------------------------------------------------------------------------|----------------------------|
| [EGL](../javax.microedition.khronos.egl/EGL.md)! | the wrapped EGL interface. |

### wrap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun wrap(
    gl: GL!, 
    configFlags: Int, 
    log: Writer!
): GL!
```
