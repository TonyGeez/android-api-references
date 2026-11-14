# EGLContext

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EGLContext

```
abstract class EGLContext
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.microedition.khronos.egl.EGLContext](https://developer.android.com/reference/kotlin/javax/microedition/khronos/egl/EGLContext#) |

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------|---|
| [EGLContext](https://developer.android.com/reference/kotlin/javax/microedition/khronos/egl/EGLContext#EGLContext())`()` <br /> |

| Public methods ||
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| openstatic [EGL](https://developer.android.com/reference/kotlin/javax/microedition/khronos/egl/EGL)! | [getEGL](https://developer.android.com/reference/kotlin/javax/microedition/khronos/egl/EGLContext#getEGL())`()` <br /> |
| abstract [GL](https://developer.android.com/reference/kotlin/javax/microedition/khronos/opengles/GL.html#)! | [getGL](https://developer.android.com/reference/kotlin/javax/microedition/khronos/egl/EGLContext#getGL())`()` <br /> |

## Public constructors

### EGLContext

```
EGLContext()
```

## Public methods

### getEGL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getEGL(): EGL!
```  

### getGL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getGL(): GL!
```
