# EGLContext

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EGLContext

```
abstract class EGLContext
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.microedition.khronos.egl.EGLContext](EGLContext.md) |

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------|---|
| [EGLContext](EGLContext.md))`()` <br /> |

| Public methods ||
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| openstatic [EGL](EGL.md)! | [getEGL](EGLContext.md))`()` <br /> |
| abstract [GL](../javax.microedition.khronos.opengles/GL.md)! | [getGL](EGLContext.md))`()` <br /> |

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
