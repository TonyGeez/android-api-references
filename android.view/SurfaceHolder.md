# SurfaceHolder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SurfaceHolder

Kotlin| [Java](https://developer.android.com/reference/android/view/SurfaceHolder "View this page in Java") 

```
interface SurfaceHolder
```

| [android.view.SurfaceHolder](https://developer.android.com/reference/kotlin/android/view/SurfaceHolder#) |

Abstract interface to someone holding a display surface. Allows you to control the surface size and format, edit the pixels in the surface, and monitor changes to the surface. This interface is typically available through the [SurfaceView](https://developer.android.com/reference/kotlin/android/view/SurfaceView) class.

When using this interface from a thread other than the one running its [SurfaceView](https://developer.android.com/reference/kotlin/android/view/SurfaceView), you will want to carefully read the methods #lockCanvas and [Callback.surfaceCreated()](https://developer.android.com/reference/kotlin/android/view/SurfaceHolder.Callback#surfaceCreated(android.view.SurfaceHolder)).

## Summary

| Nested classes ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [BadSurfaceTypeException](https://developer.android.com/reference/kotlin/android/view/SurfaceHolder.BadSurfaceTypeException) Exception that is thrown from #lockCanvas when called on a Surface whose type is SURFACE_TYPE_PUSH_BUFFERS. |
| abstract | [Callback](https://developer.android.com/reference/kotlin/android/view/SurfaceHolder.Callback) A client may implement this interface to receive information about changes to the surface. |
| abstract | [Callback2](https://developer.android.com/reference/kotlin/android/view/SurfaceHolder.Callback2) Additional callbacks that can be received for [Callback](https://developer.android.com/reference/kotlin/android/view/SurfaceHolder.Callback). |

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SURFACE_TYPE_GPU](https://developer.android.com/reference/kotlin/android/view/SurfaceHolder#SURFACE_TYPE_GPU:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SURFACE_TYPE_HARDWARE](https://developer.android.com/reference/kotlin/android/view/SurfaceHolder#SURFACE_TYPE_HARDWARE:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SURFACE_TYPE_NORMAL](https://developer.android.com/reference/kotlin/android/view/SurfaceHolder#SURFACE_TYPE_NORMAL:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SURFACE_TYPE_PUSH_BUFFERS](https://developer.android.com/reference/kotlin/android/view/SurfaceHolder#SURFACE_TYPE_PUSH_BUFFERS:kotlin.Int) <br /> |

| Public methods ||
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addCallback](https://developer.android.com/reference/kotlin/android/view/SurfaceHolder#addCallback(android.view.SurfaceHolder.Callback))`(`callback:` ` [SurfaceHolder.Callback](https://developer.android.com/reference/kotlin/android/view/SurfaceHolder.Callback)!`)` Add a Callback interface for this holder. |
| abstract [Surface](https://developer.android.com/reference/kotlin/android/view/Surface)! | [getSurface](https://developer.android.com/reference/kotlin/android/view/SurfaceHolder#getSurface())`()` Direct access to the surface object. |
| abstract [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)! | [getSurfaceFrame](https://developer.android.com/reference/kotlin/android/view/SurfaceHolder#getSurfaceFrame())`()` Retrieve the current size of the surface. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCreating](https://developer.android.com/reference/kotlin/android/view/SurfaceHolder#isCreating())`()` Use this method to find out if the surface is in the process of being created from Callback methods. |
| abstract [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#)! | [lockCanvas](https://developer.android.com/reference/kotlin/android/view/SurfaceHolder#lockCanvas())`()` Start editing the pixels in the surface. |
| abstract [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#)! | [lockCanvas](https://developer.android.com/reference/kotlin/android/view/SurfaceHolder#lockCanvas(android.graphics.Rect))`(`dirty:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)!`)` Just like [lockCanvas()](https://developer.android.com/reference/kotlin/android/view/SurfaceHolder#lockCanvas())but allows specification of a dirty rectangle. |
| open [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#)! | [lockHardwareCanvas](https://developer.android.com/reference/kotlin/android/view/SurfaceHolder#lockHardwareCanvas())`()` Just like [lockCanvas()](https://developer.android.com/reference/kotlin/android/view/SurfaceHolder#lockCanvas())but the returned canvas is hardware-accelerated. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeCallback](https://developer.android.com/reference/kotlin/android/view/SurfaceHolder#removeCallback(android.view.SurfaceHolder.Callback))`(`callback:` ` [SurfaceHolder.Callback](https://developer.android.com/reference/kotlin/android/view/SurfaceHolder.Callback)!`)` Removes a previously added Callback interface from this holder. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFixedSize](https://developer.android.com/reference/kotlin/android/view/SurfaceHolder#setFixedSize(kotlin.Int,%20kotlin.Int))`(`width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `height:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Make the surface a fixed size. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFormat](https://developer.android.com/reference/kotlin/android/view/SurfaceHolder#setFormat(kotlin.Int))`(`format:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the desired PixelFormat of the surface. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setKeepScreenOn](https://developer.android.com/reference/kotlin/android/view/SurfaceHolder#setKeepScreenOn(kotlin.Boolean))`(`screenOn:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Enable or disable option to keep the screen turned on while this surface is displayed. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSizeFromLayout](https://developer.android.com/reference/kotlin/android/view/SurfaceHolder#setSizeFromLayout())`()` Allow the surface to resized based on layout of its container (this is the default). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setType](https://developer.android.com/reference/kotlin/android/view/SurfaceHolder#setType(kotlin.Int))`(`type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the surface's type. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unlockCanvasAndPost](https://developer.android.com/reference/kotlin/android/view/SurfaceHolder#unlockCanvasAndPost(android.graphics.Canvas))`(`canvas:` ` [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#)!`)` Finish editing pixels in the surface. |

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
| `callback` | [SurfaceHolder.Callback](https://developer.android.com/reference/kotlin/android/view/SurfaceHolder.Callback)!:The new Callback interface. |

### getSurface

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getSurface(): Surface!
```

Direct access to the surface object. The Surface may not always be available -- for example when using a [SurfaceView](https://developer.android.com/reference/kotlin/android/view/SurfaceView) the holder's Surface is not created until the view has been attached to the window manager and performed a layout in order to determine the dimensions and screen position of the Surface. You will thus usually need to implement [Callback.surfaceCreated](https://developer.android.com/reference/kotlin/android/view/SurfaceHolder.Callback#surfaceCreated(android.view.SurfaceHolder))to find out when the Surface is available for use.

Note that if you directly access the Surface from another thread, it is critical that you correctly implement [Callback.surfaceCreated](https://developer.android.com/reference/kotlin/android/view/SurfaceHolder.Callback#surfaceCreated(android.view.SurfaceHolder))and [Callback.surfaceDestroyed](https://developer.android.com/reference/kotlin/android/view/SurfaceHolder.Callback#surfaceDestroyed(android.view.SurfaceHolder))to ensure that thread only accesses the Surface while it is valid, and that the Surface does not get destroyed while the thread is using it.

This method is intended to be used by frameworks which often need direct access to the Surface object (usually to pass it to native code).

| Return ||
|---------------------------------------------------------------------------------|----------------------|
| [Surface](https://developer.android.com/reference/kotlin/android/view/Surface)! | Surface The surface. |

### getSurfaceFrame

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getSurfaceFrame(): Rect!
```

Retrieve the current size of the surface. Note: do not modify the returned Rect. This is only safe to call from the thread of [SurfaceView](https://developer.android.com/reference/kotlin/android/view/SurfaceView)'s window, or while inside of [lockCanvas()](https://developer.android.com/reference/kotlin/android/view/SurfaceHolder#lockCanvas()).

| Return ||
|-------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)! | Rect The surface's dimensions. The left and top are always 0. |

### isCreating

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isCreating(): Boolean
```

Use this method to find out if the surface is in the process of being created from Callback methods. This is intended to be used with [Callback.surfaceChanged](https://developer.android.com/reference/kotlin/android/view/SurfaceHolder.Callback#surfaceChanged(android.view.SurfaceHolder,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)).

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the surface is in the process of being created. |

### lockCanvas

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun lockCanvas(): Canvas!
```

Start editing the pixels in the surface. The returned Canvas can be used to draw into the surface's bitmap. A null is returned if the surface has not been created or otherwise cannot be edited. You will usually need to implement [Callback.surfaceCreated](https://developer.android.com/reference/kotlin/android/view/SurfaceHolder.Callback#surfaceCreated(android.view.SurfaceHolder))to find out when the Surface is available for use.

The content of the Surface is never preserved between unlockCanvas() and lockCanvas(), for this reason, every pixel within the Surface area must be written. The only exception to this rule is when a dirty rectangle is specified, in which case, non-dirty pixels will be preserved.

If you call this repeatedly when the Surface is not ready (before [Callback.surfaceCreated](https://developer.android.com/reference/kotlin/android/view/SurfaceHolder.Callback#surfaceCreated(android.view.SurfaceHolder))or after [Callback.surfaceDestroyed](https://developer.android.com/reference/kotlin/android/view/SurfaceHolder.Callback#surfaceDestroyed(android.view.SurfaceHolder))), your calls will be throttled to a slow rate in order to avoid consuming CPU.

If null is not returned, this function internally holds a lock until the corresponding [unlockCanvasAndPost](https://developer.android.com/reference/kotlin/android/view/SurfaceHolder#unlockCanvasAndPost(android.graphics.Canvas))call, preventing [SurfaceView](https://developer.android.com/reference/kotlin/android/view/SurfaceView) from creating, destroying, or modifying the surface while it is being drawn. This can be more convenient than accessing the Surface directly, as you do not need to do special synchronization with a drawing thread in [Callback.surfaceDestroyed](https://developer.android.com/reference/kotlin/android/view/SurfaceHolder.Callback#surfaceDestroyed(android.view.SurfaceHolder)).

| Return ||
|-----------------------------------------------------------------------------------------|--------------------------------------|
| [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#)! | Canvas Use to draw into the surface. |

### lockCanvas

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun lockCanvas(dirty: Rect!): Canvas!
```

Just like [lockCanvas()](https://developer.android.com/reference/kotlin/android/view/SurfaceHolder#lockCanvas())but allows specification of a dirty rectangle. Every pixel within that rectangle must be written; however pixels outside the dirty rectangle will be preserved by the next call to lockCanvas().

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------|
| `dirty` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)!:Area of the Surface that will be modified. |

| Return ||
|-----------------------------------------------------------------------------------------|--------------------------------------|
| [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#)! | Canvas Use to draw into the surface. |

**See Also**

### lockHardwareCanvas

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun lockHardwareCanvas(): Canvas!
```

Just like [lockCanvas()](https://developer.android.com/reference/kotlin/android/view/SurfaceHolder#lockCanvas())but the returned canvas is hardware-accelerated.

See the [unsupported drawing operations](https://developer.android.com/guide/topics/graphics/hardware-accel.html#unsupported) for a list of what is and isn't supported in a hardware-accelerated canvas.

| Return ||
|-----------------------------------------------------------------------------------------|--------------------------------------|
| [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#)! | Canvas Use to draw into the surface. |

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
| `callback` | [SurfaceHolder.Callback](https://developer.android.com/reference/kotlin/android/view/SurfaceHolder.Callback)!:The Callback interface to remove. |

### setFixedSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setFixedSize(
    width: Int, 
    height: Int
): Unit
```

Make the surface a fixed size. It will never change from this size. When working with a [SurfaceView](https://developer.android.com/reference/kotlin/android/view/SurfaceView), this must be called from the same thread running the SurfaceView's window.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------|
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The surface's width. |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The surface's height. |

### setFormat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setFormat(format: Int): Unit
```

Set the desired PixelFormat of the surface. The default is OPAQUE. When working with a [SurfaceView](https://developer.android.com/reference/kotlin/android/view/SurfaceView), this must be called from the same thread running the SurfaceView's window.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------|
| `format` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A constant from PixelFormat. |

**See Also**

- [android.graphics.PixelFormat](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat.html#) 

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

Allow the surface to resized based on layout of its container (this is the default). When this is enabled, you should monitor [Callback.surfaceChanged](https://developer.android.com/reference/kotlin/android/view/SurfaceHolder.Callback#surfaceChanged(android.view.SurfaceHolder,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))for changes to the size of the surface. When working with a [SurfaceView](https://developer.android.com/reference/kotlin/android/view/SurfaceView), this must be called from the same thread running the SurfaceView's window. 

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
| `canvas` | [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#)!:The Canvas previously returned by lockCanvas(). |

**See Also**

- <https://developer.android.com/reference/kotlin/android/view/SurfaceHolder#lockCanvas()>
