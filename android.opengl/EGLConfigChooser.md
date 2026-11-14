# GLSurfaceView.EGLConfigChooser

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EGLConfigChooser

Kotlin| [Java](../android/opengl/GLSurfaceView.EGLConfigChooser.md) 
| --- | --- |

```
interface EGLConfigChooser
```

| [android.opengl.GLSurfaceView.EGLConfigChooser](../android/opengl/GLSurfaceView.EGLConfigChooser.md) |

An interface for choosing an EGLConfig configuration from a list of potential configurations.

This interface must be implemented by clients wishing to call [GLSurfaceView.setEGLConfigChooser(EGLConfigChooser)](GLSurfaceView.md))

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [EGLConfig](../javax.microedition.khronos.egl/EGLConfig.md)! | [chooseConfig](../android/opengl/GLSurfaceView.EGLConfigChooser.md))`(`egl:` ` [EGL10](../javax.microedition.khronos.egl/EGL10.md)!`, `display:` ` [EGLDisplay](../javax.microedition.khronos.egl/EGLDisplay.md)!`)` Choose a configuration from the list. |

## Public methods

### chooseConfig

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun chooseConfig(
    egl: EGL10!, 
    display: EGLDisplay!
): EGLConfig!
```

Choose a configuration from the list. Implementors typically implement this method by calling [EGL10.eglChooseConfig](../javax.microedition.khronos.egl/EGL10.md))and iterating through the results. Please consult the EGL specification available from The Khronos Group to learn how to call eglChooseConfig.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------|
| `egl` | [EGL10](../javax.microedition.khronos.egl/EGL10.md)!:the EGL10 for the current display. |
| `display` | [EGLDisplay](../javax.microedition.khronos.egl/EGLDisplay.md)!:the current display. |

| Return ||
|-------------------------------------------------------------------------------------------------------------|---------------------------|
| [EGLConfig](../javax.microedition.khronos.egl/EGLConfig.md)! | the chosen configuration. |
