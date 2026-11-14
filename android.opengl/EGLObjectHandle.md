# EGLObjectHandle

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EGLObjectHandle

Kotlin| [Java](EGLObjectHandle.md) 
| --- | --- |

```
abstract class EGLObjectHandle
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.opengl.EGLObjectHandle](EGLObjectHandle.md) |

| Known Direct Subclasses [EGLConfig](EGLConfig.md), [EGLContext](EGLContext.md), [EGLDisplay](EGLDisplay.md), [EGLImage](EGLImage.md), [EGLSurface](EGLSurface.md), [EGLSync](EGLSync.md) |----------------------------------------------------------------------------------------|----------------------------------------------| | [EGLConfig](EGLConfig.md) | Wrapper class for native EGLConfig objects. | | [EGLContext](EGLContext.md) | Wrapper class for native EGLContext objects. | | [EGLDisplay](EGLDisplay.md) | Wrapper class for native EGLDisplay objects. | | [EGLImage](EGLImage.md) | Wrapper class for native EGLImage objects. | | [EGLSurface](EGLSurface.md) | Wrapper class for native EGLSurface objects. | | [EGLSync](EGLSync.md) | Wrapper class for native EGLSync objects. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Base class for wrapped EGL objects.

## Summary

| Protected constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [EGLObjectHandle](EGLObjectHandle.md))`(`handle:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| [EGLObjectHandle](EGLObjectHandle.md))`(`handle:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getHandle](EGLObjectHandle.md))`()` <br /> |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getNativeHandle](EGLObjectHandle.md))`()` Returns the native handle of the wrapped EGL object. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](EGLObjectHandle.md))`()` <br /> |
| --- | --- |

## Protected constructors

### EGLObjectHandle

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected EGLObjectHandle(handle: Int)
```

**Deprecated:** *Use [EGLObjectHandle(long)](EGLObjectHandle.md))instead. Handles on 64 bit platforms will be wider than java ints.* 

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

**Deprecated:** *Use [getNativeHandle()](EGLObjectHandle.md))instead. Handles on 64 bit platforms will be wider than java ints.* 

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
