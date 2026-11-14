# Surface

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Surface

Kotlin| [Java](https://developer.android.com/reference/android/view/Surface "View this page in Java") 
| --- | --- |

```
open class Surface : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.Surface](https://developer.android.com/reference/kotlin/android/view/Surface#) |

Handle onto a raw buffer that is being managed by the screen compositor.

A Surface is generally created by or from a consumer of image buffers (such as a [android.graphics.SurfaceTexture](https://developer.android.com/reference/kotlin/android/graphics/SurfaceTexture.html#), [android.media.MediaRecorder](https://developer.android.com/reference/kotlin/android/media/MediaRecorder.html#), or [android.renderscript.Allocation](https://developer.android.com/reference/kotlin/android/renderscript/Allocation.html#)), and is handed to some kind of producer (such as [OpenGL](https://developer.android.com/reference/kotlin/android/opengl/EGL14.html#eglCreateWindowSurface(android.opengl.EGLDisplay,%20android.opengl.EGLConfig,%20kotlin.Any,%20kotlin.IntArray,%20kotlin.Int)), [MediaPlayer](https://developer.android.com/reference/kotlin/android/media/MediaPlayer.html#setSurface(android.view.Surface)), or android.hardware.camera2.CameraDevice#createCaptureSession) to draw into.

**Note:** A Surface acts like a [weak reference](https://developer.android.com/reference/kotlin/java/lang/ref/WeakReference.html#) to the consumer it is associated with. By itself it will not keep its parent consumer from being reclaimed.

## Summary

| Nested classes ||
|------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [OutOfResourcesException](https://developer.android.com/reference/kotlin/android/view/Surface.OutOfResourcesException) Exception thrown when a Canvas couldn't be locked with [Surface.lockCanvas](https://developer.android.com/reference/kotlin/android/view/Surface#lockCanvas(android.graphics.Rect)), or when a SurfaceTexture could not successfully be allocated. |

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CHANGE_FRAME_RATE_ALWAYS](https://developer.android.com/reference/kotlin/android/view/Surface#CHANGE_FRAME_RATE_ALWAYS:kotlin.Int) Change the frame rate even if the transition is going to be non-seamless, i. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CHANGE_FRAME_RATE_ONLY_IF_SEAMLESS](https://developer.android.com/reference/kotlin/android/view/Surface#CHANGE_FRAME_RATE_ONLY_IF_SEAMLESS:kotlin.Int) Change the frame rate only if the transition is going to be seamless. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FRAME_RATE_COMPATIBILITY_AT_LEAST](https://developer.android.com/reference/kotlin/android/view/Surface#FRAME_RATE_COMPATIBILITY_AT_LEAST:kotlin.Int) The surface requests a frame rate that is at least the specified frame rate. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FRAME_RATE_COMPATIBILITY_DEFAULT](https://developer.android.com/reference/kotlin/android/view/Surface#FRAME_RATE_COMPATIBILITY_DEFAULT:kotlin.Int) There are no inherent restrictions on the frame rate of this surface. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FRAME_RATE_COMPATIBILITY_FIXED_SOURCE](https://developer.android.com/reference/kotlin/android/view/Surface#FRAME_RATE_COMPATIBILITY_FIXED_SOURCE:kotlin.Int) This surface is being used to display content with an inherently fixed frame rate, e. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ROTATION_0](https://developer.android.com/reference/kotlin/android/view/Surface#ROTATION_0:kotlin.Int) Rotation constant: 0 degree rotation (natural orientation) |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ROTATION_180](https://developer.android.com/reference/kotlin/android/view/Surface#ROTATION_180:kotlin.Int) Rotation constant: 180 degree rotation. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ROTATION_270](https://developer.android.com/reference/kotlin/android/view/Surface#ROTATION_270:kotlin.Int) Rotation constant: 270 degree rotation. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ROTATION_90](https://developer.android.com/reference/kotlin/android/view/Surface#ROTATION_90:kotlin.Int) Rotation constant: 90 degree rotation. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Surface](https://developer.android.com/reference/kotlin/android/view/Surface#Surface(android.graphics.SurfaceTexture))`(`surfaceTexture:` ` [SurfaceTexture](https://developer.android.com/reference/kotlin/android/graphics/SurfaceTexture.html#)!`)` Create Surface from a [SurfaceTexture](https://developer.android.com/reference/kotlin/android/graphics/SurfaceTexture.html#). |
| [Surface](https://developer.android.com/reference/kotlin/android/view/Surface#Surface(android.view.SurfaceControl))`(`from:` ` [SurfaceControl](https://developer.android.com/reference/kotlin/android/view/SurfaceControl)`)` Create a Surface associated with a given [SurfaceControl](https://developer.android.com/reference/kotlin/android/view/SurfaceControl). |

| Public methods ||
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearFrameRate](https://developer.android.com/reference/kotlin/android/view/Surface#clearFrameRate())`()` Clears the frame rate which was set for this surface. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/view/Surface#describeContents())`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isValid](https://developer.android.com/reference/kotlin/android/view/Surface#isValid())`()` Returns true if this object holds a valid surface. |
| --- | --- |
| open [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#)! | [lockCanvas](https://developer.android.com/reference/kotlin/android/view/Surface#lockCanvas(android.graphics.Rect))`(`inOutDirty:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)!`)` Gets a [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#) for drawing into this surface. |
| open [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#)! | [lockHardwareCanvas](https://developer.android.com/reference/kotlin/android/view/Surface#lockHardwareCanvas())`()` Gets a [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#) for drawing into this surface. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [readFromParcel](https://developer.android.com/reference/kotlin/android/view/Surface#readFromParcel(android.os.Parcel))`(`source:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)!`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [release](https://developer.android.com/reference/kotlin/android/view/Surface#release())`()` Release the local reference to the server-side surface. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFrameRate](https://developer.android.com/reference/kotlin/android/view/Surface#setFrameRate(kotlin.Float,%20kotlin.Int))`(`frameRate:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `compatibility:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the intended frame rate for this surface. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFrameRate](https://developer.android.com/reference/kotlin/android/view/Surface#setFrameRate(kotlin.Float,%20kotlin.Int,%20kotlin.Int))`(`frameRate:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `compatibility:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `changeFrameRateStrategy:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the intended frame rate for this surface. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/view/Surface#toString())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unlockCanvas](https://developer.android.com/reference/kotlin/android/view/Surface#unlockCanvas(android.graphics.Canvas))`(`canvas:` ` [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unlockCanvasAndPost](https://developer.android.com/reference/kotlin/android/view/Surface#unlockCanvasAndPost(android.graphics.Canvas))`(`canvas:` ` [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#)!`)` Posts the new contents of the [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#) to the surface and releases the [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#). |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/view/Surface#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Protected methods ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](https://developer.android.com/reference/kotlin/android/view/Surface#finalize())`()` <br /> |

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [Surface](https://developer.android.com/reference/kotlin/android/view/Surface#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/view/Surface#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### CHANGE_FRAME_RATE_ALWAYS

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CHANGE_FRAME_RATE_ALWAYS: Int
```

Change the frame rate even if the transition is going to be non-seamless, i.e. with visual interruptions for the user. Non-seamless switches might be used when the benefit of matching the content's frame rate outweighs the cost of the transition, for example when displaying long-running video content. 

 Value: 1

### CHANGE_FRAME_RATE_ONLY_IF_SEAMLESS

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CHANGE_FRAME_RATE_ONLY_IF_SEAMLESS: Int
```

Change the frame rate only if the transition is going to be seamless. 

 Value: 0

### FRAME_RATE_COMPATIBILITY_AT_LEAST

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FRAME_RATE_COMPATIBILITY_AT_LEAST: Int
```

The surface requests a frame rate that is at least the specified frame rate. This value should be used for UIs, animations, scrolling and fling, and anything that is not a game or video. For video, use FRAME_RATE_COMPATIBILITY_FIXED_SOURCE instead. For game content, use FRAME_RATE_COMPATIBILITY_DEFAULT. 

 Value: 2

### FRAME_RATE_COMPATIBILITY_DEFAULT

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FRAME_RATE_COMPATIBILITY_DEFAULT: Int
```

There are no inherent restrictions on the frame rate of this surface. When the system selects a frame rate other than what the app requested, the app will be able to run at the system frame rate without requiring pull down. This value should be used when displaying game content, UIs, and anything that isn't video. In Android version [Build.VERSION_CODES.BAKLAVA](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#BAKLAVA:kotlin.Int) and above, use FRAME_RATE_COMPATIBILITY_DEFAULT for game content. For other cases, see FRAME_RATE_COMPATIBILITY_FIXED_SOURCE and FRAME_RATE_COMPATIBILITY_AT_LEAST. 

 Value: 0

### FRAME_RATE_COMPATIBILITY_FIXED_SOURCE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FRAME_RATE_COMPATIBILITY_FIXED_SOURCE: Int
```

This surface is being used to display content with an inherently fixed frame rate, e.g. a video that has a specific frame rate. When the system selects a frame rate other than what the app requested, the app will need to do pull down or use some other technique to adapt to the system's frame rate. The user experience is likely to be worse (e.g. more frame stuttering) than it would be if the system had chosen the app's requested frame rate. This value should be used for video content. 

 Value: 1

### ROTATION_0

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ROTATION_0: Int
```

Rotation constant: 0 degree rotation (natural orientation) 

 Value: 0

### ROTATION_180

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ROTATION_180: Int
```

Rotation constant: 180 degree rotation. 

 Value: 2

### ROTATION_270

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ROTATION_270: Int
```

Rotation constant: 270 degree rotation. 

 Value: 3

### ROTATION_90

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ROTATION_90: Int
```

Rotation constant: 90 degree rotation. 

 Value: 1

## Public constructors

### Surface

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Surface(surfaceTexture: SurfaceTexture!)
```

Create Surface from a [SurfaceTexture](https://developer.android.com/reference/kotlin/android/graphics/SurfaceTexture.html#). Images drawn to the Surface will be made available to the [SurfaceTexture](https://developer.android.com/reference/kotlin/android/graphics/SurfaceTexture.html#), which can attach them to an OpenGL ES texture via [android.graphics.SurfaceTexture#updateTexImage](https://developer.android.com/reference/kotlin/android/graphics/SurfaceTexture.html#updateTexImage()). Please note that holding onto the Surface created here is not enough to keep the provided SurfaceTexture from being reclaimed. In that sense, the Surface will act like a [weak reference](https://developer.android.com/reference/kotlin/java/lang/ref/WeakReference.html#) to the SurfaceTexture.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `surfaceTexture` | [SurfaceTexture](https://developer.android.com/reference/kotlin/android/graphics/SurfaceTexture.html#)!:The [SurfaceTexture](https://developer.android.com/reference/kotlin/android/graphics/SurfaceTexture.html#) that is updated by this Surface. |

| Exceptions ||
|------------------------------------------------|--------------------------------------|
| `android.view.Surface.OutOfResourcesException` | if the surface could not be created. |

### Surface

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Surface(from: SurfaceControl)
```

Create a Surface associated with a given [SurfaceControl](https://developer.android.com/reference/kotlin/android/view/SurfaceControl). Buffers submitted to this surface will be displayed by the system compositor according to the parameters specified by the control. Multiple surfaces may be constructed from one SurfaceControl, but only one can be connected (e.g. have an active EGL context) at a time.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `from` | [SurfaceControl](https://developer.android.com/reference/kotlin/android/view/SurfaceControl):The SurfaceControl to associate this Surface with This value cannot be`null`. |

## Public methods

### clearFrameRate

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clearFrameRate(): Unit
```

Clears the frame rate which was set for this surface.

This is equivalent to calling [setFrameRate(float,int,int)](https://developer.android.com/reference/kotlin/android/view/Surface#setFrameRate(kotlin.Float,%20kotlin.Int,%20kotlin.Int))using`0`for`frameRate`.

Note that this only has an effect for surfaces presented on the display. If this surface is consumed by something other than the system compositor, e.g. a media codec, this call has no effect. 
**See Also**

- [#setFrameRate(float, int, int)](https://developer.android.com/reference/kotlin/android/view/Surface#setFrameRate(kotlin.Float,%20kotlin.Int,%20kotlin.Int)) 

### describeContents

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### isValid

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isValid(): Boolean
```

Returns true if this object holds a valid surface.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if it holds a physical surface, so lockCanvas() will succeed. Otherwise returns false. |

### lockCanvas

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun lockCanvas(inOutDirty: Rect!): Canvas!
```

Gets a [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#) for drawing into this surface. After drawing into the provided [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#), the caller must invoke [unlockCanvasAndPost](https://developer.android.com/reference/kotlin/android/view/Surface#unlockCanvasAndPost(android.graphics.Canvas))to post the new contents to the surface.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `inOutDirty` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)!:A rectangle that represents the dirty region that the caller wants to redraw. This function may choose to expand the dirty rectangle if for example the surface has been resized or if the previous contents of the surface were not available. The caller must redraw the entire dirty region as represented by the contents of the inOutDirty rectangle upon return from this function. The caller may also pass`null`instead, in the case where the entire surface should be redrawn. |

| Return ||
|-----------------------------------------------------------------------------------------|----------------------------------------|
| [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#)! | A canvas for drawing into the surface. |

| Exceptions ||
|------------------------------------------------|-------------------------------------------|
| `java.lang.IllegalArgumentException` | If the inOutDirty rectangle is not valid. |
| `android.view.Surface.OutOfResourcesException` | If the canvas cannot be locked. |

### lockHardwareCanvas

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun lockHardwareCanvas(): Canvas!
```

Gets a [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#) for drawing into this surface. After drawing into the provided [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#), the caller must invoke [unlockCanvasAndPost](https://developer.android.com/reference/kotlin/android/view/Surface#unlockCanvasAndPost(android.graphics.Canvas))to post the new contents to the surface. Unlike [lockCanvas(android.graphics.Rect)](https://developer.android.com/reference/kotlin/android/view/Surface#lockCanvas(android.graphics.Rect))this will return a hardware-accelerated canvas. See the [unsupported drawing operations](https://developer.android.com/guide/topics/graphics/hardware-accel.html#unsupported) for a list of what is and isn't supported in a hardware-accelerated canvas. It is also required to fully cover the surface every time [lockHardwareCanvas()](https://developer.android.com/reference/kotlin/android/view/Surface#lockHardwareCanvas())is called as the buffer is not preserved between frames. Partial updates are not supported.

| Return ||
|-----------------------------------------------------------------------------------------|----------------------------------------|
| [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#)! | A canvas for drawing into the surface. |

| Exceptions ||
|-----------------------------------|---------------------------------|
| `java.lang.IllegalStateException` | If the canvas cannot be locked. |

### readFromParcel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun readFromParcel(source: Parcel!): Unit
```  

### release

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun release(): Unit
```

Release the local reference to the server-side surface. Always call release() when you're done with a Surface. This will make the surface invalid. 

### setFrameRate

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setFrameRate(
    frameRate: Float, 
    compatibility: Int
): Unit
```

Sets the intended frame rate for this surface. Any switching of refresh rates is most probably going to be seamless.

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `frameRate` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Value is 0.0f or greater |
| `compatibility` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.view.Surface#FRAME_RATE_COMPATIBILITY_DEFAULT](https://developer.android.com/reference/kotlin/android/view/Surface#FRAME_RATE_COMPATIBILITY_DEFAULT:kotlin.Int), [android.view.Surface#FRAME_RATE_COMPATIBILITY_FIXED_SOURCE](https://developer.android.com/reference/kotlin/android/view/Surface#FRAME_RATE_COMPATIBILITY_FIXED_SOURCE:kotlin.Int), [android.view.Surface#FRAME_RATE_COMPATIBILITY_AT_LEAST](https://developer.android.com/reference/kotlin/android/view/Surface#FRAME_RATE_COMPATIBILITY_AT_LEAST:kotlin.Int), android.view.Surface.FRAME_RATE_COMPATIBILITY_EXACT, or android.view.Surface.FRAME_RATE_COMPATIBILITY_MIN |

**See Also**

- [#setFrameRate(float, int, int)](https://developer.android.com/reference/kotlin/android/view/Surface#setFrameRate(kotlin.Float,%20kotlin.Int,%20kotlin.Int)) 

### setFrameRate

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setFrameRate(
    frameRate: Float, 
    compatibility: Int, 
    changeFrameRateStrategy: Int
): Unit
```

Sets the intended frame rate for this surface.

On devices that are capable of running the display at different refresh rates, the system may choose a display refresh rate to better match this surface's frame rate. Usage of this API won't introduce frame rate throttling, or affect other aspects of the application's frame production pipeline. However, because the system may change the display refresh rate, calls to this function may result in changes to Choreographer callback timings, and changes to the time interval at which the system releases buffers back to the application.

Note that this only has an effect for surfaces presented on the display. If this surface is consumed by something other than the system compositor, e.g. a media codec, this call has no effect.

| Parameters ||
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `frameRate` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The intended frame rate of this surface, in frames per second. 0 is a special value that indicates the app will accept the system's choice for the display frame rate, which is the default behavior if this function isn't called. The`frameRate`parameter does*not*need to be a valid refresh rate for this device's display - e.g., it's fine to pass 30fps to a device that can only run the display at 60fps. Value is 0.0f or greater |
| `compatibility` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The frame rate compatibility of this surface. The compatibility value may influence the system's choice of display frame rate. This parameter is ignored when`frameRate`is 0. Value is [android.view.Surface#FRAME_RATE_COMPATIBILITY_DEFAULT](https://developer.android.com/reference/kotlin/android/view/Surface#FRAME_RATE_COMPATIBILITY_DEFAULT:kotlin.Int), [android.view.Surface#FRAME_RATE_COMPATIBILITY_FIXED_SOURCE](https://developer.android.com/reference/kotlin/android/view/Surface#FRAME_RATE_COMPATIBILITY_FIXED_SOURCE:kotlin.Int), [android.view.Surface#FRAME_RATE_COMPATIBILITY_AT_LEAST](https://developer.android.com/reference/kotlin/android/view/Surface#FRAME_RATE_COMPATIBILITY_AT_LEAST:kotlin.Int), android.view.Surface.FRAME_RATE_COMPATIBILITY_EXACT, or android.view.Surface.FRAME_RATE_COMPATIBILITY_MIN |
| `changeFrameRateStrategy` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Whether display refresh rate transitions caused by this surface should be seamless. A seamless transition is one that doesn't have any visual interruptions, such as a black screen for a second or two. This parameter is ignored when`frameRate`is 0. Value is [android.view.Surface#CHANGE_FRAME_RATE_ONLY_IF_SEAMLESS](https://developer.android.com/reference/kotlin/android/view/Surface#CHANGE_FRAME_RATE_ONLY_IF_SEAMLESS:kotlin.Int), or [android.view.Surface#CHANGE_FRAME_RATE_ALWAYS](https://developer.android.com/reference/kotlin/android/view/Surface#CHANGE_FRAME_RATE_ALWAYS:kotlin.Int) |
| --- | --- |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If`frameRate`,`compatibility`or`changeFrameRateStrategy`are invalid. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/view/Surface#clearFrameRate()> 

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### unlockCanvas

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun unlockCanvas(canvas: Canvas!): Unit
```

**Deprecated:** *This API has been removed and is not supported. Do not use.* 

### unlockCanvasAndPost

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun unlockCanvasAndPost(canvas: Canvas!): Unit
```

Posts the new contents of the [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#) to the surface and releases the [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#).

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `canvas` | [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#)!:The canvas previously obtained from [lockCanvas](https://developer.android.com/reference/kotlin/android/view/Surface#lockCanvas(android.graphics.Rect)). |

### writeToParcel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Protected methods

### finalize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun finalize(): Unit
```

| Exceptions ||
|-----------------------|-------------------------------------|
| `java.lang.Throwable` | the`Exception`raised by this method |

## Properties

### CREATOR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<Surface!>
```
