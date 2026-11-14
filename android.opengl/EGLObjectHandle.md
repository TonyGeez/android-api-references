# EGLObjectHandle

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EGLObjectHandle

Kotlin| [Java](https://developer.android.com/reference/android/opengl/EGLObjectHandle "View this page in Java") 

```
abstract class EGLObjectHandle
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.opengl.EGLObjectHandle](https://developer.android.com/reference/kotlin/android/opengl/EGLObjectHandle#) |

| Known Direct Subclasses [EGLConfig](https://developer.android.com/reference/kotlin/android/opengl/EGLConfig), [EGLContext](https://developer.android.com/reference/kotlin/android/opengl/EGLContext), [EGLDisplay](https://developer.android.com/reference/kotlin/android/opengl/EGLDisplay), [EGLImage](https://developer.android.com/reference/kotlin/android/opengl/EGLImage), [EGLSurface](https://developer.android.com/reference/kotlin/android/opengl/EGLSurface), [EGLSync](https://developer.android.com/reference/kotlin/android/opengl/EGLSync) |----------------------------------------------------------------------------------------|----------------------------------------------| | [EGLConfig](https://developer.android.com/reference/kotlin/android/opengl/EGLConfig) | Wrapper class for native EGLConfig objects. | | [EGLContext](https://developer.android.com/reference/kotlin/android/opengl/EGLContext) | Wrapper class for native EGLContext objects. | | [EGLDisplay](https://developer.android.com/reference/kotlin/android/opengl/EGLDisplay) | Wrapper class for native EGLDisplay objects. | | [EGLImage](https://developer.android.com/reference/kotlin/android/opengl/EGLImage) | Wrapper class for native EGLImage objects. | | [EGLSurface](https://developer.android.com/reference/kotlin/android/opengl/EGLSurface) | Wrapper class for native EGLSurface objects. | | [EGLSync](https://developer.android.com/reference/kotlin/android/opengl/EGLSync) | Wrapper class for native EGLSync objects. | |

Base class for wrapped EGL objects.

## Summary

| Protected constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [EGLObjectHandle](https://developer.android.com/reference/kotlin/android/opengl/EGLObjectHandle#EGLObjectHandle(kotlin.Int))`(`handle:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| [EGLObjectHandle](https://developer.android.com/reference/kotlin/android/opengl/EGLObjectHandle#EGLObjectHandle(kotlin.Long))`(`handle:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getHandle](https://developer.android.com/reference/kotlin/android/opengl/EGLObjectHandle#getHandle())`()` <br /> |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getNativeHandle](https://developer.android.com/reference/kotlin/android/opengl/EGLObjectHandle#getNativeHandle())`()` Returns the native handle of the wrapped EGL object. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/opengl/EGLObjectHandle#hashCode())`()` <br /> |

## Protected constructors

### EGLObjectHandle

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected EGLObjectHandle(handle: Int)
```

**Deprecated:** *Use [EGLObjectHandle(long)](https://developer.android.com/reference/kotlin/android/opengl/EGLObjectHandle#EGLObjectHandle(kotlin.Long))instead. Handles on 64 bit platforms will be wider than java ints.* 

### EGLObjectHandle

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected EGLObjectHandle(handle: Long)
```

## Public methods

### getHandle

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getHandle(): Int
```

**Deprecated:** *Use [getNativeHandle()](https://developer.android.com/reference/kotlin/android/opengl/EGLObjectHandle#getNativeHandle())instead. Handles on 64 bit platforms will be wider than java ints.* 

### getNativeHandle

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getNativeHandle(): Long
```

Returns the native handle of the wrapped EGL object. This handle can be cast to the corresponding native type on the native side. For example, EGLDisplay dpy = (EGLDisplay)handle;

| Return ||
|------------------------------------------------------------------------------|----------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the native handle of the wrapped EGL object. |

### hashCode

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |
