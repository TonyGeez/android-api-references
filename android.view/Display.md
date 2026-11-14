# Display

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Display

Kotlin| [Java](../android/view/Display.md) 
| --- | --- |

```
class Display
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.Display](../android/view/Display.md) |

Provides information about the size and density of a logical display.

The display area is described in two different ways.

- The application display area specifies the part of the display that may contain an application window, excluding the system decorations. The application display area may be smaller than the real display area because the system subtracts the space needed for decor elements such as the status bar. Use [WindowMetrics.getBounds()](../android/view/WindowMetrics.md))to query the application window bounds.
- The real display area specifies the part of the display that is accessible to an application in the current system state. The real display area may be smaller than the physical size of the display in a few scenarios. Use [WindowManager.getCurrentWindowMetrics()](../android/view/WindowManager.md))to identify the current size of the activity window. UI-related work, such as choosing UI layouts, should rely upon [WindowMetrics.getBounds()](../android/view/WindowMetrics.md)). See [getRealSize](../android/view/Display.md))/ [getRealMetrics](../android/view/Display.md))for details.

<br />

A logical display does not necessarily represent a particular physical display device such as the internal display or an external display. The contents of a logical display may be presented on one or more physical displays according to the devices that are currently attached and whether mirroring has been enabled.

## Summary

| Nested classes ||
|---|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [HdrCapabilities](../android/view/Display.HdrCapabilities.md) Encapsulates the HDR capabilities of a given display. |
| | [Mode](../android/view/Display.Mode.md) A mode supported by a given display. |

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEFAULT_DISPLAY](../android/view/Display.md) The default Display id, which is the id of the primary display assuming there is one. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_PRESENTATION](../android/view/Display.md) Display flag: Indicates that the display is a presentation display. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_PRIVATE](../android/view/Display.md) Display flag: Indicates that the display is private. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_ROUND](../android/view/Display.md) Display flag: Indicates that the display has a round shape. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_SECURE](../android/view/Display.md) Display flag: Indicates that the display has a secure video output and supports compositing secure surfaces. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_SUPPORTS_PROTECTED_BUFFERS](../android/view/Display.md) Display flag: Indicates that the display supports compositing content that is stored in protected graphics buffers. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FRAME_RATE_CATEGORY_HIGH](../android/view/Display.md) High category determines the framework's recommended high frame rate. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FRAME_RATE_CATEGORY_NORMAL](../android/view/Display.md) Normal category determines the framework's recommended normal frame rate. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INVALID_DISPLAY](../android/view/Display.md) Invalid display id. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_DOZE](../android/view/Display.md) Display state: The display is dozing in a low power state; it is still on but is optimized for showing system-provided content while the device is non-interactive. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_DOZE_SUSPEND](../android/view/Display.md) Display state: The display is dozing in a suspended low power state; it is still on but the CPU is not updating it. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_OFF](../android/view/Display.md) Display state: The display is off. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_ON](../android/view/Display.md) Display state: The display is on. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_ON_SUSPEND](../android/view/Display.md) Display state: The display is in a suspended full power state; it is still on but the CPU is not updating it. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_UNKNOWN](../android/view/Display.md) Display state: The display state is unknown. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_VR](../android/view/Display.md) Display state: The display is on and optimized for VR mode. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getAppVsyncOffsetNanos](../android/view/Display.md))`()` Gets the app VSYNC offset, in nanoseconds. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getCurrentSizeRange](../android/view/Display.md))`(`outSmallestSize:` ` [Point](../android/graphics/Point.md)!`, `outLargestSize:` ` [Point](../android/graphics/Point.md)!`)` Return the range of display sizes an application can expect to encounter under normal operation, as long as there is no physical change in screen size. |
| [DisplayCutout](../android/view/DisplayCutout.md)? | [getCutout](../android/view/Display.md))`()` Returns the [DisplayCutout](../android/view/DisplayCutout.md), or`null`if there is none. |
| --- | --- |
| [DeviceProductInfo](../android/hardware/display/DeviceProductInfo.md)? | [getDeviceProductInfo](../android/view/Display.md))`()` Returns the product-specific information about the display or the directly connected device on the display chain. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDisplayId](../android/view/Display.md))`()` Gets the display id. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getFlags](../android/view/Display.md))`()` Returns a combination of flags that describe the capabilities of the display. |
| --- | --- |
| [Display.HdrCapabilities](../android/view/Display.HdrCapabilities.md)? | [getHdrCapabilities](../android/view/Display.md))`()` Returns the current display mode's HDR capabilities. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getHdrSdrRatio](../android/view/Display.md))`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getHeight](../android/view/Display.md))`()` <br /> |
| --- | --- |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getHighestHdrSdrRatio](../android/view/Display.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getMetrics](../android/view/Display.md))`(`outMetrics:` ` [DisplayMetrics](../android/util/DisplayMetrics.md)!`)` Gets the size and density of this display. |
| [Display.Mode](../android/view/Display.Mode.md)! | [getMode](../android/view/Display.md))`()` Returns the active mode of the display. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](../android/view/Display.md))`()` Gets the name of the display. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOrientation](../android/view/Display.md))`()` <br /> |
| [OverlayProperties](../android/hardware/OverlayProperties.md) | [getOverlaySupport](../android/view/Display.md))`()` Returns the [OverlayProperties](../android/hardware/OverlayProperties.md) of the display. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPixelFormat](../android/view/Display.md))`()` Gets the pixel format of the display. |
| [ColorSpace](../android/graphics/ColorSpace.md)? | [getPreferredWideGamutColorSpace](../android/view/Display.md))`()` Returns the preferred wide color space of the Display. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getPresentationDeadlineNanos](../android/view/Display.md))`()` This is how far in advance a buffer must be queued for presentation at a given time. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getRealMetrics](../android/view/Display.md))`(`outMetrics:` ` [DisplayMetrics](../android/util/DisplayMetrics.md)!`)` Gets the size of the largest region of the display accessible to an app in the current system state, without subtracting any window decor or applying scaling factors. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getRealSize](../android/view/Display.md))`(`outSize:` ` [Point](../android/graphics/Point.md)!`)` Gets the size of the largest region of the display accessible to an app in the current system state, without subtracting any window decor or applying scaling factors. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getRectSize](../android/view/Display.md))`(`outSize:` ` [Rect](../android/graphics/Rect.md)!`)` Gets the size of the display as a rectangle, in pixels. |
| --- | --- |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getRefreshRate](../android/view/Display.md))`()` Gets the refresh rate of this display in frames per second. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRotation](../android/view/Display.md))`()` Returns the rotation of the screen from its "natural" orientation. |
| [RoundedCorner](../android/view/RoundedCorner.md)? | [getRoundedCorner](../android/view/Display.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the [RoundedCorner](../android/view/RoundedCorner.md) of the given position if there is one. |
| --- | --- |
| [DisplayShape](../android/view/DisplayShape.md) | [getShape](../android/view/Display.md))`()` Returns the [DisplayShape](../android/view/DisplayShape.md) which is based on display coordinates. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getSize](../android/view/Display.md))`(`outSize:` ` [Point](../android/graphics/Point.md)!`)` Gets the size of the display in pixels. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getState](../android/view/Display.md))`()` Gets the state of the display, such as whether it is on or off. |
| --- | --- |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getSuggestedFrameRate](../android/view/Display.md))`(`category:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Gets the display-defined frame rate given a descriptive frame rate category. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Display.Mode](../android/view/Display.Mode.md)!\>! | [getSupportedModes](../android/view/Display.md))`()` Gets the supported modes of this display, might include synthetic modes |
| [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html) | [getSupportedRefreshRates](../android/view/Display.md))`()` Get the supported refresh rates of this display in frames per second. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getWidth](../android/view/Display.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasArrSupport](../android/view/Display.md))`()` Returns whether display supports adaptive refresh rate or not. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isHdr](../android/view/Display.md))`()` Returns whether this display supports any HDR type. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isHdrSdrRatioAvailable](../android/view/Display.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isInternal](../android/view/Display.md))`()` Check if this is a built-in display, i. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isMinimalPostProcessingSupported](../android/view/Display.md))`()` Returns true if the connected display can be switched into a mode with minimal post processing. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isValid](../android/view/Display.md))`()` Returns true if this display is still valid, false if the display has been removed. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isWideColorGamut](../android/view/Display.md))`()` Returns whether this display can be used to display wide color gamut content. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerHdrSdrRatioChangedListener](../android/view/Display.md))`(`executor:` ` [Executor](../java/util/concurrent/Executor.md)`, `listener:` ` [Consumer](../java/util/function/Consumer.md)< [Display](../android/view/Display.md)!>`)` Registers a listener that will be invoked whenever the display's hdr/sdr ratio has changed. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/view/Display.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterHdrSdrRatioChangedListener](../android/view/Display.md))`(`listener:` ` [Consumer](../java/util/function/Consumer.md)< [Display](../android/view/Display.md)!>`)` <br /> |

## Constants

### DEFAULT_DISPLAY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEFAULT_DISPLAY: Int
```

The default Display id, which is the id of the primary display assuming there is one. 

 Value: 0

### FLAG_PRESENTATION

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_PRESENTATION: Int
```

Display flag: Indicates that the display is a presentation display.

This flag identifies secondary displays that are suitable for use as presentation displays such as external or wireless displays. Applications may automatically project their content to presentation displays to provide richer second screen experiences. 

 Value: 8

**See Also**

- [#getFlags](../android/view/Display.md)) 

### FLAG_PRIVATE

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_PRIVATE: Int
```

Display flag: Indicates that the display is private. Only the application that owns the display and apps that are already on the display can create windows on it. 

 Value: 4

**See Also**

- [#getFlags](../android/view/Display.md)) 

### FLAG_ROUND

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_ROUND: Int
```

Display flag: Indicates that the display has a round shape.

This flag identifies displays that are circular, elliptical or otherwise do not permit the user to see all the way to the logical corners of the display. 

 Value: 16

**See Also**

- [#getFlags](../android/view/Display.md)) 

### FLAG_SECURE

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_SECURE: Int
```

Display flag: Indicates that the display has a secure video output and supports compositing secure surfaces.

If this flag is set then the display device has a secure video output and is capable of showing secure surfaces. It may also be capable of showing [protected buffers](../android/view/Display.md).

If this flag is not set then the display device may not have a secure video output; the user may see a blank region on the screen instead of the contents of secure surfaces or protected buffers.

Secure surfaces are used to prevent content rendered into those surfaces by applications from appearing in screenshots or from being viewed on non-secure displays. Protected buffers are used by secure video decoders for a similar purpose.

An application creates a window with a secure surface by specifying the [WindowManager.LayoutParams.FLAG_SECURE](../android/view/WindowManager.LayoutParams.md) window flag. Likewise, an application creates a [SurfaceView](../android/view/SurfaceView.md) with a secure surface by calling [SurfaceView.setSecure](../android/view/SurfaceView.md))before attaching the secure view to its containing window.

An application can use the absence of this flag as a hint that it should not create secure surfaces or protected buffers on this display because the content may not be visible. For example, if the flag is not set then the application may choose not to show content on this display, show an informative error message, select an alternate content stream or adopt a different strategy for decoding content that does not rely on secure surfaces or protected buffers. 

 Value: 2

**See Also**

- [#getFlags](../android/view/Display.md)) 

### FLAG_SUPPORTS_PROTECTED_BUFFERS

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_SUPPORTS_PROTECTED_BUFFERS: Int
```

Display flag: Indicates that the display supports compositing content that is stored in protected graphics buffers.

If this flag is set then the display device supports compositing protected buffers.

If this flag is not set then the display device may not support compositing protected buffers; the user may see a blank region on the screen instead of the protected content.

Secure (DRM) video decoders may allocate protected graphics buffers to request that a hardware-protected path be provided between the video decoder and the external display sink. If a hardware-protected path is not available, then content stored in protected graphics buffers may not be composited.

An application can use the absence of this flag as a hint that it should not use protected buffers for this display because the content may not be visible. For example, if the flag is not set then the application may choose not to show content on this display, show an informative error message, select an alternate content stream or adopt a different strategy for decoding content that does not rely on protected buffers. 

 Value: 1

**See Also**

- [#getFlags](../android/view/Display.md)) 

### FRAME_RATE_CATEGORY_HIGH

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FRAME_RATE_CATEGORY_HIGH: Int
```

High category determines the framework's recommended high frame rate. Opt for this high rate when a higher frame rate significantly enhances the user experience. 

 Value: 1

**See Also**

- [#getSuggestedFrameRate(int)](../android/view/Display.md))
- [#FRAME_RATE_CATEGORY_NORMAL](../android/view/Display.md) 

### FRAME_RATE_CATEGORY_NORMAL

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FRAME_RATE_CATEGORY_NORMAL: Int
```

Normal category determines the framework's recommended normal frame rate. Opt for this normal rate unless a higher frame rate significantly enhances the user experience. 

 Value: 0

**See Also**

- [#getSuggestedFrameRate(int)](../android/view/Display.md))
- [#FRAME_RATE_CATEGORY_HIGH](../android/view/Display.md) 

### INVALID_DISPLAY

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INVALID_DISPLAY: Int
```

Invalid display id. 

 Value: -1

### STATE_DOZE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_DOZE: Int
```

Display state: The display is dozing in a low power state; it is still on but is optimized for showing system-provided content while the device is non-interactive. 

 Value: 3

**See Also**

- [#getState](../android/view/Display.md))
- [android.os.PowerManager#isInteractive](../android/os/PowerManager.md)) 

### STATE_DOZE_SUSPEND

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_DOZE_SUSPEND: Int
```

Display state: The display is dozing in a suspended low power state; it is still on but the CPU is not updating it. This may be used in one of two ways: to show static system-provided content while the device is non-interactive, or to allow a "Sidekick" compute resource to update the display. For this reason, the CPU must not control the display in this mode. 

 Value: 4

**See Also**

- [#getState](../android/view/Display.md))
- [android.os.PowerManager#isInteractive](../android/os/PowerManager.md)) 

### STATE_OFF

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_OFF: Int
```

Display state: The display is off. 

 Value: 1

**See Also**

- [#getState](../android/view/Display.md)) 

### STATE_ON

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_ON: Int
```

Display state: The display is on. 

 Value: 2

**See Also**

- [#getState](../android/view/Display.md)) 

### STATE_ON_SUSPEND

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_ON_SUSPEND: Int
```

Display state: The display is in a suspended full power state; it is still on but the CPU is not updating it. This may be used in one of two ways: to show static system-provided content while the device is non-interactive, or to allow a "Sidekick" compute resource to update the display. For this reason, the CPU must not control the display in this mode. 

 Value: 6

**See Also**

- [#getState](../android/view/Display.md))
- [android.os.PowerManager#isInteractive](../android/os/PowerManager.md)) 

### STATE_UNKNOWN

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_UNKNOWN: Int
```

Display state: The display state is unknown. 

 Value: 0

**See Also**

- [#getState](../android/view/Display.md)) 

### STATE_VR

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_VR: Int
```

Display state: The display is on and optimized for VR mode. 

 Value: 5

**See Also**

- [#getState](../android/view/Display.md))
- [android.os.PowerManager#isInteractive](../android/os/PowerManager.md))

## Public methods

### getAppVsyncOffsetNanos

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAppVsyncOffsetNanos(): Long
```

Gets the app VSYNC offset, in nanoseconds. This is a positive value indicating the phase offset of the VSYNC events provided by Choreographer relative to the display refresh. For example, if Choreographer reports that the refresh occurred at time N, it actually occurred at (N - appVsyncOffset).

Apps generally do not need to be aware of this. It's only useful for fine-grained A/V synchronization. 

### getCurrentSizeRange

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCurrentSizeRange(
    outSmallestSize: Point!, 
    outLargestSize: Point!
): Unit
```

Return the range of display sizes an application can expect to encounter under normal operation, as long as there is no physical change in screen size. This is basically the sizes you will see as the orientation changes, taking into account whatever screen decoration there is in each rotation. For example, the status bar is always at the top of the screen, so it will reduce the height both in landscape and portrait, and the smallest height returned here will be the smaller of the two. This is intended for applications to get an idea of the range of sizes they will encounter while going through device rotations, to provide a stable UI through rotation. The sizes here take into account all standard system decorations that reduce the size actually available to the application: the status bar, navigation bar, system bar, etc. It does*not*take into account more transient elements like an IME soft keyboard.

| Parameters ||
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `outSmallestSize` | [Point](../android/graphics/Point.md)!:Filled in with the smallest width and height that the application will encounter, in pixels (not dp units). The x (width) dimension here directly corresponds to [Configuration.smallestScreenWidthDp](../android/content/res/Configuration.md), except the value here is in raw screen pixels rather than dp units. Your application may of course still get smaller space yet if, for example, a soft keyboard is being displayed. |
| `outLargestSize` | [Point](../android/graphics/Point.md)!:Filled in with the largest width and height that the application will encounter, in pixels (not dp units). Your application may of course still get larger space than this if, for example, screen decorations like the status bar are being hidden. |

### getCutout

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCutout(): DisplayCutout?
```

Returns the [DisplayCutout](../android/view/DisplayCutout.md), or`null`if there is none. 
**See Also**

- [android.view.DisplayCutout](../android/view/DisplayCutout.md) 

### getDeviceProductInfo

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDeviceProductInfo(): DeviceProductInfo?
```

Returns the product-specific information about the display or the directly connected device on the display chain. For example, if the display is transitively connected, this field may contain product information about the intermediate device. Returns`null`if product information is not available. 

### getDisplayId

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDisplayId(): Int
```

Gets the display id.

Each logical display has a unique id. The default display has id [DEFAULT_DISPLAY](../android/view/Display.md). 

### getFlags

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFlags(): Int
```

Returns a combination of flags that describe the capabilities of the display.

| Return ||
|----------------------------------------------------------------------------|--------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The display flags. |

**See Also**

- [#FLAG_SUPPORTS_PROTECTED_BUFFERS](../android/view/Display.md)
- [#FLAG_SECURE](../android/view/Display.md)
- [#FLAG_PRIVATE](../android/view/Display.md)
- [#FLAG_ROUND](../android/view/Display.md) 

### getHdrCapabilities

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getHdrCapabilities(): Display.HdrCapabilities?
```

Returns the current display mode's HDR capabilities.

| Return ||
|-----------------------------------------------------------------------------------------------------------------|--------------------------|
| [Display.HdrCapabilities](../android/view/Display.HdrCapabilities.md)? | This value may be`null`. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/view/Display#isHdr()> 

### getHdrSdrRatio

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getHdrSdrRatio(): Float
```

| Return ||
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | The current hdr/sdr ratio expressed as the ratio of targetHdrPeakBrightnessInNits / targetSdrWhitePointInNits. If [isHdrSdrRatioAvailable()](../android/view/Display.md))is false, this always returns 1.0f. |

### getHeight

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getHeight(): Int
```

**Deprecated:** *Use [WindowMetrics.getBounds()](../android/view/WindowMetrics.md))instead.* 

### getHighestHdrSdrRatio

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getHighestHdrSdrRatio(): Float
```

| Return ||
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | The highest possible HDR/SDR ratio. If [isHdrSdrRatioAvailable()](../android/view/Display.md))returns false, this method returns 1. |

### getMetrics

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMetrics(outMetrics: DisplayMetrics!): Unit
```

**Deprecated:** *Use [WindowMetrics.getBounds()](../android/view/WindowMetrics.md))to get the dimensions of the application window. Use [WindowMetrics.getDensity()](../android/view/WindowMetrics.md))to get the density of the application window.*

Gets the size and density of this display.

The size returned does not necessarily represent the actual size (native resolution) of the display. The returned size might be adjusted to exclude certain system decor elements that are always visible, or the size might be scaled to provide compatibility with older applications that were originally designed for smaller displays.

The returned size can also be different depending on the WindowManager associated with the display:

- If metrics are requested from an activity (either using a WindowManager accessed by`getWindowManager()`or`getSystemService(Context.WINDOW_SERVICE)`), the returned metrics provide the size of the current app window. As a result, in multi-window mode, the returned size can be smaller than the size of the device screen. System decoration handling may vary depending on API level:
 - API level 35 and above, the window size will be returned.
 - API level 34 and below, the window size minus system decoration areas and display cutout is returned.
- If metrics are requested from a non-activity context (for example, the application context, where the WindowManager is accessed by`getApplicationContext().getSystemService(Context.WINDOW_SERVICE)`), the returned size can vary depending on API level:
 - API level 29 and below --- The returned metrics provide the size of the entire display (based on current rotation) minus system decoration areas.
 - API level 30 and above --- The returned metrics provide the size of the top running activity in the current process. If the current process has no running activities, the metrics provide the size of the default display of the device, including system decoration areas.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `outMetrics` | [DisplayMetrics](../android/util/DisplayMetrics.md)!:A [DisplayMetrics](../android/util/DisplayMetrics.md) object which receives the display metrics. |

### getMode

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMode(): Display.Mode!
```

Returns the active mode of the display. 

### getName

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getName(): String!
```

Gets the name of the display.

Note that some displays may be renamed by the user.

| Return ||
|-----------------------------------------------------------------------------------|---------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The display's name. |

### getOrientation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getOrientation(): Int
```

**Deprecated:** *use [getRotation](../android/view/Display.md))*

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | orientation of this display. Value is [android.view.Surface#ROTATION_0](../android/view/Surface.md), [android.view.Surface#ROTATION_90](../android/view/Surface.md), [android.view.Surface#ROTATION_180](../android/view/Surface.md), or [android.view.Surface#ROTATION_270](../android/view/Surface.md) |

### getOverlaySupport

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getOverlaySupport(): OverlayProperties
```

Returns the [OverlayProperties](../android/hardware/OverlayProperties.md) of the display.

| Return ||
|--------------------------------------------------------------------------------------------------------------|-----------------------------|
| [OverlayProperties](../android/hardware/OverlayProperties.md) | This value cannot be`null`. |

### getPixelFormat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPixelFormat(): Int
```

**Deprecated:** *This method is no longer supported. The result is always [PixelFormat.RGBA_8888](../android/graphics/PixelFormat.md).*

Gets the pixel format of the display.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | One of the constants defined in [android.graphics.PixelFormat](../android/graphics/PixelFormat.md). |

### getPreferredWideGamutColorSpace

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPreferredWideGamutColorSpace(): ColorSpace?
```

Returns the preferred wide color space of the Display. The returned wide gamut color space is based on hardware capability and is preferred by the composition pipeline. Returns null if the display doesn't support wide color gamut. [Display.isWideColorGamut()](../android/view/Display.md)). 

### getPresentationDeadlineNanos

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPresentationDeadlineNanos(): Long
```

This is how far in advance a buffer must be queued for presentation at a given time. If you want a buffer to appear on the screen at time N, you must submit the buffer before (N - presentationDeadline).

The desired presentation time for GLES rendering may be set with [android.opengl.EGLExt#eglPresentationTimeANDROID](../android/opengl/EGLExt.md)). For video decoding, use [android.media.MediaCodec#releaseOutputBuffer(int, long)](../android/media/MediaCodec.md)). Times are expressed in nanoseconds, using the system monotonic clock ([System.nanoTime](../java/lang/System.md))). 

### getRealMetrics

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRealMetrics(outMetrics: DisplayMetrics!): Unit
```

**Deprecated:** *Use [WindowManager.getCurrentWindowMetrics()](../android/view/WindowManager.md))to identify the current size of the activity window. UI-related work, such as choosing UI layouts, should rely upon [WindowMetrics.getBounds()](../android/view/WindowMetrics.md)). Use [Configuration.densityDpi](../android/content/res/Configuration.md) to get the current density.*

Gets the size of the largest region of the display accessible to an app in the current system state, without subtracting any window decor or applying scaling factors.

The size is adjusted based on the current rotation of the display.

<br />

The returned size will fall into one of these scenarios:

1. The device has no partitions on the display. The returned value is the largest region of the display accessible to an app in the current system state, regardless of windowing mode.
2. The device divides a single display into multiple partitions. An application is restricted to a portion of the display. This is common in devices where the display changes size, such as foldables or large screens. The returned size will match the portion of the display the application is restricted to.
3. The window manager is emulating a different display size, using`adb shell wm size`. The returned size will match the emulated display size.

<br />

The returned value is**unsuitable to use when sizing and placing UI elements** , since it does not reflect the application window size in any of these scenarios. [WindowManager.getCurrentWindowMetrics()](../android/view/WindowManager.md))is an alternative that returns the size of the current application window, even if the window is on a device with a partitioned display. This helps prevent UI bugs where UI elements are misaligned or placed beyond the bounds of the window.

<br />

Handling multi-window mode correctly is necessary since applications are not always fullscreen. A user on a large screen device, such as a tablet or ChromeOS devices, is more likely to use multi-window modes.

<br />

For example, consider a device with a display partitioned into two halves. The user may have a fullscreen application open on the first partition. They may have two applications open in split screen (an example of multi-window mode) on the second partition, with each application consuming half of the partition. In this case, [WindowManager.getCurrentWindowMetrics()](../android/view/WindowManager.md))reports the fullscreen window is half of the screen in size, and each split screen window is a quarter of the screen in size. On the other hand, [getRealMetrics](../android/view/Display.md))reports half of the screen size for all windows, since the application windows are all restricted to their respective partitions.

<br />

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `outMetrics` | [DisplayMetrics](../android/util/DisplayMetrics.md)!:A [DisplayMetrics](../android/util/DisplayMetrics.md) object to receive the metrics. |

### getRealSize

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRealSize(outSize: Point!): Unit
```

**Deprecated:** *Use [WindowManager.getCurrentWindowMetrics()](../android/view/WindowManager.md))to identify the current size of the activity window. UI-related work, such as choosing UI layouts, should rely upon [WindowMetrics.getBounds()](../android/view/WindowMetrics.md)).*

Gets the size of the largest region of the display accessible to an app in the current system state, without subtracting any window decor or applying scaling factors.

The size is adjusted based on the current rotation of the display.

<br />

The returned size will fall into one of these scenarios:

1. The device has no partitions on the display. The returned value is the largest region of the display accessible to an app in the current system state, regardless of windowing mode.
2. The device divides a single display into multiple partitions. An application is restricted to a portion of the display. This is common in devices where the display changes size, such as foldables or large screens. The returned size will match the portion of the display the application is restricted to.
3. The window manager is emulating a different display size, using`adb shell wm size`. The returned size will match the emulated display size.

<br />

The returned value is**unsuitable to use when sizing and placing UI elements** , since it does not reflect the application window size in any of these scenarios. [WindowManager.getCurrentWindowMetrics()](../android/view/WindowManager.md))is an alternative that returns the size of the current application window, even if the window is on a device with a partitioned display. This helps prevent UI bugs where UI elements are misaligned or placed beyond the bounds of the window.

<br />

Handling multi-window mode correctly is necessary since applications are not always fullscreen. A user on a large screen device, such as a tablet or ChromeOS devices, is more likely to use multi-window modes.

<br />

For example, consider a device with a display partitioned into two halves. The user may have a fullscreen application open on the first partition. They may have two applications open in split screen (an example of multi-window mode) on the second partition, with each application consuming half of the partition. In this case, [WindowManager.getCurrentWindowMetrics()](../android/view/WindowManager.md))reports the fullscreen window is half of the screen in size, and each split screen window is a quarter of the screen in size. On the other hand, [getRealSize](../android/view/Display.md))reports half of the screen size for all windows, since the application windows are all restricted to their respective partitions.

<br />

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------|
| `outSize` | [Point](../android/graphics/Point.md)!:Set to the real size of the display. |

### getRectSize

Added in [API level 13](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRectSize(outSize: Rect!): Unit
```

**Deprecated:** *Use [WindowMetrics.getBounds()](../android/view/WindowMetrics.md))to get the dimensions of the application window.*

Gets the size of the display as a rectangle, in pixels.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `outSize` | [Rect](../android/graphics/Rect.md)!:A [Rect](../android/graphics/Rect.md) object to receive the size information. |

### getRefreshRate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRefreshRate(): Float
```

Gets the refresh rate of this display in frames per second. 

### getRotation

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRotation(): Int
```

Returns the rotation of the screen from its "natural" orientation. The returned value may be [Surface.ROTATION_0](../android/view/Surface.md)(no rotation), [Surface.ROTATION_90](../android/view/Surface.md), [Surface.ROTATION_180](../android/view/Surface.md), or [Surface.ROTATION_270](../android/view/Surface.md). For example, if a device has a naturally tall screen, and the user has turned it on its side to go into a landscape orientation, the value returned here may be either [Surface.ROTATION_90](../android/view/Surface.md) or [Surface.ROTATION_270](../android/view/Surface.md) depending on the direction it was turned. The angle is the rotation of the drawn graphics on the screen, which is the opposite direction of the physical rotation of the device. For example, if the device is rotated 90 degrees counter-clockwise, to compensate rendering will be rotated by 90 degrees clockwise and thus the returned value here will be [Surface.ROTATION_90](../android/view/Surface.md). This rotation value will match the results of [getMetrics](../android/view/Display.md)): this means that the rotation value will correspond to the activity if accessed through the activity.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.view.Surface#ROTATION_0](../android/view/Surface.md), [android.view.Surface#ROTATION_90](../android/view/Surface.md), [android.view.Surface#ROTATION_180](../android/view/Surface.md), or [android.view.Surface#ROTATION_270](../android/view/Surface.md) |

### getRoundedCorner

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRoundedCorner(position: Int): RoundedCorner?
```

Returns the [RoundedCorner](../android/view/RoundedCorner.md) of the given position if there is one.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `position` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the position of the rounded corner on the display. Value is [android.view.RoundedCorner#POSITION_TOP_LEFT](../android/view/RoundedCorner.md), [android.view.RoundedCorner#POSITION_TOP_RIGHT](../android/view/RoundedCorner.md), [android.view.RoundedCorner#POSITION_BOTTOM_RIGHT](../android/view/RoundedCorner.md), or [android.view.RoundedCorner#POSITION_BOTTOM_LEFT](../android/view/RoundedCorner.md) |

| Return ||
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [RoundedCorner](../android/view/RoundedCorner.md)? | the rounded corner of the given position. Returns`null`if there is none. |

### getShape

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getShape(): DisplayShape
```

Returns the [DisplayShape](../android/view/DisplayShape.md) which is based on display coordinates. To get the [DisplayShape](../android/view/DisplayShape.md) based on the window frame, use [WindowInsets.getDisplayShape()](../android/view/WindowInsets.md))instead.

| Return ||
|------------------------------------------------------------------------------------------|-----------------------------|
| [DisplayShape](../android/view/DisplayShape.md) | This value cannot be`null`. |

**See Also**

- [android.view.DisplayShape](../android/view/DisplayShape.md) 

### getSize

Added in [API level 13](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSize(outSize: Point!): Unit
```

**Deprecated:** *Use [WindowMetrics](../android/view/WindowMetrics.md) instead. Obtain a`WindowMetrics`instance by calling [WindowManager.getCurrentWindowMetrics()](../android/view/WindowManager.md)), then call [WindowMetrics.getBounds()](../android/view/WindowMetrics.md))to get the dimensions of the application window.*

Gets the size of the display in pixels.

The return value does not necessarily represent the actual size (native resolution) of the display. The returned size might be adjusted to exclude certain system decor elements that are always visible, or the size might be scaled to provide compatibility with older applications that were originally designed for smaller displays.

The returned size can also be different depending on the WindowManager bound to the display:

- If size is requested from an activity (either using a WindowManager accessed by`getWindowManager()`or`getSystemService(Context.WINDOW_SERVICE)`), the size of the current app window is returned. As a result, in multi-window mode, the returned size can be smaller than the size of the device screen. The returned window size can vary depending on API level:
 - API level 35 and above, the window size will be returned.
 - API level 34 and below, the window size minus system decoration areas and display cutout is returned.
- If size is requested from a non-activity context (for example, the application context, where the WindowManager is accessed by`getApplicationContext().getSystemService(Context.WINDOW_SERVICE)`), the returned size can vary depending on API level:
 - API level 29 and below --- The size of the entire display (based on current rotation) minus system decoration areas is returned.
 - API level 30 and above --- The size of the top running activity in the current process is returned, system decoration areas exclusion follows the behavior defined above, based on the caller's API level. If the current process has no running activities, the size of the device default display, including system decoration areas, is returned.

For layout purposes, apps should make a request from an activity context to obtain the size of the display area available for app content.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `outSize` | [Point](../android/graphics/Point.md)!:A [Point](../android/graphics/Point.md) object which receives the display size information. |

### getState

Added in [API level 20](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getState(): Int
```

Gets the state of the display, such as whether it is on or off.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The state of the display: one of [STATE_OFF](../android/view/Display.md), [STATE_ON](../android/view/Display.md), [STATE_DOZE](../android/view/Display.md), [STATE_DOZE_SUSPEND](../android/view/Display.md), [STATE_ON_SUSPEND](../android/view/Display.md), or [STATE_UNKNOWN](../android/view/Display.md). |

### getSuggestedFrameRate

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSuggestedFrameRate(category: Int): Float
```

Gets the display-defined frame rate given a descriptive frame rate category.

For example, an animation that does not require fast render rates can use the [FRAME_RATE_CATEGORY_NORMAL](../android/view/Display.md) to get the suggested frame rate. 

```kotlin
<code>float desiredMinRate = display.getSuggestedFrameRate(FRAME_RATE_CATEGORY_NORMAL);
   surface.setFrameRate(desiredMinRate, Surface.FRAME_RATE_COMPATIBILITY_DEFAULT);
  </code>
```

<br />

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `category` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):either [FRAME_RATE_CATEGORY_NORMAL](../android/view/Display.md) or [FRAME_RATE_CATEGORY_HIGH](../android/view/Display.md) Value is [android.view.Display#FRAME_RATE_CATEGORY_NORMAL](../android/view/Display.md), or [android.view.Display#FRAME_RATE_CATEGORY_HIGH](../android/view/Display.md) |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | when category is not [FRAME_RATE_CATEGORY_NORMAL](../android/view/Display.md) or [FRAME_RATE_CATEGORY_HIGH](../android/view/Display.md) |

**See Also**

- [android.view.Surface#setFrameRate(float, int)](../android/view/Surface.md)) 

### getSupportedModes

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSupportedModes(): Array<Display.Mode!>!
```

Gets the supported modes of this display, might include synthetic modes 

### getSupportedRefreshRates

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSupportedRefreshRates(): FloatArray
```

Get the supported refresh rates of this display in frames per second.

- Android version [Build.VERSION_CODES.BAKLAVA](../android/os/Build.VERSION_CODES.md) and above: returns display supported render rates.
- Android version [Build.VERSION_CODES.VANILLA_ICE_CREAM](../android/os/Build.VERSION_CODES.md) and below: This method only returns refresh rates for the display's default modes. For more options, use [getSupportedModes()](../android/view/Display.md)).

<br />

| Return ||
|-------------------------------------------------------------------------------------------|-----------------------------|
| [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html) | This value cannot be`null`. |

### getWidth

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getWidth(): Int
```

**Deprecated:** *Use [WindowMetrics.getBounds](../android/view/WindowMetrics.md))instead.* 

### hasArrSupport

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasArrSupport(): Boolean
```

Returns whether display supports adaptive refresh rate or not. 

### isHdr

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isHdr(): Boolean
```

Returns whether this display supports any HDR type. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/view/Display#getHdrCapabilities()>
- [android.view.Display.HdrCapabilities#getSupportedHdrTypes()](../android/view/Display.HdrCapabilities.md)) 

### isHdrSdrRatioAvailable

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isHdrSdrRatioAvailable(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Whether the display supports reporting an hdr/sdr ratio. If this is false, [getHdrSdrRatio()](../android/view/Display.md))will always be 1.0f |

### isInternal

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isInternal(): Boolean
```

Check if this is a built-in display, i.e. one that is physically part of the device rather than one connected via an external cable, or a Wi-Fi/Overlay/Virtual one. 

### isMinimalPostProcessingSupported

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isMinimalPostProcessingSupported(): Boolean
```

Returns true if the connected display can be switched into a mode with minimal post processing.

If the Display sink is connected via HDMI, this method will return true if the display supports either Auto Low Latency Mode or Game Content Type.

If the Display sink has an internal connection or uses some other protocol than HDMI, this method will return true if the sink can be switched into an implementation-defined low latency image processing mode.

The ability to switch to a mode with minimal post processing may be disabled by a user setting in the system settings menu. In that case, this method returns false. 
**See Also**

- [android.view.Window#setPreferMinimalPostProcessing](../android/view/Window.md)) 

### isValid

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isValid(): Boolean
```

Returns true if this display is still valid, false if the display has been removed. If the display is invalid, then the methods of this class will continue to report the most recently observed display information. However, it is unwise (and rather fruitless) to continue using a [Display](../android/view/Display.md) object after the display's demise. It's possible for a display that was previously invalid to become valid again if a display with the same id is reconnected.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the display is still valid. |

### isWideColorGamut

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isWideColorGamut(): Boolean
```

Returns whether this display can be used to display wide color gamut content. This does not necessarily mean the device itself can render wide color gamut content. To ensure wide color gamut content can be produced, refer to [Configuration.isScreenWideColorGamut()](../android/content/res/Configuration.md)). 

### registerHdrSdrRatioChangedListener

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun registerHdrSdrRatioChangedListener(
    executor: Executor, 
    listener: Consumer<Display!>
): Unit
```

Registers a listener that will be invoked whenever the display's hdr/sdr ratio has changed. After receiving the callback on the specified Executor, call [getHdrSdrRatio()](../android/view/Display.md))to get the updated value. If [isHdrSdrRatioAvailable()](../android/view/Display.md))is false, then an IllegalStateException will be thrown

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](../java/util/concurrent/Executor.md):The executor to invoke the listener on This value cannot be`null`. |
| `listener` | [Consumer](../java/util/function/Consumer.md)\< [Display](../android/view/Display.md)!\>:The listener to invoke when the HDR/SDR ratio changes This value cannot be`null`. |

| Exceptions ||
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if [isHdrSdrRatioAvailable()](../android/view/Display.md))is false |

**See Also**

- [#unregisterHdrSdrRatioChangedListener(Consumer)](../android/view/Display.md)) 

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### unregisterHdrSdrRatioChangedListener

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun unregisterHdrSdrRatioChangedListener(listener: Consumer<Display!>): Unit
```

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [Consumer](../java/util/function/Consumer.md)\< [Display](../android/view/Display.md)!\>:The previously [registered](../android/view/Display.md))hdr/sdr ratio listener to remove. This value cannot be`null`. |

**See Also**

- [#registerHdrSdrRatioChangedListener(Executor, Consumer)](../android/view/Display.md))
