# SurfaceHolder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SurfaceHolder

Kotlin| [Java](../android/view/SurfaceHolder.md) 
| --- | --- |

```
interface SurfaceHolder
```

| [android.view.SurfaceHolder](../android/view/SurfaceHolder.md) |

Abstract interface to someone holding a display surface. Allows you to control the surface size and format, edit the pixels in the surface, and monitor changes to the surface. This interface is typically available through the [SurfaceView](../android/view/SurfaceView.md) class.

When using this interface from a thread other than the one running its [SurfaceView](../android/view/SurfaceView.md), you will want to carefully read the methods #lockCanvas and [Callback.surfaceCreated()](../android/view/SurfaceHolder.Callback.md)).

## Summary

| Nested classes ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [BadSurfaceTypeException](../android/view/SurfaceHolder.BadSurfaceTypeException.md) Exception that is thrown from #lockCanvas when called on a Surface whose type is SURFACE_TYPE_PUSH_BUFFERS. |
| abstract | [Callback](../android/view/SurfaceHolder.Callback.md) A client may implement this interface to receive information about changes to the surface. |
| abstract | [Callback2](../android/view/SurfaceHolder.Callback2.md) Additional callbacks that can be received for [Callback](../android/view/SurfaceHolder.Callback.md). |
| --- | --- |

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SURFACE_TYPE_GPU](../android/view/SurfaceHolder.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SURFACE_TYPE_HARDWARE](../android/view/SurfaceHolder.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SURFACE_TYPE_NORMAL](../android/view/SurfaceHolder.md) <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SURFACE_TYPE_PUSH_BUFFERS](../android/view/SurfaceHolder.md) <br /> |

| Public methods ||
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addCallback](../android/view/SurfaceHolder.md))`(`callback:` ` [SurfaceHolder.Callback](../android/view/SurfaceHolder.Callback.md)!`)` Add a Callback interface for this holder. |
| abstract [Surface](../android/view/Surface.md)! | [getSurface](../android/view/SurfaceHolder.md))`()` Direct access to the surface object. |
| abstract [Rect](../android/graphics/Rect.md)! | [getSurfaceFrame](../android/view/SurfaceHolder.md))`()` Retrieve the current size of the surface. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCreating](../android/view/SurfaceHolder.md))`()` Use this method to find out if the surface is in the process of being created from Callback methods. |
| abstract [Canvas](../android/graphics/Canvas.md)! | [lockCanvas](../android/view/SurfaceHolder.md))`()` Start editing the pixels in the surface. |
| abstract [Canvas](../android/graphics/Canvas.md)! | [lockCanvas](../android/view/SurfaceHolder.md))`(`dirty:` ` [Rect](../android/graphics/Rect.md)!`)` Just like [lockCanvas()](../android/view/SurfaceHolder.md))but allows specification of a dirty rectangle. |
| --- | --- |
| open [Canvas](../android/graphics/Canvas.md)! | [lockHardwareCanvas](../android/view/SurfaceHolder.md))`()` Just like [lockCanvas()](../android/view/SurfaceHolder.md))but the returned canvas is hardware-accelerated. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeCallback](../android/view/SurfaceHolder.md))`(`callback:` ` [SurfaceHolder.Callback](../android/view/SurfaceHolder.Callback.md)!`)` Removes a previously added Callback interface from this holder. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFixedSize](../android/view/SurfaceHolder.md))`(`width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `height:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Make the surface a fixed size. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFormat](../android/view/SurfaceHolder.md))`(`format:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the desired PixelFormat of the surface. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setKeepScreenOn](../android/view/SurfaceHolder.md))`(`screenOn:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Enable or disable option to keep the screen turned on while this surface is displayed. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSizeFromLayout](../android/view/SurfaceHolder.md))`()` Allow the surface to resized based on layout of its container (this is the default). |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setType](../android/view/SurfaceHolder.md))`(`type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the surface's type. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unlockCanvasAndPost](../android/view/SurfaceHolder.md))`(`canvas:` ` [Canvas](../android/graphics/Canvas.md)!`)` Finish editing pixels in the surface. |

## Constants

### SURFACE_TYPE_GPU

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SURFACE_TYPE_GPU: Int
```

**Deprecated:** *this is ignored, this value is set automatically when needed.* 

 Value: 2

### SURFACE_TYPE_HARDWARE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SURFACE_TYPE_HARDWARE: Int
```

**Deprecated:** *this is ignored, this value is set automatically when needed.* 

 Value: 1

### SURFACE_TYPE_NORMAL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SURFACE_TYPE_NORMAL: Int
```

**Deprecated:** *this is ignored, this value is set automatically when needed.* 

 Value: 0

### SURFACE_TYPE_PUSH_BUFFERS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SURFACE_TYPE_PUSH_BUFFERS: Int
```

**Deprecated:** *this is ignored, this value is set automatically when needed.* 

 Value: 3

## Public methods

### addCallback

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun addCallback(callback: SurfaceHolder.Callback!): Unit
```

Add a Callback interface for this holder. There can several Callback interfaces associated with a holder.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [SurfaceHolder.Callback](../android/view/SurfaceHolder.Callback.md)!:The new Callback interface. |

### getSurface

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getSurface(): Surface!
```

Direct access to the surface object. The Surface may not always be available -- for example when using a [SurfaceView](../android/view/SurfaceView.md) the holder's Surface is not created until the view has been attached to the window manager and performed a layout in order to determine the dimensions and screen position of the Surface. You will thus usually need to implement [Callback.surfaceCreated](../android/view/SurfaceHolder.Callback.md))to find out when the Surface is available for use.

Note that if you directly access the Surface from another thread, it is critical that you correctly implement [Callback.surfaceCreated](../android/view/SurfaceHolder.Callback.md))and [Callback.surfaceDestroyed](../android/view/SurfaceHolder.Callback.md))to ensure that thread only accesses the Surface while it is valid, and that the Surface does not get destroyed while the thread is using it.

This method is intended to be used by frameworks which often need direct access to the Surface object (usually to pass it to native code).

| Return ||
|---------------------------------------------------------------------------------|----------------------|
| [Surface](../android/view/Surface.md)! | Surface The surface. |

### getSurfaceFrame

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getSurfaceFrame(): Rect!
```

Retrieve the current size of the surface. Note: do not modify the returned Rect. This is only safe to call from the thread of [SurfaceView](../android/view/SurfaceView.md)'s window, or while inside of [lockCanvas()](../android/view/SurfaceHolder.md)).

| Return ||
|-------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [Rect](../android/graphics/Rect.md)! | Rect The surface's dimensions. The left and top are always 0. |

### isCreating

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isCreating(): Boolean
```

Use this method to find out if the surface is in the process of being created from Callback methods. This is intended to be used with [Callback.surfaceChanged](../android/view/SurfaceHolder.Callback.md)).

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the surface is in the process of being created. |

### lockCanvas

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun lockCanvas(): Canvas!
```

Start editing the pixels in the surface. The returned Canvas can be used to draw into the surface's bitmap. A null is returned if the surface has not been created or otherwise cannot be edited. You will usually need to implement [Callback.surfaceCreated](../android/view/SurfaceHolder.Callback.md))to find out when the Surface is available for use.

The content of the Surface is never preserved between unlockCanvas() and lockCanvas(), for this reason, every pixel within the Surface area must be written. The only exception to this rule is when a dirty rectangle is specified, in which case, non-dirty pixels will be preserved.

If you call this repeatedly when the Surface is not ready (before [Callback.surfaceCreated](../android/view/SurfaceHolder.Callback.md))or after [Callback.surfaceDestroyed](../android/view/SurfaceHolder.Callback.md))), your calls will be throttled to a slow rate in order to avoid consuming CPU.

If null is not returned, this function internally holds a lock until the corresponding [unlockCanvasAndPost](../android/view/SurfaceHolder.md))call, preventing [SurfaceView](../android/view/SurfaceView.md) from creating, destroying, or modifying the surface while it is being drawn. This can be more convenient than accessing the Surface directly, as you do not need to do special synchronization with a drawing thread in [Callback.surfaceDestroyed](../android/view/SurfaceHolder.Callback.md)).

| Return ||
|-----------------------------------------------------------------------------------------|--------------------------------------|
| [Canvas](../android/graphics/Canvas.md)! | Canvas Use to draw into the surface. |

### lockCanvas

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun lockCanvas(dirty: Rect!): Canvas!
```

Just like [lockCanvas()](../android/view/SurfaceHolder.md))but allows specification of a dirty rectangle. Every pixel within that rectangle must be written; however pixels outside the dirty rectangle will be preserved by the next call to lockCanvas().

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------|
| `dirty` | [Rect](../android/graphics/Rect.md)!:Area of the Surface that will be modified. |

| Return ||
|-----------------------------------------------------------------------------------------|--------------------------------------|
| [Canvas](../android/graphics/Canvas.md)! | Canvas Use to draw into the surface. |

**See Also**

### lockHardwareCanvas

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun lockHardwareCanvas(): Canvas!
```

Just like [lockCanvas()](../android/view/SurfaceHolder.md))but the returned canvas is hardware-accelerated.

See the [unsupported drawing operations](https://developer.android.com/guide/topics/graphics/hardware-accel.html#unsupported) for a list of what is and isn't supported in a hardware-accelerated canvas.

| Return ||
|-----------------------------------------------------------------------------------------|--------------------------------------|
| [Canvas](../android/graphics/Canvas.md)! | Canvas Use to draw into the surface. |

| Exceptions ||
|-----------------------------------|---------------------------------|
| `java.lang.IllegalStateException` | If the canvas cannot be locked. |

### removeCallback

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun removeCallback(callback: SurfaceHolder.Callback!): Unit
```

Removes a previously added Callback interface from this holder.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [SurfaceHolder.Callback](../android/view/SurfaceHolder.Callback.md)!:The Callback interface to remove. |

### setFixedSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setFixedSize(
    width: Int, 
    height: Int
): Unit
```

Make the surface a fixed size. It will never change from this size. When working with a [SurfaceView](../android/view/SurfaceView.md), this must be called from the same thread running the SurfaceView's window.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------|
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The surface's width. |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The surface's height. |

### setFormat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setFormat(format: Int): Unit
```

Set the desired PixelFormat of the surface. The default is OPAQUE. When working with a [SurfaceView](../android/view/SurfaceView.md), this must be called from the same thread running the SurfaceView's window.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------|
| `format` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A constant from PixelFormat. |

**See Also**

- [android.graphics.PixelFormat](../android/graphics/PixelFormat.md) 

### setKeepScreenOn

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setKeepScreenOn(screenOn: Boolean): Unit
```

Enable or disable option to keep the screen turned on while this surface is displayed. The default is false, allowing it to turn off. This is safe to call from any thread.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `screenOn` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Set to true to force the screen to stay on, false to allow it to turn off. |

### setSizeFromLayout

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setSizeFromLayout(): Unit
```

Allow the surface to resized based on layout of its container (this is the default). When this is enabled, you should monitor [Callback.surfaceChanged](../android/view/SurfaceHolder.Callback.md))for changes to the size of the surface. When working with a [SurfaceView](../android/view/SurfaceView.md), this must be called from the same thread running the SurfaceView's window. 

### setType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setType(type: Int): Unit
```

**Deprecated:** *this is ignored, this value is set automatically when needed.*

Sets the surface's type. 

### unlockCanvasAndPost

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun unlockCanvasAndPost(canvas: Canvas!): Unit
```

Finish editing pixels in the surface. After this call, the surface's current pixels will be shown on the screen, but its content is lost, in particular there is no guarantee that the content of the Surface will remain unchanged when lockCanvas() is called again.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `canvas` | [Canvas](../android/graphics/Canvas.md)!:The Canvas previously returned by lockCanvas(). |

**See Also**

- <https://developer.android.com/reference/kotlin/android/view/SurfaceHolder#lockCanvas()>
