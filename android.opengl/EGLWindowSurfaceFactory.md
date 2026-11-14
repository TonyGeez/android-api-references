# GLSurfaceView.EGLWindowSurfaceFactory

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EGLWindowSurfaceFactory

Kotlin| [Java](../android/opengl/GLSurfaceView.EGLWindowSurfaceFactory.md) 
| --- | --- |

```
interface EGLWindowSurfaceFactory
```

| [android.opengl.GLSurfaceView.EGLWindowSurfaceFactory](../android/opengl/GLSurfaceView.EGLWindowSurfaceFactory.md) |

An interface for customizing the eglCreateWindowSurface and eglDestroySurface calls.

This interface must be implemented by clients wishing to call [GLSurfaceView.setEGLWindowSurfaceFactory(EGLWindowSurfaceFactory)](../android/opengl/GLSurfaceView.md))

## Summary

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [EGLSurface](../javax/microedition/khronos/egl/EGLSurface.md)! | [createWindowSurface](../android/opengl/GLSurfaceView.EGLWindowSurfaceFactory.md))`(`egl:` ` [EGL10](../javax/microedition/khronos/egl/EGL10.md)!`, `display:` ` [EGLDisplay](../javax/microedition/khronos/egl/EGLDisplay.md)!`, `config:` ` [EGLConfig](../javax/microedition/khronos/egl/EGLConfig.md)!`, `nativeWindow:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [destroySurface](../android/opengl/GLSurfaceView.EGLWindowSurfaceFactory.md))`(`egl:` ` [EGL10](../javax/microedition/khronos/egl/EGL10.md)!`, `display:` ` [EGLDisplay](../javax/microedition/khronos/egl/EGLDisplay.md)!`, `surface:` ` [EGLSurface](../javax/microedition/khronos/egl/EGLSurface.md)!`)` <br /> |

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
| [EGLSurface](../javax/microedition/khronos/egl/EGLSurface.md)! | null if the surface cannot be constructed. |

### destroySurface

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun destroySurface(
    egl: EGL10!, 
    display: EGLDisplay!, 
    surface: EGLSurface!
): Unit
```
