# OverlayProperties

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OverlayProperties

Kotlin| [Java](../android/hardware/OverlayProperties.md) 
| --- | --- |

```
class OverlayProperties : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.hardware.OverlayProperties](../android/hardware/OverlayProperties.md) |

Provides supported overlay properties of the device.

Hardware overlay is a technique to composite different buffers directly to the screen using display hardware rather than the GPU. The system compositor is able to assign any content managed by a [android.view.SurfaceControl](../android/view/SurfaceControl.md) onto a hardware overlay if possible. Applications may be interested in the display hardware capabilities exposed by this class as a hint to determine if their [android.view.SurfaceControl](../android/view/SurfaceControl.md) tree is power-efficient and performant.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/hardware/OverlayProperties.md))`()` <br /> |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [LutProperties](../android/hardware/LutProperties.md)!\> | [getLutProperties](../android/hardware/OverlayProperties.md))`()` Returns the lut properties of the device. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCombinationSupported](../android/hardware/OverlayProperties.md))`(`dataspace:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `format:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Indicates that hardware composition of a buffer encoded with the provided [DataSpace](../android/hardware/DataSpace.md) and android. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isMixedColorSpacesSupported](../android/hardware/OverlayProperties.md))`()` Indicates that hardware composition of two or more overlays with different colorspaces is supported on the device. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/hardware/OverlayProperties.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [OverlayProperties](../android/hardware/OverlayProperties.md)!\> | [CREATOR](../android/hardware/OverlayProperties.md) <br /> |

## Public methods

### describeContents

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### getLutProperties

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLutProperties(): Array<LutProperties!>
```

Returns the lut properties of the device.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [LutProperties](../android/hardware/LutProperties.md)!> | This value cannot be`null`. |

### isCombinationSupported

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isCombinationSupported(
    dataspace: Int, 
    format: Int
): Boolean
```

Indicates that hardware composition of a buffer encoded with the provided [DataSpace](../android/hardware/DataSpace.md) and android.hardware.HardwareBuffer.Format is supported on the device.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dataspace` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is either`0`or a combination of [android.hardware.DataSpace#DATASPACE_UNKNOWN](../android/hardware/DataSpace.md), [android.hardware.DataSpace#DATASPACE_SCRGB_LINEAR](../android/hardware/DataSpace.md), [android.hardware.DataSpace#DATASPACE_SRGB](../android/hardware/DataSpace.md), [android.hardware.DataSpace#DATASPACE_SCRGB](../android/hardware/DataSpace.md), [android.hardware.DataSpace#DATASPACE_DISPLAY_P3](../android/hardware/DataSpace.md), [android.hardware.DataSpace#DATASPACE_BT2020_HLG](../android/hardware/DataSpace.md), [android.hardware.DataSpace#DATASPACE_BT2020_PQ](../android/hardware/DataSpace.md), [android.hardware.DataSpace#DATASPACE_ADOBE_RGB](../android/hardware/DataSpace.md), [android.hardware.DataSpace#DATASPACE_JFIF](../android/hardware/DataSpace.md), [android.hardware.DataSpace#DATASPACE_BT601_625](../android/hardware/DataSpace.md), [android.hardware.DataSpace#DATASPACE_BT601_525](../android/hardware/DataSpace.md), [android.hardware.DataSpace#DATASPACE_BT2020](../android/hardware/DataSpace.md), [android.hardware.DataSpace#DATASPACE_BT709](../android/hardware/DataSpace.md), [android.hardware.DataSpace#DATASPACE_DCI_P3](../android/hardware/DataSpace.md), and [android.hardware.DataSpace#DATASPACE_SRGB_LINEAR](../android/hardware/DataSpace.md) |
| `format` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.hardware.HardwareBuffer#RGBA_8888](../android/hardware/HardwareBuffer.md), [android.hardware.HardwareBuffer#RGBA_FP16](../android/hardware/HardwareBuffer.md), [android.hardware.HardwareBuffer#RGBA_1010102](../android/hardware/HardwareBuffer.md), [android.hardware.HardwareBuffer#RGBX_8888](../android/hardware/HardwareBuffer.md), [android.hardware.HardwareBuffer#RGB_888](../android/hardware/HardwareBuffer.md), [android.hardware.HardwareBuffer#RGB_565](../android/hardware/HardwareBuffer.md), [android.hardware.HardwareBuffer#BLOB](../android/hardware/HardwareBuffer.md), [android.hardware.HardwareBuffer#YCBCR_420_888](../android/hardware/HardwareBuffer.md), [android.hardware.HardwareBuffer#D_16](../android/hardware/HardwareBuffer.md), [android.hardware.HardwareBuffer#D_24](../android/hardware/HardwareBuffer.md), [android.hardware.HardwareBuffer#DS_24UI8](../android/hardware/HardwareBuffer.md), [android.hardware.HardwareBuffer#D_FP32](../android/hardware/HardwareBuffer.md), [android.hardware.HardwareBuffer#DS_FP32UI8](../android/hardware/HardwareBuffer.md), [android.hardware.HardwareBuffer#S_UI8](../android/hardware/HardwareBuffer.md), [android.hardware.HardwareBuffer#YCBCR_P010](../android/hardware/HardwareBuffer.md), [android.hardware.HardwareBuffer#YCBCR_P210](../android/hardware/HardwareBuffer.md), [android.hardware.HardwareBuffer#R_8](../android/hardware/HardwareBuffer.md), [android.hardware.HardwareBuffer#R_16](../android/hardware/HardwareBuffer.md), [android.hardware.HardwareBuffer#RG_1616](../android/hardware/HardwareBuffer.md), [android.hardware.HardwareBuffer#RGBA_10101010](../android/hardware/HardwareBuffer.md), android.hardware.HardwareBuffer.R_12, android.hardware.HardwareBuffer.R_14, android.hardware.HardwareBuffer.RG_1212, android.hardware.HardwareBuffer.RG_1414, android.hardware.HardwareBuffer.RGBA_12121212, android.hardware.HardwareBuffer.RGBA_14141414, android.hardware.HardwareBuffer.BGRA_1010102, or android.hardware.HardwareBuffer.BGRX_1010102 |

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
| `dest` | [Parcel](../android/os/Parcel.md):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<OverlayProperties!>
```
