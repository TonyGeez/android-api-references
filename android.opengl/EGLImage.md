# EGLImage

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EGLImage

Kotlin| [Java](https://developer.android.com/reference/android/opengl/EGLImage "View this page in Java") 
| --- | --- |

```
open class EGLImage : EGLObjectHandle
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.opengl.EGLObjectHandle](https://developer.android.com/reference/kotlin/android/opengl/EGLObjectHandle) ||
| | ↳ | [android.opengl.EGLImage](https://developer.android.com/reference/kotlin/android/opengl/EGLImage#) |

Wrapper class for native EGLImage objects.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/opengl/EGLImage#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |

| Inherited functions ||
|---|---|
| From class [EGLObjectHandle](https://developer.android.com/reference/kotlin/android/opengl/EGLObjectHandle) |------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getHandle](https://developer.android.com/reference/kotlin/android/opengl/EGLObjectHandle#getHandle())`()` <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getNativeHandle](https://developer.android.com/reference/kotlin/android/opengl/EGLObjectHandle#getNativeHandle())`()` <br /> Returns the native handle of the wrapped EGL object. This handle can be cast to the corresponding native type on the native side. For example, EGLDisplay dpy = (EGLDisplay)handle; <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/opengl/EGLObjectHandle#hashCode())`()` <br /> | ||

## Public methods

### equals

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |
