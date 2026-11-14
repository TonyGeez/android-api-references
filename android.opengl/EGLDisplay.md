# EGLDisplay

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EGLDisplay

Kotlin| [Java](EGLDisplay.md) 
| --- | --- |

```
open class EGLDisplay : EGLObjectHandle
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.opengl.EGLObjectHandle](EGLObjectHandle.md) ||
| | ↳ | [android.opengl.EGLDisplay](EGLDisplay.md) |

Wrapper class for native EGLDisplay objects.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](EGLDisplay.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |

| Inherited functions ||
|---|---|
| From class [EGLObjectHandle](EGLObjectHandle.md) |------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getHandle](EGLObjectHandle.md))`()` <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getNativeHandle](EGLObjectHandle.md))`()` <br /> Returns the native handle of the wrapped EGL object. This handle can be cast to the corresponding native type on the native side. For example, EGLDisplay dpy = (EGLDisplay)handle; <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](EGLObjectHandle.md))`()` <br /> | ||

## Public methods

### equals

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |
