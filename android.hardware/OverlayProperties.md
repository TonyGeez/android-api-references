# OverlayProperties

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OverlayProperties

Kotlin| [Java](https://developer.android.com/reference/android/hardware/OverlayProperties "View this page in Java") 
| --- | --- |

```
class OverlayProperties : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.hardware.OverlayProperties](https://developer.android.com/reference/kotlin/android/hardware/OverlayProperties#) |

Provides supported overlay properties of the device.

Hardware overlay is a technique to composite different buffers directly to the screen using display hardware rather than the GPU. The system compositor is able to assign any content managed by a [android.view.SurfaceControl](https://developer.android.com/reference/kotlin/android/view/SurfaceControl.html#) onto a hardware overlay if possible. Applications may be interested in the display hardware capabilities exposed by this class as a hint to determine if their [android.view.SurfaceControl](https://developer.android.com/reference/kotlin/android/view/SurfaceControl.html#) tree is power-efficient and performant.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/hardware/OverlayProperties#describeContents())`()` <br /> |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [LutProperties](https://developer.android.com/reference/kotlin/android/hardware/LutProperties)!\> | [getLutProperties](https://developer.android.com/reference/kotlin/android/hardware/OverlayProperties#getLutProperties())`()` Returns the lut properties of the device. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCombinationSupported](https://developer.android.com/reference/kotlin/android/hardware/OverlayProperties#isCombinationSupported(kotlin.Int,%20kotlin.Int))`(`dataspace:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `format:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Indicates that hardware composition of a buffer encoded with the provided [DataSpace](https://developer.android.com/reference/kotlin/android/hardware/DataSpace) and android. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isMixedColorSpacesSupported](https://developer.android.com/reference/kotlin/android/hardware/OverlayProperties#isMixedColorSpacesSupported())`()` Indicates that hardware composition of two or more overlays with different colorspaces is supported on the device. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/hardware/OverlayProperties#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [OverlayProperties](https://developer.android.com/reference/kotlin/android/hardware/OverlayProperties#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/hardware/OverlayProperties#CREATOR:android.os.Parcelable.Creator) <br /> |

## Public methods

### describeContents

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getLutProperties

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLutProperties(): Array<LutProperties!>
```

Returns the lut properties of the device.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [LutProperties](https://developer.android.com/reference/kotlin/android/hardware/LutProperties)!> | This value cannot be`null`. |

### isCombinationSupported

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isCombinationSupported(
    dataspace: Int, 
    format: Int
): Boolean
```

Indicates that hardware composition of a buffer encoded with the provided [DataSpace](https://developer.android.com/reference/kotlin/android/hardware/DataSpace) and android.hardware.HardwareBuffer.Format is supported on the device.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dataspace` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is either`0`or a combination of [android.hardware.DataSpace#DATASPACE_UNKNOWN](https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_UNKNOWN:kotlin.Int), [android.hardware.DataSpace#DATASPACE_SCRGB_LINEAR](https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_SCRGB_LINEAR:kotlin.Int), [android.hardware.DataSpace#DATASPACE_SRGB](https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_SRGB:kotlin.Int), [android.hardware.DataSpace#DATASPACE_SCRGB](https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_SCRGB:kotlin.Int), [android.hardware.DataSpace#DATASPACE_DISPLAY_P3](https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_DISPLAY_P3:kotlin.Int), [android.hardware.DataSpace#DATASPACE_BT2020_HLG](https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_BT2020_HLG:kotlin.Int), [android.hardware.DataSpace#DATASPACE_BT2020_PQ](https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_BT2020_PQ:kotlin.Int), [android.hardware.DataSpace#DATASPACE_ADOBE_RGB](https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_ADOBE_RGB:kotlin.Int), [android.hardware.DataSpace#DATASPACE_JFIF](https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_JFIF:kotlin.Int), [android.hardware.DataSpace#DATASPACE_BT601_625](https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_BT601_625:kotlin.Int), [android.hardware.DataSpace#DATASPACE_BT601_525](https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_BT601_525:kotlin.Int), [android.hardware.DataSpace#DATASPACE_BT2020](https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_BT2020:kotlin.Int), [android.hardware.DataSpace#DATASPACE_BT709](https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_BT709:kotlin.Int), [android.hardware.DataSpace#DATASPACE_DCI_P3](https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_DCI_P3:kotlin.Int), and [android.hardware.DataSpace#DATASPACE_SRGB_LINEAR](https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_SRGB_LINEAR:kotlin.Int) |
| `format` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.hardware.HardwareBuffer#RGBA_8888](https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer#RGBA_8888:kotlin.Int), [android.hardware.HardwareBuffer#RGBA_FP16](https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer#RGBA_FP16:kotlin.Int), [android.hardware.HardwareBuffer#RGBA_1010102](https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer#RGBA_1010102:kotlin.Int), [android.hardware.HardwareBuffer#RGBX_8888](https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer#RGBX_8888:kotlin.Int), [android.hardware.HardwareBuffer#RGB_888](https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer#RGB_888:kotlin.Int), [android.hardware.HardwareBuffer#RGB_565](https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer#RGB_565:kotlin.Int), [android.hardware.HardwareBuffer#BLOB](https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer#BLOB:kotlin.Int), [android.hardware.HardwareBuffer#YCBCR_420_888](https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer#YCBCR_420_888:kotlin.Int), [android.hardware.HardwareBuffer#D_16](https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer#D_16:kotlin.Int), [android.hardware.HardwareBuffer#D_24](https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer#D_24:kotlin.Int), [android.hardware.HardwareBuffer#DS_24UI8](https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer#DS_24UI8:kotlin.Int), [android.hardware.HardwareBuffer#D_FP32](https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer#D_FP32:kotlin.Int), [android.hardware.HardwareBuffer#DS_FP32UI8](https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer#DS_FP32UI8:kotlin.Int), [android.hardware.HardwareBuffer#S_UI8](https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer#S_UI8:kotlin.Int), [android.hardware.HardwareBuffer#YCBCR_P010](https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer#YCBCR_P010:kotlin.Int), [android.hardware.HardwareBuffer#YCBCR_P210](https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer#YCBCR_P210:kotlin.Int), [android.hardware.HardwareBuffer#R_8](https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer#R_8:kotlin.Int), [android.hardware.HardwareBuffer#R_16](https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer#R_16:kotlin.Int), [android.hardware.HardwareBuffer#RG_1616](https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer#RG_1616:kotlin.Int), [android.hardware.HardwareBuffer#RGBA_10101010](https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer#RGBA_10101010:kotlin.Int), android.hardware.HardwareBuffer.R_12, android.hardware.HardwareBuffer.R_14, android.hardware.HardwareBuffer.RG_1212, android.hardware.HardwareBuffer.RG_1414, android.hardware.HardwareBuffer.RGBA_12121212, android.hardware.HardwareBuffer.RGBA_14141414, android.hardware.HardwareBuffer.BGRA_1010102, or android.hardware.HardwareBuffer.BGRX_1010102 |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the device can support efficiently compositing the content described by the dataspace and format. False if GPU composition fallback is otherwise required. |

### isMixedColorSpacesSupported

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isMixedColorSpacesSupported(): Boolean
```

Indicates that hardware composition of two or more overlays with different colorspaces is supported on the device.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the device can support mixed colorspaces efficiently, false if GPU composition fallback is otherwise required. |

### writeToParcel

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<OverlayProperties!>
```
