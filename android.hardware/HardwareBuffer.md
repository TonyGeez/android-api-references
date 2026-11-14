# HardwareBuffer

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# HardwareBuffer

Kotlin| [Java](HardwareBuffer.md) 
| --- | --- |

```
class HardwareBuffer : AutoCloseable, Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.hardware.HardwareBuffer](HardwareBuffer.md) |

HardwareBuffer wraps a native`AHardwareBuffer`object, which is a low-level object representing a memory buffer accessible by various hardware units. HardwareBuffer allows sharing buffers across different application processes. In particular, HardwareBuffers may be mappable to memory accessible to various hardware systems, such as the GPU, a sensor or context hub, or other auxiliary processing units. For more information, see the NDK documentation for`AHardwareBuffer`.

## Summary

| Constants ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BLOB](HardwareBuffer.md) Format: opaque format used for raw data transfer; must have a height of 1 |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DS_24UI8](HardwareBuffer.md) Format: 24 bits depth, 8 bits stencil |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DS_FP32UI8](HardwareBuffer.md) Format: 32 bits depth, 8 bits stencil |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [D_16](HardwareBuffer.md) Format: 16 bits depth |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [D_24](HardwareBuffer.md) Format: 24 bits depth |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [D_FP32](HardwareBuffer.md) Format: 32 bits depth |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RGBA_10101010](HardwareBuffer.md) Format: 10 bits each red, green, blue, alpha |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RGBA_1010102](HardwareBuffer.md) Format: 10 bits each red, green, blue, 2 bits alpha |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RGBA_8888](HardwareBuffer.md) Value is [android.hardware.HardwareBuffer#RGBA_8888](HardwareBuffer.md), [android.hardware.HardwareBuffer#RGBA_FP16](HardwareBuffer.md), [android.hardware.HardwareBuffer#RGBA_1010102](HardwareBuffer.md), [android.hardware.HardwareBuffer#RGBX_8888](HardwareBuffer.md), [android.hardware.HardwareBuffer#RGB_888](HardwareBuffer.md), [android.hardware.HardwareBuffer#RGB_565](HardwareBuffer.md), [android.hardware.HardwareBuffer#BLOB](HardwareBuffer.md), [android.hardware.HardwareBuffer#YCBCR_420_888](HardwareBuffer.md), [android.hardware.HardwareBuffer#D_16](HardwareBuffer.md), [android.hardware.HardwareBuffer#D_24](HardwareBuffer.md), [android.hardware.HardwareBuffer#DS_24UI8](HardwareBuffer.md), [android.hardware.HardwareBuffer#D_FP32](HardwareBuffer.md), [android.hardware.HardwareBuffer#DS_FP32UI8](HardwareBuffer.md), [android.hardware.HardwareBuffer#S_UI8](HardwareBuffer.md), [android.hardware.HardwareBuffer#YCBCR_P010](HardwareBuffer.md), [android.hardware.HardwareBuffer#YCBCR_P210](HardwareBuffer.md), [android.hardware.HardwareBuffer#R_8](HardwareBuffer.md), [android.hardware.HardwareBuffer#R_16](HardwareBuffer.md), [android.hardware.HardwareBuffer#RG_1616](HardwareBuffer.md), [android.hardware.HardwareBuffer#RGBA_10101010](HardwareBuffer.md), android. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RGBA_FP16](HardwareBuffer.md) Format: 16 bits each red, green, blue, alpha |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RGBX_8888](HardwareBuffer.md) Format: 8 bits each red, green, blue, alpha, alpha is always 0xFF |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RGB_565](HardwareBuffer.md) Format: 5 bits each red and blue, 6 bits green, no alpha |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RGB_888](HardwareBuffer.md) Format: 8 bits each red, green, blue, no alpha |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RG_1616](HardwareBuffer.md) Format: 16 bits each red, green. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [R_16](HardwareBuffer.md) Format: 16 bits red. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [R_8](HardwareBuffer.md) Format: 8 bits red |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [S_UI8](HardwareBuffer.md) Format: 8 bits stencil |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [USAGE_COMPOSER_OVERLAY](HardwareBuffer.md) The buffer will be used as a hardware composer overlay layer. |
| --- | --- |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [USAGE_CPU_READ_OFTEN](HardwareBuffer.md) Usage: The buffer will often be read by the CPU |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [USAGE_CPU_READ_RARELY](HardwareBuffer.md) Value is either`0`or a combination of [android.hardware.HardwareBuffer#USAGE_CPU_READ_RARELY](HardwareBuffer.md), [android.hardware.HardwareBuffer#USAGE_CPU_READ_OFTEN](HardwareBuffer.md), [android.hardware.HardwareBuffer#USAGE_CPU_WRITE_RARELY](HardwareBuffer.md), [android.hardware.HardwareBuffer#USAGE_CPU_WRITE_OFTEN](HardwareBuffer.md), [android.hardware.HardwareBuffer#USAGE_GPU_SAMPLED_IMAGE](HardwareBuffer.md), [android.hardware.HardwareBuffer#USAGE_GPU_COLOR_OUTPUT](HardwareBuffer.md), [android.hardware.HardwareBuffer#USAGE_COMPOSER_OVERLAY](HardwareBuffer.md), [android.hardware.HardwareBuffer#USAGE_PROTECTED_CONTENT](HardwareBuffer.md), [android.hardware.HardwareBuffer#USAGE_VIDEO_ENCODE](HardwareBuffer.md), [android.hardware.HardwareBuffer#USAGE_GPU_DATA_BUFFER](HardwareBuffer.md), [android.hardware.HardwareBuffer#USAGE_SENSOR_DIRECT_DATA](HardwareBuffer.md), [android.hardware.HardwareBuffer#USAGE_GPU_CUBE_MAP](HardwareBuffer.md), [android.hardware.HardwareBuffer#USAGE_GPU_MIPMAP_COMPLETE](HardwareBuffer.md), and [android.hardware.HardwareBuffer#USAGE_FRONT_BUFFER](HardwareBuffer.md) |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [USAGE_CPU_WRITE_OFTEN](HardwareBuffer.md) Usage: The buffer will often be written to by the CPU |
| --- | --- |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [USAGE_CPU_WRITE_RARELY](HardwareBuffer.md) Usage: The buffer will sometimes be written to by the CPU |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [USAGE_FRONT_BUFFER](HardwareBuffer.md) Usage: The buffer is used for front-buffer rendering. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [USAGE_GPU_COLOR_OUTPUT](HardwareBuffer.md) Usage: The buffer will be written to by the GPU |
| --- | --- |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [USAGE_GPU_CUBE_MAP](HardwareBuffer.md) Usage: The buffer will be used as a cube map texture |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [USAGE_GPU_DATA_BUFFER](HardwareBuffer.md) Usage: The buffer will be used as a shader storage or uniform buffer object |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [USAGE_GPU_MIPMAP_COMPLETE](HardwareBuffer.md) Usage: The buffer contains a complete mipmap hierarchy |
| --- | --- |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [USAGE_GPU_SAMPLED_IMAGE](HardwareBuffer.md) Usage: The buffer will be read from by the GPU |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [USAGE_PROTECTED_CONTENT](HardwareBuffer.md) Usage: The buffer must not be used outside of a protected hardware path |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [USAGE_SENSOR_DIRECT_DATA](HardwareBuffer.md) Usage: The buffer will be used for sensor direct data |
| --- | --- |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [USAGE_VIDEO_ENCODE](HardwareBuffer.md) Usage: The buffer will be read by a hardware video encoder |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [YCBCR_420_888](HardwareBuffer.md) Format: Planar YCbCr 420; must have an even width and height |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [YCBCR_P010](HardwareBuffer.md) Android YUV P010 format. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [YCBCR_P210](HardwareBuffer.md) Android YUV P210 format. |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](HardwareBuffer.md))`()` Destroys this buffer immediately. |
| static [HardwareBuffer](HardwareBuffer.md) | [create](HardwareBuffer.md))`(`width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `height:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `format:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `layers:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `usage:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Creates a new`HardwareBuffer`instance. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](HardwareBuffer.md))`()` <br /> |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getFormat](HardwareBuffer.md))`()` Returns the @Format of this buffer. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getHeight](HardwareBuffer.md))`()` Returns the height of this buffer in pixels. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getId](HardwareBuffer.md))`()` Returns the system-wide unique id for this buffer This can be useful as a cache key for associating additional objects with a given HardwareBuffer, such as associating an imported EGLImage with the target HardwareBuffer when processing a stream of buffers from ImageReader. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLayers](HardwareBuffer.md))`()` Returns the number of layers in this buffer. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getUsage](HardwareBuffer.md))`()` Returns the usage flags of the usage hints set on this buffer. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getWidth](HardwareBuffer.md))`()` Returns the width of this buffer in pixels. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isClosed](HardwareBuffer.md))`()` Indicates whether this buffer has been closed. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSupported](HardwareBuffer.md))`(`width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `height:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `format:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `layers:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `usage:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Queries whether the given buffer description is supported by the system. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](HardwareBuffer.md))`(`dest:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |
| --- | --- |

| Protected methods ||
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](HardwareBuffer.md))`()` <br /> |

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [HardwareBuffer](HardwareBuffer.md)!\> | [CREATOR](HardwareBuffer.md) <br /> |

## Constants

### BLOB

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BLOB: Int
```

Format: opaque format used for raw data transfer; must have a height of 1 

 Value: 33

### DS_24UI8

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DS_24UI8: Int
```

Format: 24 bits depth, 8 bits stencil 

 Value: 50

### DS_FP32UI8

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DS_FP32UI8: Int
```

Format: 32 bits depth, 8 bits stencil 

 Value: 52

### D_16

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val D_16: Int
```

Format: 16 bits depth 

 Value: 48

### D_24

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val D_24: Int
```

Format: 24 bits depth 

 Value: 49

### D_FP32

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val D_FP32: Int
```

Format: 32 bits depth 

 Value: 51

### RGBA_10101010

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RGBA_10101010: Int
```

Format: 10 bits each red, green, blue, alpha 

 Value: 59

### RGBA_1010102

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RGBA_1010102: Int
```

Format: 10 bits each red, green, blue, 2 bits alpha 

 Value: 43

### RGBA_8888

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RGBA_8888: Int
```

Value is [android.hardware.HardwareBuffer#RGBA_8888](HardwareBuffer.md), [android.hardware.HardwareBuffer#RGBA_FP16](HardwareBuffer.md), [android.hardware.HardwareBuffer#RGBA_1010102](HardwareBuffer.md), [android.hardware.HardwareBuffer#RGBX_8888](HardwareBuffer.md), [android.hardware.HardwareBuffer#RGB_888](HardwareBuffer.md), [android.hardware.HardwareBuffer#RGB_565](HardwareBuffer.md), [android.hardware.HardwareBuffer#BLOB](HardwareBuffer.md), [android.hardware.HardwareBuffer#YCBCR_420_888](HardwareBuffer.md), [android.hardware.HardwareBuffer#D_16](HardwareBuffer.md), [android.hardware.HardwareBuffer#D_24](HardwareBuffer.md), [android.hardware.HardwareBuffer#DS_24UI8](HardwareBuffer.md), [android.hardware.HardwareBuffer#D_FP32](HardwareBuffer.md), [android.hardware.HardwareBuffer#DS_FP32UI8](HardwareBuffer.md), [android.hardware.HardwareBuffer#S_UI8](HardwareBuffer.md), [android.hardware.HardwareBuffer#YCBCR_P010](HardwareBuffer.md), [android.hardware.HardwareBuffer#YCBCR_P210](HardwareBuffer.md), [android.hardware.HardwareBuffer#R_8](HardwareBuffer.md), [android.hardware.HardwareBuffer#R_16](HardwareBuffer.md), [android.hardware.HardwareBuffer#RG_1616](HardwareBuffer.md), [android.hardware.HardwareBuffer#RGBA_10101010](HardwareBuffer.md), android.hardware.HardwareBuffer.R_12, android.hardware.HardwareBuffer.R_14, android.hardware.HardwareBuffer.RG_1212, android.hardware.HardwareBuffer.RG_1414, android.hardware.HardwareBuffer.RGBA_12121212, android.hardware.HardwareBuffer.RGBA_14141414, android.hardware.HardwareBuffer.BGRA_1010102, or android.hardware.HardwareBuffer.BGRX_1010102 

 Value: 1

### RGBA_FP16

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RGBA_FP16: Int
```

Format: 16 bits each red, green, blue, alpha 

 Value: 22

### RGBX_8888

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RGBX_8888: Int
```

Format: 8 bits each red, green, blue, alpha, alpha is always 0xFF 

 Value: 2

### RGB_565

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RGB_565: Int
```

Format: 5 bits each red and blue, 6 bits green, no alpha 

 Value: 4

### RGB_888

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RGB_888: Int
```

Format: 8 bits each red, green, blue, no alpha 

 Value: 3

### RG_1616

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RG_1616: Int
```

Format: 16 bits each red, green. When sampled on the GPU this is represented as an unsigned integer instead of implicit unsigned normalize. For more information see https://www.khronos.org/opengl/wiki/Normalized_Integer 

 Value: 58

### R_16

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val R_16: Int
```

Format: 16 bits red. When sampled on the GPU this is represented as an unsigned integer instead of implicit unsigned normalize. For more information see https://www.khronos.org/opengl/wiki/Normalized_Integer 

 Value: 57

### R_8

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val R_8: Int
```

Format: 8 bits red 

 Value: 56

### S_UI8

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val S_UI8: Int
```

Format: 8 bits stencil 

 Value: 53

### USAGE_COMPOSER_OVERLAY

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USAGE_COMPOSER_OVERLAY: Long
```

The buffer will be used as a hardware composer overlay layer. That is, it will be displayed using the system compositor via [SurfaceControl](../android.view/SurfaceControl.md) This flag is currently only needed when using [android.view.SurfaceControl.Transaction#setBuffer(SurfaceControl, HardwareBuffer)](../android/view/SurfaceControl.Transaction.md))to set a buffer. In all other cases, the framework adds this flag internally to buffers that could be presented in a composer overlay. 

 Value: 2048L

### USAGE_CPU_READ_OFTEN

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USAGE_CPU_READ_OFTEN: Long
```

Usage: The buffer will often be read by the CPU 

 Value: 3L

### USAGE_CPU_READ_RARELY

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USAGE_CPU_READ_RARELY: Long
```

Value is either`0`or a combination of [android.hardware.HardwareBuffer#USAGE_CPU_READ_RARELY](HardwareBuffer.md), [android.hardware.HardwareBuffer#USAGE_CPU_READ_OFTEN](HardwareBuffer.md), [android.hardware.HardwareBuffer#USAGE_CPU_WRITE_RARELY](HardwareBuffer.md), [android.hardware.HardwareBuffer#USAGE_CPU_WRITE_OFTEN](HardwareBuffer.md), [android.hardware.HardwareBuffer#USAGE_GPU_SAMPLED_IMAGE](HardwareBuffer.md), [android.hardware.HardwareBuffer#USAGE_GPU_COLOR_OUTPUT](HardwareBuffer.md), [android.hardware.HardwareBuffer#USAGE_COMPOSER_OVERLAY](HardwareBuffer.md), [android.hardware.HardwareBuffer#USAGE_PROTECTED_CONTENT](HardwareBuffer.md), [android.hardware.HardwareBuffer#USAGE_VIDEO_ENCODE](HardwareBuffer.md), [android.hardware.HardwareBuffer#USAGE_GPU_DATA_BUFFER](HardwareBuffer.md), [android.hardware.HardwareBuffer#USAGE_SENSOR_DIRECT_DATA](HardwareBuffer.md), [android.hardware.HardwareBuffer#USAGE_GPU_CUBE_MAP](HardwareBuffer.md), [android.hardware.HardwareBuffer#USAGE_GPU_MIPMAP_COMPLETE](HardwareBuffer.md), and [android.hardware.HardwareBuffer#USAGE_FRONT_BUFFER](HardwareBuffer.md) 

 Value: 2L

### USAGE_CPU_WRITE_OFTEN

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USAGE_CPU_WRITE_OFTEN: Long
```

Usage: The buffer will often be written to by the CPU 

 Value: 48L

### USAGE_CPU_WRITE_RARELY

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USAGE_CPU_WRITE_RARELY: Long
```

Usage: The buffer will sometimes be written to by the CPU 

 Value: 32L

### USAGE_FRONT_BUFFER

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USAGE_FRONT_BUFFER: Long
```

Usage: The buffer is used for front-buffer rendering. When front-buffering rendering is specified, different usages may adjust their behavior as a result. For example, when used as USAGE_GPU_COLOR_OUTPUT the buffer will behave similar to a single-buffered window. When used with USAGE_COMPOSER_OVERLAY, the system will try to prioritize the buffer receiving an overlay plane \& avoid caching it in intermediate composition buffers. 

 Value: 4294967296L

### USAGE_GPU_COLOR_OUTPUT

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USAGE_GPU_COLOR_OUTPUT: Long
```

Usage: The buffer will be written to by the GPU 

 Value: 512L

### USAGE_GPU_CUBE_MAP

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USAGE_GPU_CUBE_MAP: Long
```

Usage: The buffer will be used as a cube map texture 

 Value: 33554432L

### USAGE_GPU_DATA_BUFFER

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USAGE_GPU_DATA_BUFFER: Long
```

Usage: The buffer will be used as a shader storage or uniform buffer object 

 Value: 16777216L

### USAGE_GPU_MIPMAP_COMPLETE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USAGE_GPU_MIPMAP_COMPLETE: Long
```

Usage: The buffer contains a complete mipmap hierarchy 

 Value: 67108864L

### USAGE_GPU_SAMPLED_IMAGE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USAGE_GPU_SAMPLED_IMAGE: Long
```

Usage: The buffer will be read from by the GPU 

 Value: 256L

### USAGE_PROTECTED_CONTENT

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USAGE_PROTECTED_CONTENT: Long
```

Usage: The buffer must not be used outside of a protected hardware path 

 Value: 16384L

### USAGE_SENSOR_DIRECT_DATA

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USAGE_SENSOR_DIRECT_DATA: Long
```

Usage: The buffer will be used for sensor direct data 

 Value: 8388608L

### USAGE_VIDEO_ENCODE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USAGE_VIDEO_ENCODE: Long
```

Usage: The buffer will be read by a hardware video encoder 

 Value: 65536L

### YCBCR_420_888

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val YCBCR_420_888: Int
```

Format: Planar YCbCr 420; must have an even width and height 

 Value: 35

### YCBCR_P010

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val YCBCR_P010: Int
```

Android YUV P010 format.
P010 is a 4:2:0 YCbCr semiplanar format comprised of a WxH Y plane followed by a Wx(H/2) CbCr plane. Each sample is represented by a 16-bit little-endian value, with the lower 6 bits set to zero. 

 Value: 54

### YCBCR_P210

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val YCBCR_P210: Int
```

Android YUV P210 format.
P210 is a 4:2:2 YCbCr semiplanar format comprised of a WxH Y plane followed by a WxH CbCr plane. Each sample is represented by a 16-bit little-endian value, with the lower 6 bits set to zero. 

 Value: 60

## Public methods

### close

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun close(): Unit
```

Destroys this buffer immediately. Calling this method frees up any underlying native resources. After calling this method, this buffer must not be used in any way.

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |

**See Also**

- <https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer#isClosed()> 

### create

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun create(
    width: Int, 
    height: Int, 
    format: Int, 
    layers: Int, 
    usage: Long
): HardwareBuffer
```

Creates a new`HardwareBuffer`instance.

Calling this method will throw an`IllegalStateException`if format is not a supported Format type.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The width in pixels of the buffer Value is 1 or greater |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The height in pixels of the buffer Value is 1 or greater |
| `format` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The @Format of each pixel Value is [android.hardware.HardwareBuffer#RGBA_8888](HardwareBuffer.md), [android.hardware.HardwareBuffer#RGBA_FP16](HardwareBuffer.md), [android.hardware.HardwareBuffer#RGBA_1010102](HardwareBuffer.md), [android.hardware.HardwareBuffer#RGBX_8888](HardwareBuffer.md), [android.hardware.HardwareBuffer#RGB_888](HardwareBuffer.md), [android.hardware.HardwareBuffer#RGB_565](HardwareBuffer.md), [android.hardware.HardwareBuffer#BLOB](HardwareBuffer.md), [android.hardware.HardwareBuffer#YCBCR_420_888](HardwareBuffer.md), [android.hardware.HardwareBuffer#D_16](HardwareBuffer.md), [android.hardware.HardwareBuffer#D_24](HardwareBuffer.md), [android.hardware.HardwareBuffer#DS_24UI8](HardwareBuffer.md), [android.hardware.HardwareBuffer#D_FP32](HardwareBuffer.md), [android.hardware.HardwareBuffer#DS_FP32UI8](HardwareBuffer.md), [android.hardware.HardwareBuffer#S_UI8](HardwareBuffer.md), [android.hardware.HardwareBuffer#YCBCR_P010](HardwareBuffer.md), [android.hardware.HardwareBuffer#YCBCR_P210](HardwareBuffer.md), [android.hardware.HardwareBuffer#R_8](HardwareBuffer.md), [android.hardware.HardwareBuffer#R_16](HardwareBuffer.md), [android.hardware.HardwareBuffer#RG_1616](HardwareBuffer.md), [android.hardware.HardwareBuffer#RGBA_10101010](HardwareBuffer.md), android.hardware.HardwareBuffer.R_12, android.hardware.HardwareBuffer.R_14, android.hardware.HardwareBuffer.RG_1212, android.hardware.HardwareBuffer.RG_1414, android.hardware.HardwareBuffer.RGBA_12121212, android.hardware.HardwareBuffer.RGBA_14141414, android.hardware.HardwareBuffer.BGRA_1010102, or android.hardware.HardwareBuffer.BGRX_1010102 |
| --- | --- |
| `layers` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The number of layers in the buffer Value is 1 or greater |
| `usage` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The @Usage flags describing how the buffer will be used Value is either`0`or a combination of [android.hardware.HardwareBuffer#USAGE_CPU_READ_RARELY](HardwareBuffer.md), [android.hardware.HardwareBuffer#USAGE_CPU_READ_OFTEN](HardwareBuffer.md), [android.hardware.HardwareBuffer#USAGE_CPU_WRITE_RARELY](HardwareBuffer.md), [android.hardware.HardwareBuffer#USAGE_CPU_WRITE_OFTEN](HardwareBuffer.md), [android.hardware.HardwareBuffer#USAGE_GPU_SAMPLED_IMAGE](HardwareBuffer.md), [android.hardware.HardwareBuffer#USAGE_GPU_COLOR_OUTPUT](HardwareBuffer.md), [android.hardware.HardwareBuffer#USAGE_COMPOSER_OVERLAY](HardwareBuffer.md), [android.hardware.HardwareBuffer#USAGE_PROTECTED_CONTENT](HardwareBuffer.md), [android.hardware.HardwareBuffer#USAGE_VIDEO_ENCODE](HardwareBuffer.md), [android.hardware.HardwareBuffer#USAGE_GPU_DATA_BUFFER](HardwareBuffer.md), [android.hardware.HardwareBuffer#USAGE_SENSOR_DIRECT_DATA](HardwareBuffer.md), [android.hardware.HardwareBuffer#USAGE_GPU_CUBE_MAP](HardwareBuffer.md), [android.hardware.HardwareBuffer#USAGE_GPU_MIPMAP_COMPLETE](HardwareBuffer.md), and [android.hardware.HardwareBuffer#USAGE_FRONT_BUFFER](HardwareBuffer.md) |

| Return ||
|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [HardwareBuffer](HardwareBuffer.md) | A`HardwareBuffer`instance if successful, or throws an IllegalArgumentException if the dimensions passed are invalid (either zero, negative, or too large to allocate), if the format is not supported, if the requested number of layers is less than one or not supported, or if the passed usage flags are not a supported set. This value cannot be`null`. |

### describeContents

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) |

### getFormat

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFormat(): Int
```

Returns the @Format of this buffer.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.hardware.HardwareBuffer#RGBA_8888](HardwareBuffer.md), [android.hardware.HardwareBuffer#RGBA_FP16](HardwareBuffer.md), [android.hardware.HardwareBuffer#RGBA_1010102](HardwareBuffer.md), [android.hardware.HardwareBuffer#RGBX_8888](HardwareBuffer.md), [android.hardware.HardwareBuffer#RGB_888](HardwareBuffer.md), [android.hardware.HardwareBuffer#RGB_565](HardwareBuffer.md), [android.hardware.HardwareBuffer#BLOB](HardwareBuffer.md), [android.hardware.HardwareBuffer#YCBCR_420_888](HardwareBuffer.md), [android.hardware.HardwareBuffer#D_16](HardwareBuffer.md), [android.hardware.HardwareBuffer#D_24](HardwareBuffer.md), [android.hardware.HardwareBuffer#DS_24UI8](HardwareBuffer.md), [android.hardware.HardwareBuffer#D_FP32](HardwareBuffer.md), [android.hardware.HardwareBuffer#DS_FP32UI8](HardwareBuffer.md), [android.hardware.HardwareBuffer#S_UI8](HardwareBuffer.md), [android.hardware.HardwareBuffer#YCBCR_P010](HardwareBuffer.md), [android.hardware.HardwareBuffer#YCBCR_P210](HardwareBuffer.md), [android.hardware.HardwareBuffer#R_8](HardwareBuffer.md), [android.hardware.HardwareBuffer#R_16](HardwareBuffer.md), [android.hardware.HardwareBuffer#RG_1616](HardwareBuffer.md), [android.hardware.HardwareBuffer#RGBA_10101010](HardwareBuffer.md), android.hardware.HardwareBuffer.R_12, android.hardware.HardwareBuffer.R_14, android.hardware.HardwareBuffer.RG_1212, android.hardware.HardwareBuffer.RG_1414, android.hardware.HardwareBuffer.RGBA_12121212, android.hardware.HardwareBuffer.RGBA_14141414, android.hardware.HardwareBuffer.BGRA_1010102, or android.hardware.HardwareBuffer.BGRX_1010102 |

### getHeight

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getHeight(): Int
```

Returns the height of this buffer in pixels. 

### getId

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getId(): Long
```

Returns the system-wide unique id for this buffer This can be useful as a cache key for associating additional objects with a given HardwareBuffer, such as associating an imported EGLImage with the target HardwareBuffer when processing a stream of buffers from ImageReader. This can also be useful for doing cross-process buffer caching. As sending a HardwareBuffer over Binder is slower than sending a long, this can be used as reliable cache key after an initial handshake that passes the HardwareBuffers themselves to later be referred to using only the id. 

### getLayers

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLayers(): Int
```

Returns the number of layers in this buffer. 

### getUsage

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getUsage(): Long
```

Returns the usage flags of the usage hints set on this buffer. 

### getWidth

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getWidth(): Int
```

Returns the width of this buffer in pixels. 

### isClosed

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isClosed(): Boolean
```

Indicates whether this buffer has been closed. A closed buffer cannot be used in any way: the buffer cannot be written to a parcel, etc.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if this`HardwareBuffer`is in a closed state, false otherwise. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer#close()> 

### isSupported

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isSupported(
    width: Int, 
    height: Int, 
    format: Int, 
    layers: Int, 
    usage: Long
): Boolean
```

Queries whether the given buffer description is supported by the system. If this returns true, then the allocation may succeed until resource exhaustion occurs. If this returns false then this combination will never succeed.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The width in pixels of the buffer Value is 1 or greater |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The height in pixels of the buffer Value is 1 or greater |
| `format` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The @Format of each pixel Value is [android.hardware.HardwareBuffer#RGBA_8888](HardwareBuffer.md), [android.hardware.HardwareBuffer#RGBA_FP16](HardwareBuffer.md), [android.hardware.HardwareBuffer#RGBA_1010102](HardwareBuffer.md), [android.hardware.HardwareBuffer#RGBX_8888](HardwareBuffer.md), [android.hardware.HardwareBuffer#RGB_888](HardwareBuffer.md), [android.hardware.HardwareBuffer#RGB_565](HardwareBuffer.md), [android.hardware.HardwareBuffer#BLOB](HardwareBuffer.md), [android.hardware.HardwareBuffer#YCBCR_420_888](HardwareBuffer.md), [android.hardware.HardwareBuffer#D_16](HardwareBuffer.md), [android.hardware.HardwareBuffer#D_24](HardwareBuffer.md), [android.hardware.HardwareBuffer#DS_24UI8](HardwareBuffer.md), [android.hardware.HardwareBuffer#D_FP32](HardwareBuffer.md), [android.hardware.HardwareBuffer#DS_FP32UI8](HardwareBuffer.md), [android.hardware.HardwareBuffer#S_UI8](HardwareBuffer.md), [android.hardware.HardwareBuffer#YCBCR_P010](HardwareBuffer.md), [android.hardware.HardwareBuffer#YCBCR_P210](HardwareBuffer.md), [android.hardware.HardwareBuffer#R_8](HardwareBuffer.md), [android.hardware.HardwareBuffer#R_16](HardwareBuffer.md), [android.hardware.HardwareBuffer#RG_1616](HardwareBuffer.md), [android.hardware.HardwareBuffer#RGBA_10101010](HardwareBuffer.md), android.hardware.HardwareBuffer.R_12, android.hardware.HardwareBuffer.R_14, android.hardware.HardwareBuffer.RG_1212, android.hardware.HardwareBuffer.RG_1414, android.hardware.HardwareBuffer.RGBA_12121212, android.hardware.HardwareBuffer.RGBA_14141414, android.hardware.HardwareBuffer.BGRA_1010102, or android.hardware.HardwareBuffer.BGRX_1010102 |
| --- | --- |
| `layers` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The number of layers in the buffer Value is 1 or greater |
| `usage` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The @Usage flags describing how the buffer will be used Value is either`0`or a combination of [android.hardware.HardwareBuffer#USAGE_CPU_READ_RARELY](HardwareBuffer.md), [android.hardware.HardwareBuffer#USAGE_CPU_READ_OFTEN](HardwareBuffer.md), [android.hardware.HardwareBuffer#USAGE_CPU_WRITE_RARELY](HardwareBuffer.md), [android.hardware.HardwareBuffer#USAGE_CPU_WRITE_OFTEN](HardwareBuffer.md), [android.hardware.HardwareBuffer#USAGE_GPU_SAMPLED_IMAGE](HardwareBuffer.md), [android.hardware.HardwareBuffer#USAGE_GPU_COLOR_OUTPUT](HardwareBuffer.md), [android.hardware.HardwareBuffer#USAGE_COMPOSER_OVERLAY](HardwareBuffer.md), [android.hardware.HardwareBuffer#USAGE_PROTECTED_CONTENT](HardwareBuffer.md), [android.hardware.HardwareBuffer#USAGE_VIDEO_ENCODE](HardwareBuffer.md), [android.hardware.HardwareBuffer#USAGE_GPU_DATA_BUFFER](HardwareBuffer.md), [android.hardware.HardwareBuffer#USAGE_SENSOR_DIRECT_DATA](HardwareBuffer.md), [android.hardware.HardwareBuffer#USAGE_GPU_CUBE_MAP](HardwareBuffer.md), [android.hardware.HardwareBuffer#USAGE_GPU_MIPMAP_COMPLETE](HardwareBuffer.md), and [android.hardware.HardwareBuffer#USAGE_FRONT_BUFFER](HardwareBuffer.md) |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the combination is supported, false otherwise. |

### writeToParcel

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

Calling this method will throw an`IllegalStateException`if [close()](HardwareBuffer.md))has been previously called.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](../android.os/Parcel.md):The Parcel in which the object should be written. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md). |

## Protected methods

### finalize

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected fun finalize(): Unit
```

| Exceptions ||
|-----------------------|-------------------------------------|
| `java.lang.Throwable` | the`Exception`raised by this method |

## Properties

### CREATOR

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<HardwareBuffer!>
```
