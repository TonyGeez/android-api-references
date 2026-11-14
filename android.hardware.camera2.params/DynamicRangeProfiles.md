# DynamicRangeProfiles

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DynamicRangeProfiles

Kotlin| [Java](../android/hardware/camera2/params/DynamicRangeProfiles.md) 
| --- | --- |

```
class DynamicRangeProfiles
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.hardware.camera2.params.DynamicRangeProfiles](../android/hardware/camera2/params/DynamicRangeProfiles.md) |

Immutable class with information about supported 10-bit dynamic range profiles.

An instance of this class can be queried by retrieving the value of [android.hardware.camera2.CameraCharacteristics#REQUEST_AVAILABLE_DYNAMIC_RANGE_PROFILES](../android/hardware/camera2/CameraCharacteristics.md).

All camera devices supporting the [android.hardware.camera2.CameraCharacteristics#REQUEST_AVAILABLE_CAPABILITIES_DYNAMIC_RANGE_TEN_BIT](../android/hardware/camera2/CameraMetadata.md) capability must advertise the supported 10-bit dynamic range profiles in [getSupportedProfiles](../android/hardware/camera2/params/DynamicRangeProfiles.md))

Some devices may not be able to support 8-bit and/or 10-bit output with different dynamic range profiles within the same capture request. Such device specific constraints can be queried by calling [getProfileCaptureRequestConstraints](../android/hardware/camera2/params/DynamicRangeProfiles.md)). Do note that unsupported combinations will result in [IllegalArgumentException](../java/lang/IllegalArgumentException.md) when trying to submit a capture request. Capture requests that only reference outputs configured using the same dynamic range profile value will never fail due to such constraints.

## Summary

| Constants ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [DOLBY_VISION_10B_HDR_OEM](../android/hardware/camera2/params/DynamicRangeProfiles.md) This is the camera mode for the default Dolby Vision capture mode for the specific device. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [DOLBY_VISION_10B_HDR_OEM_PO](../android/hardware/camera2/params/DynamicRangeProfiles.md) This is the power optimized mode for 10-bit Dolby Vision HDR device specific capture Mode. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [DOLBY_VISION_10B_HDR_REF](../android/hardware/camera2/params/DynamicRangeProfiles.md) This is a camera mode for Dolby Vision capture optimized for a more scene accurate capture. |
| --- | --- |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [DOLBY_VISION_10B_HDR_REF_PO](../android/hardware/camera2/params/DynamicRangeProfiles.md) This is the power optimized mode for 10-bit Dolby Vision HDR Reference Mode. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [DOLBY_VISION_8B_HDR_OEM](../android/hardware/camera2/params/DynamicRangeProfiles.md) This is the 8-bit version of device specific tuned and optimized Dolby Vision capture mode. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [DOLBY_VISION_8B_HDR_OEM_PO](../android/hardware/camera2/params/DynamicRangeProfiles.md) This is the power optimized mode for 8-bit Dolby Vision HDR device specific capture Mode. |
| --- | --- |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [DOLBY_VISION_8B_HDR_REF](../android/hardware/camera2/params/DynamicRangeProfiles.md) This is the 8-bit version of the Dolby Vision reference capture mode optimized for scene accuracy. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [DOLBY_VISION_8B_HDR_REF_PO](../android/hardware/camera2/params/DynamicRangeProfiles.md) This is the power optimized mode for 8-bit Dolby Vision HDR Reference Mode. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [HDR10](../android/hardware/camera2/params/DynamicRangeProfiles.md) 10-bit pixel samples encoded using the SMPTE ST 2084 transfer function. |
| --- | --- |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [HDR10_PLUS](../android/hardware/camera2/params/DynamicRangeProfiles.md) 10-bit pixel samples encoded using the SMPTE ST 2084 transfer function. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [HLG10](../android/hardware/camera2/params/DynamicRangeProfiles.md) 10-bit pixel samples encoded using the Hybrid log-gamma transfer function |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [PUBLIC_MAX](../android/hardware/camera2/params/DynamicRangeProfiles.md) <br /> |
| --- | --- |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [STANDARD](../android/hardware/camera2/params/DynamicRangeProfiles.md) This the default 8-bit standard profile that will be used in case where camera clients do not explicitly configure a supported dynamic range profile by calling [OutputConfiguration.setDynamicRangeProfile](../android/hardware/camera2/params/OutputConfiguration.md)). |

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DynamicRangeProfiles](../android/hardware/camera2/params/DynamicRangeProfiles.md))`(`elements:` ` [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)`)` Create a new immutable DynamicRangeProfiles instance. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)!\> | [getProfileCaptureRequestConstraints](../android/hardware/camera2/params/DynamicRangeProfiles.md))`(`profile:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Return a list of supported dynamic range profiles that can be referenced in a single capture request along with a given profile. |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)!\> | [getSupportedProfiles](../android/hardware/camera2/params/DynamicRangeProfiles.md))`()` Return a set of supported dynamic range profiles. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isExtraLatencyPresent](../android/hardware/camera2/params/DynamicRangeProfiles.md))`(`profile:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Check whether a given dynamic range profile is suitable for latency sensitive use cases. |
| --- | --- |

## Constants

### DOLBY_VISION_10B_HDR_OEM

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DOLBY_VISION_10B_HDR_OEM: Long
```

This is the camera mode for the default Dolby Vision capture mode for the specific device. This would be tuned by each specific device for consumer pleasing results that resonate with their particular audience. We expect that each specific device would have a different look for their default Dolby Vision capture. 

 Value: 64L

### DOLBY_VISION_10B_HDR_OEM_PO

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DOLBY_VISION_10B_HDR_OEM_PO: Long
```

This is the power optimized mode for 10-bit Dolby Vision HDR device specific capture Mode. 

 Value: 128L

### DOLBY_VISION_10B_HDR_REF

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DOLBY_VISION_10B_HDR_REF: Long
```

This is a camera mode for Dolby Vision capture optimized for a more scene accurate capture. This would typically differ from what a specific device might want to tune for a consumer optimized Dolby Vision general capture. 

 Value: 16L

### DOLBY_VISION_10B_HDR_REF_PO

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DOLBY_VISION_10B_HDR_REF_PO: Long
```

This is the power optimized mode for 10-bit Dolby Vision HDR Reference Mode. 

 Value: 32L

### DOLBY_VISION_8B_HDR_OEM

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DOLBY_VISION_8B_HDR_OEM: Long
```

This is the 8-bit version of device specific tuned and optimized Dolby Vision capture mode. 

 Value: 1024L

### DOLBY_VISION_8B_HDR_OEM_PO

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DOLBY_VISION_8B_HDR_OEM_PO: Long
```

This is the power optimized mode for 8-bit Dolby Vision HDR device specific capture Mode. 

 Value: 2048L

### DOLBY_VISION_8B_HDR_REF

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DOLBY_VISION_8B_HDR_REF: Long
```

This is the 8-bit version of the Dolby Vision reference capture mode optimized for scene accuracy. 

 Value: 256L

### DOLBY_VISION_8B_HDR_REF_PO

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DOLBY_VISION_8B_HDR_REF_PO: Long
```

This is the power optimized mode for 8-bit Dolby Vision HDR Reference Mode. 

 Value: 512L

### HDR10

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HDR10: Long
```

10-bit pixel samples encoded using the SMPTE ST 2084 transfer function.

This profile utilizes internal static metadata to increase the quality of the capture. 

 Value: 4L

### HDR10_PLUS

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HDR10_PLUS: Long
```

10-bit pixel samples encoded using the SMPTE ST 2084 transfer function.

In contrast to HDR10, this profile uses internal per-frame metadata to further enhance the quality of the capture. 

 Value: 8L

### HLG10

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HLG10: Long
```

10-bit pixel samples encoded using the Hybrid log-gamma transfer function

All 10-bit output capable devices are required to support this profile. 

 Value: 2L

### PUBLIC_MAX

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PUBLIC_MAX: Long
```  

 Value: 4096L

### STANDARD

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STANDARD: Long
```

This the default 8-bit standard profile that will be used in case where camera clients do not explicitly configure a supported dynamic range profile by calling [OutputConfiguration.setDynamicRangeProfile](../android/hardware/camera2/params/OutputConfiguration.md)). 

 Value: 1L

## Public constructors

### DynamicRangeProfiles

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DynamicRangeProfiles(elements: LongArray)
```

Create a new immutable DynamicRangeProfiles instance.

This constructor takes over the array; do not write to the array afterwards.

Do note that the constructor is available for testing purposes only! Camera clients must always retrieve the value of [android.hardware.camera2.CameraCharacteristics#REQUEST_AVAILABLE_DYNAMIC_RANGE_PROFILES](../android/hardware/camera2/CameraCharacteristics.md). for a given camera id in order to retrieve the device capabilities.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `elements` | [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html):An array of elements describing the map. It contains three elements per entry. The first element describes the supported dynamic range profile value. The second element contains a bitmap of concurrently supported dynamic range profiles within the same capture request. The third element contains a hint about extra latency associated with the corresponding dynamic range. Bitmap values of 0 indicate that there are no constraints. This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the`elements`array length is invalid, not divisible by 3 or contains invalid element values |
| `java.lang.NullPointerException` | if`elements`is`null` |

## Public methods

### getProfileCaptureRequestConstraints

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getProfileCaptureRequestConstraints(profile: Long): MutableSet<Long!>
```

Return a list of supported dynamic range profiles that can be referenced in a single capture request along with a given profile.

For example if assume that a particular 10-bit output capable device returns ([STANDARD](../android/hardware/camera2/params/DynamicRangeProfiles.md), [HLG10](../android/hardware/camera2/params/DynamicRangeProfiles.md), [HDR10](../android/hardware/camera2/params/DynamicRangeProfiles.md)) as result from calling [getSupportedProfiles()](../android/hardware/camera2/params/DynamicRangeProfiles.md))and [getProfileCaptureRequestConstraints](../android/hardware/camera2/params/DynamicRangeProfiles.md))returns ([STANDARD](../android/hardware/camera2/params/DynamicRangeProfiles.md), [HLG10](../android/hardware/camera2/params/DynamicRangeProfiles.md)) when given an argument of [STANDARD](../android/hardware/camera2/params/DynamicRangeProfiles.md). This means that the corresponding camera device will only accept and process capture requests that reference outputs configured using [HDR10](../android/hardware/camera2/params/DynamicRangeProfiles.md) dynamic profile or alternatively some combination of [STANDARD](../android/hardware/camera2/params/DynamicRangeProfiles.md) and [HLG10](../android/hardware/camera2/params/DynamicRangeProfiles.md). However trying to queue capture requests to outputs that reference both [HDR10](../android/hardware/camera2/params/DynamicRangeProfiles.md) and [STANDARD](../android/hardware/camera2/params/DynamicRangeProfiles.md)/ [HLG10](../android/hardware/camera2/params/DynamicRangeProfiles.md) will result in [IllegalArgumentException](../java/lang/IllegalArgumentException.md).

The list will be empty in case there are no constraints for the given profile.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `profile` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):Value is [android.hardware.camera2.params.DynamicRangeProfiles#STANDARD](../android/hardware/camera2/params/DynamicRangeProfiles.md), [android.hardware.camera2.params.DynamicRangeProfiles#HLG10](../android/hardware/camera2/params/DynamicRangeProfiles.md), [android.hardware.camera2.params.DynamicRangeProfiles#HDR10](../android/hardware/camera2/params/DynamicRangeProfiles.md), [android.hardware.camera2.params.DynamicRangeProfiles#HDR10_PLUS](../android/hardware/camera2/params/DynamicRangeProfiles.md), [android.hardware.camera2.params.DynamicRangeProfiles#DOLBY_VISION_10B_HDR_REF](../android/hardware/camera2/params/DynamicRangeProfiles.md), [android.hardware.camera2.params.DynamicRangeProfiles#DOLBY_VISION_10B_HDR_REF_PO](../android/hardware/camera2/params/DynamicRangeProfiles.md), [android.hardware.camera2.params.DynamicRangeProfiles#DOLBY_VISION_10B_HDR_OEM](../android/hardware/camera2/params/DynamicRangeProfiles.md), [android.hardware.camera2.params.DynamicRangeProfiles#DOLBY_VISION_10B_HDR_OEM_PO](../android/hardware/camera2/params/DynamicRangeProfiles.md), [android.hardware.camera2.params.DynamicRangeProfiles#DOLBY_VISION_8B_HDR_REF](../android/hardware/camera2/params/DynamicRangeProfiles.md), [android.hardware.camera2.params.DynamicRangeProfiles#DOLBY_VISION_8B_HDR_REF_PO](../android/hardware/camera2/params/DynamicRangeProfiles.md), [android.hardware.camera2.params.DynamicRangeProfiles#DOLBY_VISION_8B_HDR_OEM](../android/hardware/camera2/params/DynamicRangeProfiles.md), or [android.hardware.camera2.params.DynamicRangeProfiles#DOLBY_VISION_8B_HDR_OEM_PO](../android/hardware/camera2/params/DynamicRangeProfiles.md) |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)!> | non-modifiable set of dynamic range profiles This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If the profile argument is not within the list returned by getSupportedProfiles() |

**See Also**

- [android.hardware.camera2.params.OutputConfiguration#setDynamicRangeProfile](../android/hardware/camera2/params/OutputConfiguration.md)) 

### getSupportedProfiles

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSupportedProfiles(): MutableSet<Long!>
```

Return a set of supported dynamic range profiles.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)!> | non-modifiable set of dynamic range profiles This value cannot be`null`. |

### isExtraLatencyPresent

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isExtraLatencyPresent(profile: Long): Boolean
```

Check whether a given dynamic range profile is suitable for latency sensitive use cases.

Due to internal lookahead logic, camera outputs configured with some dynamic range profiles may experience additional latency greater than 3 buffers. Using camera outputs with such profiles for latency sensitive use cases such as camera preview is not recommended. Profiles that have such extra streaming delay are typically utilized for scenarios such as offscreen video recording.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `profile` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):Value is [android.hardware.camera2.params.DynamicRangeProfiles#STANDARD](../android/hardware/camera2/params/DynamicRangeProfiles.md), [android.hardware.camera2.params.DynamicRangeProfiles#HLG10](../android/hardware/camera2/params/DynamicRangeProfiles.md), [android.hardware.camera2.params.DynamicRangeProfiles#HDR10](../android/hardware/camera2/params/DynamicRangeProfiles.md), [android.hardware.camera2.params.DynamicRangeProfiles#HDR10_PLUS](../android/hardware/camera2/params/DynamicRangeProfiles.md), [android.hardware.camera2.params.DynamicRangeProfiles#DOLBY_VISION_10B_HDR_REF](../android/hardware/camera2/params/DynamicRangeProfiles.md), [android.hardware.camera2.params.DynamicRangeProfiles#DOLBY_VISION_10B_HDR_REF_PO](../android/hardware/camera2/params/DynamicRangeProfiles.md), [android.hardware.camera2.params.DynamicRangeProfiles#DOLBY_VISION_10B_HDR_OEM](../android/hardware/camera2/params/DynamicRangeProfiles.md), [android.hardware.camera2.params.DynamicRangeProfiles#DOLBY_VISION_10B_HDR_OEM_PO](../android/hardware/camera2/params/DynamicRangeProfiles.md), [android.hardware.camera2.params.DynamicRangeProfiles#DOLBY_VISION_8B_HDR_REF](../android/hardware/camera2/params/DynamicRangeProfiles.md), [android.hardware.camera2.params.DynamicRangeProfiles#DOLBY_VISION_8B_HDR_REF_PO](../android/hardware/camera2/params/DynamicRangeProfiles.md), [android.hardware.camera2.params.DynamicRangeProfiles#DOLBY_VISION_8B_HDR_OEM](../android/hardware/camera2/params/DynamicRangeProfiles.md), or [android.hardware.camera2.params.DynamicRangeProfiles#DOLBY_VISION_8B_HDR_OEM_PO](../android/hardware/camera2/params/DynamicRangeProfiles.md) |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the given profile is not suitable for latency sensitive use cases, false otherwise |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If the profile argument is not within the list returned by getSupportedProfiles() |

**See Also**

- [android.hardware.camera2.params.OutputConfiguration#setDynamicRangeProfile](../android/hardware/camera2/params/OutputConfiguration.md))
