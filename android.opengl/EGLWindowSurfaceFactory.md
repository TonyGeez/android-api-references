# GLSurfaceView.EGLWindowSurfaceFactory

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EGLWindowSurfaceFactory

Kotlin| [Java](https://developer.android.com/reference/android/opengl/GLSurfaceView.EGLWindowSurfaceFactory "View this page in Java") 

```
interface EGLWindowSurfaceFactory
```

| [android.opengl.GLSurfaceView.EGLWindowSurfaceFactory](https://developer.android.com/reference/kotlin/android/opengl/GLSurfaceView.EGLWindowSurfaceFactory#) |

An interface for customizing the eglCreateWindowSurface and eglDestroySurface calls.

This interface must be implemented by clients wishing to call [GLSurfaceView.setEGLWindowSurfaceFactory(EGLWindowSurfaceFactory)](https://developer.android.com/reference/kotlin/android/opengl/GLSurfaceView#setEGLWindowSurfaceFactory(android.opengl.GLSurfaceView.EGLWindowSurfaceFactory))

## Summary

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [EGLSurface](https://developer.android.com/reference/kotlin/javax/microedition/khronos/egl/EGLSurface.html#)! | [createWindowSurface](https://developer.android.com/reference/kotlin/android/opengl/GLSurfaceView.EGLWindowSurfaceFactory#createWindowSurface(javax.microedition.khronos.egl.EGL10,%20javax.microedition.khronos.egl.EGLDisplay,%20javax.microedition.khronos.egl.EGLConfig,%20kotlin.Any))`(`egl:` ` [EGL10](https://developer.android.com/reference/kotlin/javax/microedition/khronos/egl/EGL10.html#)!`, `display:` ` [EGLDisplay](https://developer.android.com/reference/kotlin/javax/microedition/khronos/egl/EGLDisplay.html#)!`, `config:` ` [EGLConfig](https://developer.android.com/reference/kotlin/javax/microedition/khronos/egl/EGLConfig.html#)!`, `nativeWindow:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [destroySurface](https://developer.android.com/reference/kotlin/android/opengl/GLSurfaceView.EGLWindowSurfaceFactory#destroySurface(javax.microedition.khronos.egl.EGL10,%20javax.microedition.khronos.egl.EGLDisplay,%20javax.microedition.khronos.egl.EGLSurface))`(`egl:` ` [EGL10](https://developer.android.com/reference/kotlin/javax/microedition/khronos/egl/EGL10.html#)!`, `display:` ` [EGLDisplay](https://developer.android.com/reference/kotlin/javax/microedition/khronos/egl/EGLDisplay.html#)!`, `surface:` ` [EGLSurface](https://developer.android.com/reference/kotlin/javax/microedition/khronos/egl/EGLSurface.html#)!`)` <br /> |

## Public methods

### createWindowSurface

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun createWindowSurface(
    egl: EGL10!, 
    display: EGLDisplay!, 
    config: EGLConfig!, 
    nativeWindow: Any!
): EGLSurface!
```

| Return ||
|---------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| [EGLSurface](https://developer.android.com/reference/kotlin/javax/microedition/khronos/egl/EGLSurface.html#)! | null if the surface cannot be constructed. |

### destroySurface

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun destroySurface(
    egl: EGL10!, 
    display: EGLDisplay!, 
    surface: EGLSurface!
): Unit
```
