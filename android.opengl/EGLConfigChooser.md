# GLSurfaceView.EGLConfigChooser

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EGLConfigChooser

Kotlin| [Java](https://developer.android.com/reference/android/opengl/GLSurfaceView.EGLConfigChooser "View this page in Java") 

```
interface EGLConfigChooser
```

| [android.opengl.GLSurfaceView.EGLConfigChooser](https://developer.android.com/reference/kotlin/android/opengl/GLSurfaceView.EGLConfigChooser#) |

An interface for choosing an EGLConfig configuration from a list of potential configurations.

This interface must be implemented by clients wishing to call [GLSurfaceView.setEGLConfigChooser(EGLConfigChooser)](https://developer.android.com/reference/kotlin/android/opengl/GLSurfaceView#setEGLConfigChooser(android.opengl.GLSurfaceView.EGLConfigChooser))

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [EGLConfig](https://developer.android.com/reference/kotlin/javax/microedition/khronos/egl/EGLConfig.html#)! | [chooseConfig](https://developer.android.com/reference/kotlin/android/opengl/GLSurfaceView.EGLConfigChooser#chooseConfig(javax.microedition.khronos.egl.EGL10,%20javax.microedition.khronos.egl.EGLDisplay))`(`egl:` ` [EGL10](https://developer.android.com/reference/kotlin/javax/microedition/khronos/egl/EGL10.html#)!`, `display:` ` [EGLDisplay](https://developer.android.com/reference/kotlin/javax/microedition/khronos/egl/EGLDisplay.html#)!`)` Choose a configuration from the list. |

## Public methods

### chooseConfig

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun chooseConfig(
    egl: EGL10!, 
    display: EGLDisplay!
): EGLConfig!
```

Choose a configuration from the list. Implementors typically implement this method by calling [EGL10.eglChooseConfig](https://developer.android.com/reference/kotlin/javax/microedition/khronos/egl/EGL10.html#eglChooseConfig(javax.microedition.khronos.egl.EGLDisplay,%20kotlin.IntArray,%20kotlin.Array,%20kotlin.Int,%20kotlin.IntArray))and iterating through the results. Please consult the EGL specification available from The Khronos Group to learn how to call eglChooseConfig.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------|
| `egl` | [EGL10](https://developer.android.com/reference/kotlin/javax/microedition/khronos/egl/EGL10.html#)!:the EGL10 for the current display. |
| `display` | [EGLDisplay](https://developer.android.com/reference/kotlin/javax/microedition/khronos/egl/EGLDisplay.html#)!:the current display. |

| Return ||
|-------------------------------------------------------------------------------------------------------------|---------------------------|
| [EGLConfig](https://developer.android.com/reference/kotlin/javax/microedition/khronos/egl/EGLConfig.html#)! | the chosen configuration. |
