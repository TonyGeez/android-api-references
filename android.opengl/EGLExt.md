# EGLExt

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EGLExt

Kotlin| [Java](../android/opengl/EGLExt.md) 
| --- | --- |

```
open class EGLExt
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.opengl.EGLExt](../android/opengl/EGLExt.md) |

EGL Extensions

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EGL_CONTEXT_FLAGS_KHR](../android/opengl/EGLExt.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EGL_CONTEXT_MAJOR_VERSION_KHR](../android/opengl/EGLExt.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EGL_CONTEXT_MINOR_VERSION_KHR](../android/opengl/EGLExt.md) <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EGL_NO_NATIVE_FENCE_FD_ANDROID](../android/opengl/EGLExt.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EGL_OPENGL_ES3_BIT_KHR](../android/opengl/EGLExt.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EGL_RECORDABLE_ANDROID](../android/opengl/EGLExt.md) <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EGL_SYNC_NATIVE_FENCE_ANDROID](../android/opengl/EGLExt.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EGL_SYNC_NATIVE_FENCE_FD_ANDROID](../android/opengl/EGLExt.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EGL_SYNC_NATIVE_FENCE_SIGNALED_ANDROID](../android/opengl/EGLExt.md) <br /> |
| --- | --- |

| Public constructors ||
|----------------------------------------------------------------------------------------------------|---|
| [EGLExt](../android/opengl/EGLExt.md))`()` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [SyncFence](../android/hardware/SyncFence.md) | [eglDupNativeFenceFDANDROID](../android/opengl/EGLExt.md))`(`display:` ` [EGLDisplay](../android/opengl/EGLDisplay.md)`, `sync:` ` [EGLSync](../android/opengl/EGLSync.md)`)` Retrieves the SyncFence for an EGLSync created with EGL_SYNC_NATIVE_FENCE_ANDROID See [EGL_ANDROID_native_fence_sync](https://www.khronos.org/registry/EGL/extensions/ANDROID/EGL_ANDROID_native_fence_sync.txt) extension for more details |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [eglPresentationTimeANDROID](../android/opengl/EGLExt.md))`(`dpy:` ` [EGLDisplay](../android/opengl/EGLDisplay.md)!`, `sur:` ` [EGLSurface](../android/opengl/EGLSurface.md)!`, `time:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> |

## Constants

### EGL_CONTEXT_FLAGS_KHR

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EGL_CONTEXT_FLAGS_KHR: Int
```  

 Value: 12540

### EGL_CONTEXT_MAJOR_VERSION_KHR

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EGL_CONTEXT_MAJOR_VERSION_KHR: Int
```  

 Value: 12440

### EGL_CONTEXT_MINOR_VERSION_KHR

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EGL_CONTEXT_MINOR_VERSION_KHR: Int
```  

 Value: 12539

### EGL_NO_NATIVE_FENCE_FD_ANDROID

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EGL_NO_NATIVE_FENCE_FD_ANDROID: Int
```  

 Value: -1

### EGL_OPENGL_ES3_BIT_KHR

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EGL_OPENGL_ES3_BIT_KHR: Int
```  

 Value: 64

### EGL_RECORDABLE_ANDROID

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EGL_RECORDABLE_ANDROID: Int
```  

 Value: 12610

### EGL_SYNC_NATIVE_FENCE_ANDROID

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EGL_SYNC_NATIVE_FENCE_ANDROID: Int
```  

 Value: 12612

### EGL_SYNC_NATIVE_FENCE_FD_ANDROID

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EGL_SYNC_NATIVE_FENCE_FD_ANDROID: Int
```  

 Value: 12613

### EGL_SYNC_NATIVE_FENCE_SIGNALED_ANDROID

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EGL_SYNC_NATIVE_FENCE_SIGNALED_ANDROID: Int
```  

 Value: 12614

## Public constructors

### EGLExt

```
EGLExt()
```

## Public methods

### eglDupNativeFenceFDANDROID

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun eglDupNativeFenceFDANDROID(
    display: EGLDisplay, 
    sync: EGLSync
): SyncFence
```

Retrieves the SyncFence for an EGLSync created with EGL_SYNC_NATIVE_FENCE_ANDROID See [EGL_ANDROID_native_fence_sync](https://www.khronos.org/registry/EGL/extensions/ANDROID/EGL_ANDROID_native_fence_sync.txt) extension for more details

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `display` | [EGLDisplay](../android/opengl/EGLDisplay.md):The EGLDisplay connection This value cannot be`null`. |
| `sync` | [EGLSync](../android/opengl/EGLSync.md):The EGLSync to fetch the SyncFence from This value cannot be`null`. |

| Return ||
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [SyncFence](../android/hardware/SyncFence.md) | A SyncFence representing the native fence. \* If is not a valid sync object for , an [invalid](../android/hardware/SyncFence.md))SyncFence is returned and an EGL_BAD_PARAMETER error is generated. \* If the EGL_SYNC_NATIVE_FENCE_FD_ANDROID attribute of is EGL_NO_NATIVE_FENCE_FD_ANDROID, an [invalid](../android/hardware/SyncFence.md))SyncFence is returned and an EGL_BAD_PARAMETER error is generated. \* If does not match the display passed to eglCreateSync when was created, the behaviour is undefined. This value cannot be`null`. |

### eglPresentationTimeANDROID

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun eglPresentationTimeANDROID(
    dpy: EGLDisplay!, 
    sur: EGLSurface!, 
    time: Long
): Boolean
```
