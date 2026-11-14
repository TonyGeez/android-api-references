# GLSurfaceView.EGLContextFactory

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EGLContextFactory

Kotlin| [Java](../android/opengl/GLSurfaceView.EGLContextFactory.md) 
| --- | --- |

```
interface EGLContextFactory
```

| [android.opengl.GLSurfaceView.EGLContextFactory](../android/opengl/GLSurfaceView.EGLContextFactory.md) |

An interface for customizing the eglCreateContext and eglDestroyContext calls.

This interface must be implemented by clients wishing to call [GLSurfaceView.setEGLContextFactory(EGLContextFactory)](../android/opengl/GLSurfaceView.md))

## Summary

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [EGLContext](../javax/microedition/khronos/egl/EGLContext.md)! | [createContext](../android/opengl/GLSurfaceView.EGLContextFactory.md))`(`egl:` ` [EGL10](../javax/microedition/khronos/egl/EGL10.md)!`, `display:` ` [EGLDisplay](../javax/microedition/khronos/egl/EGLDisplay.md)!`, `eglConfig:` ` [EGLConfig](../javax/microedition/khronos/egl/EGLConfig.md)!`)` <br /> |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [destroyContext](../android/opengl/GLSurfaceView.EGLContextFactory.md))`(`egl:` ` [EGL10](../javax/microedition/khronos/egl/EGL10.md)!`, `display:` ` [EGLDisplay](../javax/microedition/khronos/egl/EGLDisplay.md)!`, `context:` ` [EGLContext](../javax/microedition/khronos/egl/EGLContext.md)!`)` <br /> |

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
