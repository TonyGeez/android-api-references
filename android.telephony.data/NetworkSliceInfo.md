# NetworkSliceInfo

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NetworkSliceInfo

Kotlin| [Java](../android/telephony/data/NetworkSliceInfo.md) 
| --- | --- |

```
class NetworkSliceInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telephony.data.NetworkSliceInfo](../android/telephony/data/NetworkSliceInfo.md) |

Represents a S-NSSAI as defined in 3GPP TS 24.501, which represents a network slice. There are 2 main fields that define a slice, SliceServiceType and SliceDifferentiator. SliceServiceType defines the type of service provided by the slice, and SliceDifferentiator is used to differentiate between multiple slices of the same type. If the devices is not on HPLMN, the mappedHplmn versions of these 2 fields indicate the corresponding values in HPLMN.

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/telephony/data/NetworkSliceInfo.Builder.md) Provides a convenient way to set the fields of a [NetworkSliceInfo](../android/telephony/data/NetworkSliceInfo.md) when creating a new instance. |

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SLICE_DIFFERENTIATOR_NO_SLICE](../android/telephony/data/NetworkSliceInfo.md) When set on a Slice Differentiator, this value indicates that there is no corresponding Slice. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SLICE_SERVICE_TYPE_EMBB](../android/telephony/data/NetworkSliceInfo.md) Slice suitable for the handling of 5G enhanced Mobile Broadband. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SLICE_SERVICE_TYPE_MIOT](../android/telephony/data/NetworkSliceInfo.md) Slice suitable for the handling of massive IoT. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SLICE_SERVICE_TYPE_NONE](../android/telephony/data/NetworkSliceInfo.md) Indicates that the service type is not present. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SLICE_SERVICE_TYPE_URLLC](../android/telephony/data/NetworkSliceInfo.md) Slice suitable for the handling of ultra-reliable low latency communications. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SLICE_STATUS_ALLOWED](../android/telephony/data/NetworkSliceInfo.md) The slice is allowed to be used. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SLICE_STATUS_CONFIGURED](../android/telephony/data/NetworkSliceInfo.md) The slice is configured but not allowed or rejected yet. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SLICE_STATUS_DEFAULT_CONFIGURED](../android/telephony/data/NetworkSliceInfo.md) The slice is configured by home operator(HPLMN) in default and is used if configured/allowed slices are not available for the serving PLMN. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SLICE_STATUS_REJECTED_NOT_AVAILABLE_IN_PLMN](../android/telephony/data/NetworkSliceInfo.md) The slice is rejected because not available in PLMN. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SLICE_STATUS_REJECTED_NOT_AVAILABLE_IN_REGISTERED_AREA](../android/telephony/data/NetworkSliceInfo.md) The slice is rejected because not available in registered area. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SLICE_STATUS_UNKNOWN](../android/telephony/data/NetworkSliceInfo.md) The slice status is unknown. |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/telephony/data/NetworkSliceInfo.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/telephony/data/NetworkSliceInfo.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMappedHplmnSliceDifferentiator](../android/telephony/data/NetworkSliceInfo.md))`()` This Slice Differentiator corresponds to a [NetworkSliceInfo](../android/telephony/data/NetworkSliceInfo.md)(S-NSSAI) of the HPLMN; [getSliceDifferentiator()](../android/telephony/data/NetworkSliceInfo.md))is mapped to this value. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMappedHplmnSliceServiceType](../android/telephony/data/NetworkSliceInfo.md))`()` Corresponds to a Slice Info (S-NSSAI) of the HPLMN. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSliceDifferentiator](../android/telephony/data/NetworkSliceInfo.md))`()` Identifies the slice from others with the same Slice Service Type. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSliceServiceType](../android/telephony/data/NetworkSliceInfo.md))`()` The type of service provided by the slice. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getStatus](../android/telephony/data/NetworkSliceInfo.md))`()` Field to indicate the current status of the slice. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/telephony/data/NetworkSliceInfo.md))`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/telephony/data/NetworkSliceInfo.md))`()` <br /> |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/telephony/data/NetworkSliceInfo.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [NetworkSliceInfo](../android/telephony/data/NetworkSliceInfo.md)!\> | [CREATOR](../android/telephony/data/NetworkSliceInfo.md) <br /> |

## Constants

### SLICE_DIFFERENTIATOR_NO_SLICE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SLICE_DIFFERENTIATOR_NO_SLICE: Int
```

When set on a Slice Differentiator, this value indicates that there is no corresponding Slice. 

 Value: -1

### SLICE_SERVICE_TYPE_EMBB

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SLICE_SERVICE_TYPE_EMBB: Int
```

Slice suitable for the handling of 5G enhanced Mobile Broadband. 

 Value: 1

### SLICE_SERVICE_TYPE_MIOT

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SLICE_SERVICE_TYPE_MIOT: Int
```

Slice suitable for the handling of massive IoT. 

 Value: 3

### SLICE_SERVICE_TYPE_NONE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SLICE_SERVICE_TYPE_NONE: Int
```

Indicates that the service type is not present. 

 Value: 0

### SLICE_SERVICE_TYPE_URLLC

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SLICE_SERVICE_TYPE_URLLC: Int
```

Slice suitable for the handling of ultra-reliable low latency communications. 

 Value: 2

### SLICE_STATUS_ALLOWED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SLICE_STATUS_ALLOWED: Int
```

The slice is allowed to be used. 

 Value: 2

### SLICE_STATUS_CONFIGURED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SLICE_STATUS_CONFIGURED: Int
```

The slice is configured but not allowed or rejected yet. 

 Value: 1

### SLICE_STATUS_DEFAULT_CONFIGURED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SLICE_STATUS_DEFAULT_CONFIGURED: Int
```

The slice is configured by home operator(HPLMN) in default and is used if configured/allowed slices are not available for the serving PLMN. 

 Value: 5

### SLICE_STATUS_REJECTED_NOT_AVAILABLE_IN_PLMN

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SLICE_STATUS_REJECTED_NOT_AVAILABLE_IN_PLMN: Int
```

The slice is rejected because not available in PLMN. 

 Value: 3

### SLICE_STATUS_REJECTED_NOT_AVAILABLE_IN_REGISTERED_AREA

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SLICE_STATUS_REJECTED_NOT_AVAILABLE_IN_REGISTERED_AREA: Int
```

The slice is rejected because not available in registered area. 

 Value: 4

### SLICE_STATUS_UNKNOWN

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SLICE_STATUS_UNKNOWN: Int
```

The slice status is unknown. This can happen during IWLAN-\>cellular handover when the NetworkSliceInfo is received over IWLAN. 

 Value: 0

## Public methods

### describeContents

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### equals

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getMappedHplmnSliceDifferentiator

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMappedHplmnSliceDifferentiator(): Int
```

This Slice Differentiator corresponds to a [NetworkSliceInfo](../android/telephony/data/NetworkSliceInfo.md)(S-NSSAI) of the HPLMN; [getSliceDifferentiator()](../android/telephony/data/NetworkSliceInfo.md))is mapped to this value.

<br />

Returns [SLICE_DIFFERENTIATOR_NO_SLICE](../android/telephony/data/NetworkSliceInfo.md) if either of the following are true:

- [getSliceDifferentiator()](../android/telephony/data/NetworkSliceInfo.md))returns [SLICE_DIFFERENTIATOR_NO_SLICE](../android/telephony/data/NetworkSliceInfo.md)
- [getMappedHplmnSliceServiceType()](../android/telephony/data/NetworkSliceInfo.md))returns [SLICE_SERVICE_TYPE_NONE](../android/telephony/data/NetworkSliceInfo.md)

<br />

see: 3GPP TS 24.501 Section 9.11.2.8.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is between android.telephony.data.NetworkSliceInfo#MIN_SLICE_DIFFERENTIATOR and android.telephony.data.NetworkSliceInfo#MAX_SLICE_DIFFERENTIATOR inclusive |

### getMappedHplmnSliceServiceType

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMappedHplmnSliceServiceType(): Int
```

Corresponds to a Slice Info (S-NSSAI) of the HPLMN.

<br />

see: 3GPP TS 24.501 Section 9.11.2.8.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.telephony.data.NetworkSliceInfo#SLICE_SERVICE_TYPE_NONE](../android/telephony/data/NetworkSliceInfo.md), [android.telephony.data.NetworkSliceInfo#SLICE_SERVICE_TYPE_EMBB](../android/telephony/data/NetworkSliceInfo.md), [android.telephony.data.NetworkSliceInfo#SLICE_SERVICE_TYPE_URLLC](../android/telephony/data/NetworkSliceInfo.md), or [android.telephony.data.NetworkSliceInfo#SLICE_SERVICE_TYPE_MIOT](../android/telephony/data/NetworkSliceInfo.md) |

### getSliceDifferentiator

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSliceDifferentiator(): Int
```

Identifies the slice from others with the same Slice Service Type.

<br />

Returns [SLICE_DIFFERENTIATOR_NO_SLICE](../android/telephony/data/NetworkSliceInfo.md) if [getSliceServiceType](../android/telephony/data/NetworkSliceInfo.md))returns [SLICE_SERVICE_TYPE_NONE](../android/telephony/data/NetworkSliceInfo.md).

<br />

see: 3GPP TS 24.501 Section 9.11.2.8.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is between android.telephony.data.NetworkSliceInfo#MIN_SLICE_DIFFERENTIATOR and android.telephony.data.NetworkSliceInfo#MAX_SLICE_DIFFERENTIATOR inclusive |

### getSliceServiceType

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSliceServiceType(): Int
```

The type of service provided by the slice.

<br />

see: 3GPP TS 24.501 Section 9.11.2.8.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.telephony.data.NetworkSliceInfo#SLICE_SERVICE_TYPE_NONE](../android/telephony/data/NetworkSliceInfo.md), [android.telephony.data.NetworkSliceInfo#SLICE_SERVICE_TYPE_EMBB](../android/telephony/data/NetworkSliceInfo.md), [android.telephony.data.NetworkSliceInfo#SLICE_SERVICE_TYPE_URLLC](../android/telephony/data/NetworkSliceInfo.md), or [android.telephony.data.NetworkSliceInfo#SLICE_SERVICE_TYPE_MIOT](../android/telephony/data/NetworkSliceInfo.md) |

### getStatus

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getStatus(): Int
```

Field to indicate the current status of the slice.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the current status for this slice info. Value is [android.telephony.data.NetworkSliceInfo#SLICE_STATUS_UNKNOWN](../android/telephony/data/NetworkSliceInfo.md), [android.telephony.data.NetworkSliceInfo#SLICE_STATUS_CONFIGURED](../android/telephony/data/NetworkSliceInfo.md), [android.telephony.data.NetworkSliceInfo#SLICE_STATUS_ALLOWED](../android/telephony/data/NetworkSliceInfo.md), [android.telephony.data.NetworkSliceInfo#SLICE_STATUS_REJECTED_NOT_AVAILABLE_IN_PLMN](../android/telephony/data/NetworkSliceInfo.md), [android.telephony.data.NetworkSliceInfo#SLICE_STATUS_REJECTED_NOT_AVAILABLE_IN_REGISTERED_AREA](../android/telephony/data/NetworkSliceInfo.md), or [android.telephony.data.NetworkSliceInfo#SLICE_STATUS_DEFAULT_CONFIGURED](../android/telephony/data/NetworkSliceInfo.md) |

### hashCode

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### toString

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<NetworkSliceInfo!>
```
