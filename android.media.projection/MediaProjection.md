# MediaProjection

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MediaProjection

Kotlin| [Java](MediaProjection.md) 
| --- | --- |

```
class MediaProjection
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.projection.MediaProjection](MediaProjection.md) |

A token granting applications the ability to capture screen contents and/or record system audio. The exact capabilities granted depend on the type of MediaProjection.

A screen capture session can be started through android.media.projection.MediaProjectionManager#createScreenCaptureIntent. This grants the ability to capture screen contents, but not system audio.

## Summary

| Nested classes ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [Callback](../android/media/projection/MediaProjection.Callback.md) Callbacks for the projection session. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [VirtualDisplay](../android.hardware.display/VirtualDisplay.md)? | [createVirtualDisplay](MediaProjection.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `height:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dpi:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `surface:` ` [Surface](../android.view/Surface.md)?`, `callback:` ` [VirtualDisplay.Callback](../android/hardware/display/VirtualDisplay.Callback.md)?`, `handler:` ` [Handler](../android.os/Handler.md)?`)` Creates a [android.hardware.display.VirtualDisplay](../android.hardware.display/VirtualDisplay.md) to capture the contents of the screen. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerCallback](MediaProjection.md))`(`callback:` ` [MediaProjection.Callback](../android/media/projection/MediaProjection.Callback.md)`, `handler:` ` [Handler](../android.os/Handler.md)?`)` Register a listener to receive notifications about when the [MediaProjection](MediaProjection.md) or captured content changes state. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [stop](MediaProjection.md))`()` Stops projection. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterCallback](MediaProjection.md))`(`callback:` ` [MediaProjection.Callback](../android/media/projection/MediaProjection.Callback.md)`)` Unregister a [MediaProjection](MediaProjection.md) listener. |

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

Creates a [android.hardware.display.VirtualDisplay](../android.hardware.display/VirtualDisplay.md) to capture the contents of the screen.

To correctly clean up resources associated with a capture, the application must register a [Callback](../android/media/projection/MediaProjection.Callback.md) before invocation. The app must override [Callback.onStop()](../android/media/projection/MediaProjection.Callback.md))to clean up resources (by invoking [VirtualDisplay.release()](../android.hardware.display/VirtualDisplay.md)), [Surface.release()](../android.view/Surface.md))and related resources) and to update any available UI regarding the MediaProjection status.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The name of the virtual display, must be non-empty. This value cannot be`null`. |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The width of the virtual display in pixels. Must be greater than 0. |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The height of the virtual display in pixels. Must be greater than 0. |
| --- | --- |
| `dpi` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The density of the virtual display in dpi. Must be greater than 0. |
| `surface` | [Surface](../android.view/Surface.md)?:The surface to which the content of the virtual display should be rendered, or null if there is none initially. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A combination of virtual display flags. See [DisplayManager](../android.hardware.display/DisplayManager.md) for the full list of flags. Note that [DisplayManager.VIRTUAL_DISPLAY_FLAG_PRESENTATION](../android.hardware.display/DisplayManager.md) is always enabled. The following flags may be overridden, depending on how the component with {android.Manifest.permission.MANAGE_MEDIA_PROJECTION} handles the user's consent: [android.hardware.display.DisplayManager#VIRTUAL_DISPLAY_FLAG_OWN_CONTENT_ONLY](../android.hardware.display/DisplayManager.md), [android.hardware.display.DisplayManager#VIRTUAL_DISPLAY_FLAG_AUTO_MIRROR](../android.hardware.display/DisplayManager.md), [android.hardware.display.DisplayManager#VIRTUAL_DISPLAY_FLAG_PUBLIC](../android.hardware.display/DisplayManager.md). Value is either`0`or a combination of [android.hardware.display.DisplayManager#VIRTUAL_DISPLAY_FLAG_PUBLIC](../android.hardware.display/DisplayManager.md), [android.hardware.display.DisplayManager#VIRTUAL_DISPLAY_FLAG_PRESENTATION](../android.hardware.display/DisplayManager.md), [android.hardware.display.DisplayManager#VIRTUAL_DISPLAY_FLAG_SECURE](../android.hardware.display/DisplayManager.md), [android.hardware.display.DisplayManager#VIRTUAL_DISPLAY_FLAG_OWN_CONTENT_ONLY](../android.hardware.display/DisplayManager.md), [android.hardware.display.DisplayManager#VIRTUAL_DISPLAY_FLAG_AUTO_MIRROR](../android.hardware.display/DisplayManager.md), android.hardware.display.DisplayManager.VIRTUAL_DISPLAY_FLAG_CAN_SHOW_WITH_INSECURE_KEYGUARD, android.hardware.display.DisplayManager.VIRTUAL_DISPLAY_FLAG_SUPPORTS_TOUCH, android.hardware.display.DisplayManager.VIRTUAL_DISPLAY_FLAG_ROTATES_WITH_CONTENT, android.hardware.display.DisplayManager.VIRTUAL_DISPLAY_FLAG_DESTROY_CONTENT_ON_REMOVAL, android.hardware.display.DisplayManager.VIRTUAL_DISPLAY_FLAG_SHOULD_SHOW_SYSTEM_DECORATIONS, android.hardware.display.DisplayManager.VIRTUAL_DISPLAY_FLAG_TRUSTED, android.hardware.display.DisplayManager.VIRTUAL_DISPLAY_FLAG_OWN_DISPLAY_GROUP, android.hardware.display.DisplayManager.VIRTUAL_DISPLAY_FLAG_ALWAYS_UNLOCKED, android.hardware.display.DisplayManager.VIRTUAL_DISPLAY_FLAG_TOUCH_FEEDBACK_DISABLED, android.hardware.display.DisplayManager.VIRTUAL_DISPLAY_FLAG_OWN_FOCUS, and android.hardware.display.DisplayManager.VIRTUAL_DISPLAY_FLAG_STEAL_TOP_FOCUS_DISABLED |
| --- | --- |
| `callback` | [VirtualDisplay.Callback](../android/hardware/display/VirtualDisplay.Callback.md)?:Callback invoked when the virtual display's state changes, or null. |
| `handler` | [Handler](../android.os/Handler.md)?:The [android.os.Handler](../android.os/Handler.md) on which the callback should be invoked, or null if the callback should be invoked on the calling thread's main [android.os.Looper](../android.os/Looper.md). |

| Return ||
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [VirtualDisplay](../android.hardware.display/VirtualDisplay.md)? | The created [VirtualDisplay](../android.hardware.display/VirtualDisplay.md), or`null`if no [VirtualDisplay](../android.hardware.display/VirtualDisplay.md) could be created. |

| Exceptions ||
|-----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | If the target SDK is [U](../android/os/Build.VERSION_CODES.md) and up, and if no [Callback](../android/media/projection/MediaProjection.Callback.md) is registered. |
| `java.lang.SecurityException` | In any of the following scenarios: 1. If attempting to create a new virtual display associated with this MediaProjection instance after it has been stopped by invoking [stop()](MediaProjection.md)). 2. If attempting to create a new virtual display associated with this MediaProjection instance after a [MediaProjection.Callback.onStop()](../android/media/projection/MediaProjection.Callback.md))callback has been received due to the user or the system stopping the MediaProjection session. 3. If the target SDK is [U](../android/os/Build.VERSION_CODES.md) and up, and if this instance has already taken a recording through`createVirtualDisplay`, but [stop()](MediaProjection.md))wasn't invoked to end the recording. 4. If the target SDK is [U](../android/os/Build.VERSION_CODES.md) and up, and if [MediaProjectionManager.getMediaProjection](MediaProjectionManager.md))was invoked more than once to get this`MediaProjection`instance. In cases 2 \& 3, no exception is thrown if the target SDK is less than [U](../android/os/Build.VERSION_CODES.md). Instead, recording doesn't begin until the user re-grants consent in the dialog. |

**See Also**

- [android.hardware.display.VirtualDisplay](../android.hardware.display/VirtualDisplay.md)
- [android.hardware.display.VirtualDisplay.Callback](../android/hardware/display/VirtualDisplay.Callback.md) 

### registerCallback

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun registerCallback(
    callback: MediaProjection.Callback, 
    handler: Handler?
): Unit
```

Register a listener to receive notifications about when the [MediaProjection](MediaProjection.md) or captured content changes state.

The callback must be registered before invoking [createVirtualDisplay(java.lang.String,int,int,int,int,android.view.Surface,android.hardware.display.VirtualDisplay.Callback,android.os.Handler)](MediaProjection.md))to ensure that any notifications on the callback are not missed. The client must implement [Callback.onStop()](../android/media/projection/MediaProjection.Callback.md))to properly handle MediaProjection clean up any resources it is holding, e.g. the [VirtualDisplay](../android.hardware.display/VirtualDisplay.md) and [Surface](../android.view/Surface.md). This should also update any application UI indicating the MediaProjection status as MediaProjection has stopped.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [MediaProjection.Callback](../android/media/projection/MediaProjection.Callback.md):The callback to call. This value cannot be`null`. |
| `handler` | [Handler](../android.os/Handler.md)?:The handler on which the callback should be invoked, or null if the callback should be invoked on the calling thread's looper. |

| Exceptions ||
|----------------------------------|--------------------------------|
| `java.lang.NullPointerException` | If the given callback is null. |

**See Also**

- [#unregisterCallback](MediaProjection.md)) 

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

Unregister a [MediaProjection](MediaProjection.md) listener.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [MediaProjection.Callback](../android/media/projection/MediaProjection.Callback.md):The callback to unregister. This value cannot be`null`. |

| Exceptions ||
|----------------------------------|--------------------------------|
| `java.lang.NullPointerException` | If the given callback is null. |

**See Also**

- [#registerCallback](MediaProjection.md))
