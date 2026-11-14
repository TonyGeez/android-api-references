# EGLExt

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EGLExt

Kotlin| [Java](https://developer.android.com/reference/android/opengl/EGLExt "View this page in Java") 
| --- | --- |

```
open class EGLExt
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.opengl.EGLExt](https://developer.android.com/reference/kotlin/android/opengl/EGLExt#) |

EGL Extensions

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EGL_CONTEXT_FLAGS_KHR](https://developer.android.com/reference/kotlin/android/opengl/EGLExt#EGL_CONTEXT_FLAGS_KHR:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EGL_CONTEXT_MAJOR_VERSION_KHR](https://developer.android.com/reference/kotlin/android/opengl/EGLExt#EGL_CONTEXT_MAJOR_VERSION_KHR:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EGL_CONTEXT_MINOR_VERSION_KHR](https://developer.android.com/reference/kotlin/android/opengl/EGLExt#EGL_CONTEXT_MINOR_VERSION_KHR:kotlin.Int) <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EGL_NO_NATIVE_FENCE_FD_ANDROID](https://developer.android.com/reference/kotlin/android/opengl/EGLExt#EGL_NO_NATIVE_FENCE_FD_ANDROID:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EGL_OPENGL_ES3_BIT_KHR](https://developer.android.com/reference/kotlin/android/opengl/EGLExt#EGL_OPENGL_ES3_BIT_KHR:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EGL_RECORDABLE_ANDROID](https://developer.android.com/reference/kotlin/android/opengl/EGLExt#EGL_RECORDABLE_ANDROID:kotlin.Int) <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EGL_SYNC_NATIVE_FENCE_ANDROID](https://developer.android.com/reference/kotlin/android/opengl/EGLExt#EGL_SYNC_NATIVE_FENCE_ANDROID:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EGL_SYNC_NATIVE_FENCE_FD_ANDROID](https://developer.android.com/reference/kotlin/android/opengl/EGLExt#EGL_SYNC_NATIVE_FENCE_FD_ANDROID:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EGL_SYNC_NATIVE_FENCE_SIGNALED_ANDROID](https://developer.android.com/reference/kotlin/android/opengl/EGLExt#EGL_SYNC_NATIVE_FENCE_SIGNALED_ANDROID:kotlin.Int) <br /> |
| --- | --- |

| Public constructors ||
|----------------------------------------------------------------------------------------------------|---|
| [EGLExt](https://developer.android.com/reference/kotlin/android/opengl/EGLExt#EGLExt())`()` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [SyncFence](https://developer.android.com/reference/kotlin/android/hardware/SyncFence.html#) | [eglDupNativeFenceFDANDROID](https://developer.android.com/reference/kotlin/android/opengl/EGLExt#eglDupNativeFenceFDANDROID(android.opengl.EGLDisplay,%20android.opengl.EGLSync))`(`display:` ` [EGLDisplay](https://developer.android.com/reference/kotlin/android/opengl/EGLDisplay)`, `sync:` ` [EGLSync](https://developer.android.com/reference/kotlin/android/opengl/EGLSync)`)` Retrieves the SyncFence for an EGLSync created with EGL_SYNC_NATIVE_FENCE_ANDROID See [EGL_ANDROID_native_fence_sync](https://www.khronos.org/registry/EGL/extensions/ANDROID/EGL_ANDROID_native_fence_sync.txt) extension for more details |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [eglPresentationTimeANDROID](https://developer.android.com/reference/kotlin/android/opengl/EGLExt#eglPresentationTimeANDROID(android.opengl.EGLDisplay,%20android.opengl.EGLSurface,%20kotlin.Long))`(`dpy:` ` [EGLDisplay](https://developer.android.com/reference/kotlin/android/opengl/EGLDisplay)!`, `sur:` ` [EGLSurface](https://developer.android.com/reference/kotlin/android/opengl/EGLSurface)!`, `time:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> |

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
| `display` | [EGLDisplay](https://developer.android.com/reference/kotlin/android/opengl/EGLDisplay):The EGLDisplay connection This value cannot be`null`. |
| `sync` | [EGLSync](https://developer.android.com/reference/kotlin/android/opengl/EGLSync):The EGLSync to fetch the SyncFence from This value cannot be`null`. |

| Return ||
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [SyncFence](https://developer.android.com/reference/kotlin/android/hardware/SyncFence.html#) | A SyncFence representing the native fence. \* If is not a valid sync object for , an [invalid](https://developer.android.com/reference/kotlin/android/hardware/SyncFence.html#isValid())SyncFence is returned and an EGL_BAD_PARAMETER error is generated. \* If the EGL_SYNC_NATIVE_FENCE_FD_ANDROID attribute of is EGL_NO_NATIVE_FENCE_FD_ANDROID, an [invalid](https://developer.android.com/reference/kotlin/android/hardware/SyncFence.html#isValid())SyncFence is returned and an EGL_BAD_PARAMETER error is generated. \* If does not match the display passed to eglCreateSync when was created, the behaviour is undefined. This value cannot be`null`. |

### eglPresentationTimeANDROID

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun eglPresentationTimeANDROID(
    dpy: EGLDisplay!, 
    sur: EGLSurface!, 
    time: Long
): Boolean
```
