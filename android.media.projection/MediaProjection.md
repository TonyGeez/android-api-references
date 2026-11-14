# MediaProjection

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MediaProjection

Kotlin| [Java](https://developer.android.com/reference/android/media/projection/MediaProjection "View this page in Java") 
| --- | --- |

```
class MediaProjection
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.projection.MediaProjection](https://developer.android.com/reference/kotlin/android/media/projection/MediaProjection#) |

A token granting applications the ability to capture screen contents and/or record system audio. The exact capabilities granted depend on the type of MediaProjection.

A screen capture session can be started through android.media.projection.MediaProjectionManager#createScreenCaptureIntent. This grants the ability to capture screen contents, but not system audio.

## Summary

| Nested classes ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [Callback](https://developer.android.com/reference/kotlin/android/media/projection/MediaProjection.Callback) Callbacks for the projection session. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [VirtualDisplay](https://developer.android.com/reference/kotlin/android/hardware/display/VirtualDisplay.html#)? | [createVirtualDisplay](https://developer.android.com/reference/kotlin/android/media/projection/MediaProjection#createVirtualDisplay(kotlin.String,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20android.view.Surface,%20android.hardware.display.VirtualDisplay.Callback,%20android.os.Handler))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `height:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dpi:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `surface:` ` [Surface](https://developer.android.com/reference/kotlin/android/view/Surface.html#)?`, `callback:` ` [VirtualDisplay.Callback](https://developer.android.com/reference/kotlin/android/hardware/display/VirtualDisplay.Callback.html#)?`, `handler:` ` [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)?`)` Creates a [android.hardware.display.VirtualDisplay](https://developer.android.com/reference/kotlin/android/hardware/display/VirtualDisplay.html#) to capture the contents of the screen. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerCallback](https://developer.android.com/reference/kotlin/android/media/projection/MediaProjection#registerCallback(android.media.projection.MediaProjection.Callback,%20android.os.Handler))`(`callback:` ` [MediaProjection.Callback](https://developer.android.com/reference/kotlin/android/media/projection/MediaProjection.Callback)`, `handler:` ` [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)?`)` Register a listener to receive notifications about when the [MediaProjection](https://developer.android.com/reference/kotlin/android/media/projection/MediaProjection#) or captured content changes state. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [stop](https://developer.android.com/reference/kotlin/android/media/projection/MediaProjection#stop())`()` Stops projection. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterCallback](https://developer.android.com/reference/kotlin/android/media/projection/MediaProjection#unregisterCallback(android.media.projection.MediaProjection.Callback))`(`callback:` ` [MediaProjection.Callback](https://developer.android.com/reference/kotlin/android/media/projection/MediaProjection.Callback)`)` Unregister a [MediaProjection](https://developer.android.com/reference/kotlin/android/media/projection/MediaProjection#) listener. |

## Public methods

### createVirtualDisplay

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun createVirtualDisplay(
    name: String, 
    width: Int, 
    height: Int, 
    dpi: Int, 
    flags: Int, 
    surface: Surface?, 
    callback: VirtualDisplay.Callback?, 
    handler: Handler?
): VirtualDisplay?
```

Creates a [android.hardware.display.VirtualDisplay](https://developer.android.com/reference/kotlin/android/hardware/display/VirtualDisplay.html#) to capture the contents of the screen.

To correctly clean up resources associated with a capture, the application must register a [Callback](https://developer.android.com/reference/kotlin/android/media/projection/MediaProjection.Callback) before invocation. The app must override [Callback.onStop()](https://developer.android.com/reference/kotlin/android/media/projection/MediaProjection.Callback#onStop())to clean up resources (by invoking [VirtualDisplay.release()](https://developer.android.com/reference/kotlin/android/hardware/display/VirtualDisplay.html#release()), [Surface.release()](https://developer.android.com/reference/kotlin/android/view/Surface.html#release())and related resources) and to update any available UI regarding the MediaProjection status.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The name of the virtual display, must be non-empty. This value cannot be`null`. |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The width of the virtual display in pixels. Must be greater than 0. |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The height of the virtual display in pixels. Must be greater than 0. |
| --- | --- |
| `dpi` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The density of the virtual display in dpi. Must be greater than 0. |
| `surface` | [Surface](https://developer.android.com/reference/kotlin/android/view/Surface.html#)?:The surface to which the content of the virtual display should be rendered, or null if there is none initially. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A combination of virtual display flags. See [DisplayManager](https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager.html#) for the full list of flags. Note that [DisplayManager.VIRTUAL_DISPLAY_FLAG_PRESENTATION](https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager.html#VIRTUAL_DISPLAY_FLAG_PRESENTATION:kotlin.Int) is always enabled. The following flags may be overridden, depending on how the component with {android.Manifest.permission.MANAGE_MEDIA_PROJECTION} handles the user's consent: [android.hardware.display.DisplayManager#VIRTUAL_DISPLAY_FLAG_OWN_CONTENT_ONLY](https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager.html#VIRTUAL_DISPLAY_FLAG_OWN_CONTENT_ONLY:kotlin.Int), [android.hardware.display.DisplayManager#VIRTUAL_DISPLAY_FLAG_AUTO_MIRROR](https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager.html#VIRTUAL_DISPLAY_FLAG_AUTO_MIRROR:kotlin.Int), [android.hardware.display.DisplayManager#VIRTUAL_DISPLAY_FLAG_PUBLIC](https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager.html#VIRTUAL_DISPLAY_FLAG_PUBLIC:kotlin.Int). Value is either`0`or a combination of [android.hardware.display.DisplayManager#VIRTUAL_DISPLAY_FLAG_PUBLIC](https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager.html#VIRTUAL_DISPLAY_FLAG_PUBLIC:kotlin.Int), [android.hardware.display.DisplayManager#VIRTUAL_DISPLAY_FLAG_PRESENTATION](https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager.html#VIRTUAL_DISPLAY_FLAG_PRESENTATION:kotlin.Int), [android.hardware.display.DisplayManager#VIRTUAL_DISPLAY_FLAG_SECURE](https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager.html#VIRTUAL_DISPLAY_FLAG_SECURE:kotlin.Int), [android.hardware.display.DisplayManager#VIRTUAL_DISPLAY_FLAG_OWN_CONTENT_ONLY](https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager.html#VIRTUAL_DISPLAY_FLAG_OWN_CONTENT_ONLY:kotlin.Int), [android.hardware.display.DisplayManager#VIRTUAL_DISPLAY_FLAG_AUTO_MIRROR](https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager.html#VIRTUAL_DISPLAY_FLAG_AUTO_MIRROR:kotlin.Int), android.hardware.display.DisplayManager.VIRTUAL_DISPLAY_FLAG_CAN_SHOW_WITH_INSECURE_KEYGUARD, android.hardware.display.DisplayManager.VIRTUAL_DISPLAY_FLAG_SUPPORTS_TOUCH, android.hardware.display.DisplayManager.VIRTUAL_DISPLAY_FLAG_ROTATES_WITH_CONTENT, android.hardware.display.DisplayManager.VIRTUAL_DISPLAY_FLAG_DESTROY_CONTENT_ON_REMOVAL, android.hardware.display.DisplayManager.VIRTUAL_DISPLAY_FLAG_SHOULD_SHOW_SYSTEM_DECORATIONS, android.hardware.display.DisplayManager.VIRTUAL_DISPLAY_FLAG_TRUSTED, android.hardware.display.DisplayManager.VIRTUAL_DISPLAY_FLAG_OWN_DISPLAY_GROUP, android.hardware.display.DisplayManager.VIRTUAL_DISPLAY_FLAG_ALWAYS_UNLOCKED, android.hardware.display.DisplayManager.VIRTUAL_DISPLAY_FLAG_TOUCH_FEEDBACK_DISABLED, android.hardware.display.DisplayManager.VIRTUAL_DISPLAY_FLAG_OWN_FOCUS, and android.hardware.display.DisplayManager.VIRTUAL_DISPLAY_FLAG_STEAL_TOP_FOCUS_DISABLED |
| --- | --- |
| `callback` | [VirtualDisplay.Callback](https://developer.android.com/reference/kotlin/android/hardware/display/VirtualDisplay.Callback.html#)?:Callback invoked when the virtual display's state changes, or null. |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)?:The [android.os.Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#) on which the callback should be invoked, or null if the callback should be invoked on the calling thread's main [android.os.Looper](https://developer.android.com/reference/kotlin/android/os/Looper.html#). |

| Return ||
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [VirtualDisplay](https://developer.android.com/reference/kotlin/android/hardware/display/VirtualDisplay.html#)? | The created [VirtualDisplay](https://developer.android.com/reference/kotlin/android/hardware/display/VirtualDisplay.html#), or`null`if no [VirtualDisplay](https://developer.android.com/reference/kotlin/android/hardware/display/VirtualDisplay.html#) could be created. |

| Exceptions ||
|-----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | If the target SDK is [U](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int) and up, and if no [Callback](https://developer.android.com/reference/kotlin/android/media/projection/MediaProjection.Callback) is registered. |
| `java.lang.SecurityException` | In any of the following scenarios: 1. If attempting to create a new virtual display associated with this MediaProjection instance after it has been stopped by invoking [stop()](https://developer.android.com/reference/kotlin/android/media/projection/MediaProjection#stop()). 2. If attempting to create a new virtual display associated with this MediaProjection instance after a [MediaProjection.Callback.onStop()](https://developer.android.com/reference/kotlin/android/media/projection/MediaProjection.Callback#onStop())callback has been received due to the user or the system stopping the MediaProjection session. 3. If the target SDK is [U](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int) and up, and if this instance has already taken a recording through`createVirtualDisplay`, but [stop()](https://developer.android.com/reference/kotlin/android/media/projection/MediaProjection#stop())wasn't invoked to end the recording. 4. If the target SDK is [U](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int) and up, and if [MediaProjectionManager.getMediaProjection](https://developer.android.com/reference/kotlin/android/media/projection/MediaProjectionManager#getMediaProjection(kotlin.Int,%20android.content.Intent))was invoked more than once to get this`MediaProjection`instance. In cases 2 \& 3, no exception is thrown if the target SDK is less than [U](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int). Instead, recording doesn't begin until the user re-grants consent in the dialog. |

**See Also**

- [android.hardware.display.VirtualDisplay](https://developer.android.com/reference/kotlin/android/hardware/display/VirtualDisplay.html#)
- [android.hardware.display.VirtualDisplay.Callback](https://developer.android.com/reference/kotlin/android/hardware/display/VirtualDisplay.Callback.html#) 

### registerCallback

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun registerCallback(
    callback: MediaProjection.Callback, 
    handler: Handler?
): Unit
```

Register a listener to receive notifications about when the [MediaProjection](https://developer.android.com/reference/kotlin/android/media/projection/MediaProjection#) or captured content changes state.

The callback must be registered before invoking [createVirtualDisplay(java.lang.String,int,int,int,int,android.view.Surface,android.hardware.display.VirtualDisplay.Callback,android.os.Handler)](https://developer.android.com/reference/kotlin/android/media/projection/MediaProjection#createVirtualDisplay(kotlin.String,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20android.view.Surface,%20android.hardware.display.VirtualDisplay.Callback,%20android.os.Handler))to ensure that any notifications on the callback are not missed. The client must implement [Callback.onStop()](https://developer.android.com/reference/kotlin/android/media/projection/MediaProjection.Callback#onStop())to properly handle MediaProjection clean up any resources it is holding, e.g. the [VirtualDisplay](https://developer.android.com/reference/kotlin/android/hardware/display/VirtualDisplay.html#) and [Surface](https://developer.android.com/reference/kotlin/android/view/Surface.html#). This should also update any application UI indicating the MediaProjection status as MediaProjection has stopped.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [MediaProjection.Callback](https://developer.android.com/reference/kotlin/android/media/projection/MediaProjection.Callback):The callback to call. This value cannot be`null`. |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)?:The handler on which the callback should be invoked, or null if the callback should be invoked on the calling thread's looper. |

| Exceptions ||
|----------------------------------|--------------------------------|
| `java.lang.NullPointerException` | If the given callback is null. |

**See Also**

- [#unregisterCallback](https://developer.android.com/reference/kotlin/android/media/projection/MediaProjection#unregisterCallback(android.media.projection.MediaProjection.Callback)) 

### stop

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun stop(): Unit
```

Stops projection. 

### unregisterCallback

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun unregisterCallback(callback: MediaProjection.Callback): Unit
```

Unregister a [MediaProjection](https://developer.android.com/reference/kotlin/android/media/projection/MediaProjection#) listener.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [MediaProjection.Callback](https://developer.android.com/reference/kotlin/android/media/projection/MediaProjection.Callback):The callback to unregister. This value cannot be`null`. |

| Exceptions ||
|----------------------------------|--------------------------------|
| `java.lang.NullPointerException` | If the given callback is null. |

**See Also**

- [#registerCallback](https://developer.android.com/reference/kotlin/android/media/projection/MediaProjection#registerCallback(android.media.projection.MediaProjection.Callback,%20android.os.Handler))
