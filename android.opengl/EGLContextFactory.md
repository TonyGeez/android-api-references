# GLSurfaceView.EGLContextFactory

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EGLContextFactory

Kotlin| [Java](https://developer.android.com/reference/android/opengl/GLSurfaceView.EGLContextFactory "View this page in Java") 
| --- | --- |

```
interface EGLContextFactory
```

| [android.opengl.GLSurfaceView.EGLContextFactory](https://developer.android.com/reference/kotlin/android/opengl/GLSurfaceView.EGLContextFactory#) |

An interface for customizing the eglCreateContext and eglDestroyContext calls.

This interface must be implemented by clients wishing to call [GLSurfaceView.setEGLContextFactory(EGLContextFactory)](https://developer.android.com/reference/kotlin/android/opengl/GLSurfaceView#setEGLContextFactory(android.opengl.GLSurfaceView.EGLContextFactory))

## Summary

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [EGLContext](https://developer.android.com/reference/kotlin/javax/microedition/khronos/egl/EGLContext.html#)! | [createContext](https://developer.android.com/reference/kotlin/android/opengl/GLSurfaceView.EGLContextFactory#createContext(javax.microedition.khronos.egl.EGL10,%20javax.microedition.khronos.egl.EGLDisplay,%20javax.microedition.khronos.egl.EGLConfig))`(`egl:` ` [EGL10](https://developer.android.com/reference/kotlin/javax/microedition/khronos/egl/EGL10.html#)!`, `display:` ` [EGLDisplay](https://developer.android.com/reference/kotlin/javax/microedition/khronos/egl/EGLDisplay.html#)!`, `eglConfig:` ` [EGLConfig](https://developer.android.com/reference/kotlin/javax/microedition/khronos/egl/EGLConfig.html#)!`)` <br /> |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [destroyContext](https://developer.android.com/reference/kotlin/android/opengl/GLSurfaceView.EGLContextFactory#destroyContext(javax.microedition.khronos.egl.EGL10,%20javax.microedition.khronos.egl.EGLDisplay,%20javax.microedition.khronos.egl.EGLContext))`(`egl:` ` [EGL10](https://developer.android.com/reference/kotlin/javax/microedition/khronos/egl/EGL10.html#)!`, `display:` ` [EGLDisplay](https://developer.android.com/reference/kotlin/javax/microedition/khronos/egl/EGLDisplay.html#)!`, `context:` ` [EGLContext](https://developer.android.com/reference/kotlin/javax/microedition/khronos/egl/EGLContext.html#)!`)` <br /> |

## Public methods

### createContext

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun createContext(
    egl: EGL10!, 
    display: EGLDisplay!, 
    eglConfig: EGLConfig!
): EGLContext!
```  

### destroyContext

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun destroyContext(
    egl: EGL10!, 
    display: EGLDisplay!, 
    context: EGLContext!
): Unit
```
