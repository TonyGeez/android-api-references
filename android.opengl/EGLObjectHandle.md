# EGLObjectHandle

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EGLObjectHandle

Kotlin| [Java](../android/opengl/EGLObjectHandle.md) 
| --- | --- |

```
abstract class EGLObjectHandle
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.opengl.EGLObjectHandle](../android/opengl/EGLObjectHandle.md) |

| Known Direct Subclasses [EGLConfig](../android/opengl/EGLConfig.md), [EGLContext](../android/opengl/EGLContext.md), [EGLDisplay](../android/opengl/EGLDisplay.md), [EGLImage](../android/opengl/EGLImage.md), [EGLSurface](../android/opengl/EGLSurface.md), [EGLSync](../android/opengl/EGLSync.md) |----------------------------------------------------------------------------------------|----------------------------------------------| | [EGLConfig](../android/opengl/EGLConfig.md) | Wrapper class for native EGLConfig objects. | | [EGLContext](../android/opengl/EGLContext.md) | Wrapper class for native EGLContext objects. | | [EGLDisplay](../android/opengl/EGLDisplay.md) | Wrapper class for native EGLDisplay objects. | | [EGLImage](../android/opengl/EGLImage.md) | Wrapper class for native EGLImage objects. | | [EGLSurface](../android/opengl/EGLSurface.md) | Wrapper class for native EGLSurface objects. | | [EGLSync](../android/opengl/EGLSync.md) | Wrapper class for native EGLSync objects. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Base class for wrapped EGL objects.

## Summary

| Protected constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [EGLObjectHandle](../android/opengl/EGLObjectHandle.md))`(`handle:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| [EGLObjectHandle](../android/opengl/EGLObjectHandle.md))`(`handle:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getHandle](../android/opengl/EGLObjectHandle.md))`()` <br /> |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getNativeHandle](../android/opengl/EGLObjectHandle.md))`()` Returns the native handle of the wrapped EGL object. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/opengl/EGLObjectHandle.md))`()` <br /> |
| --- | --- |

## Protected constructors

### EGLObjectHandle

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected EGLObjectHandle(handle: Int)
```

**Deprecated:** *Use [EGLObjectHandle(long)](../android/opengl/EGLObjectHandle.md))instead. Handles on 64 bit platforms will be wider than java ints.* 

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

**Deprecated:** *Use [getNativeHandle()](../android/opengl/EGLObjectHandle.md))instead. Handles on 64 bit platforms will be wider than java ints.* 

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
