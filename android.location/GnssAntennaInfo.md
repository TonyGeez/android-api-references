# GnssAntennaInfo

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GnssAntennaInfo

Kotlin| [Java](../android/location/GnssAntennaInfo.md) 
| --- | --- |

```
class GnssAntennaInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.location.GnssAntennaInfo](../android/location/GnssAntennaInfo.md) |

A class that contains information about a GNSS antenna. GNSS antenna characteristics can change with device configuration, such as when a device is folded open or closed. Antenna information is delivered to registered instances of [Listener](../android/location/GnssAntennaInfo.Listener.md).

Antenna info parameters are measured for each specific device model by the device manufacturers and provided to the Android framework.

[GnssAntennaInfo](../android/location/GnssAntennaInfo.md) is returned per frequency band at the center frequency of the band.

## Summary

| Nested classes ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/location/GnssAntennaInfo.Builder.md) Builder class for GnssAntennaInfo. |
| abstract | [Listener](../android/location/GnssAntennaInfo.Listener.md) Used for receiving GNSS antenna info from the GNSS engine. |
| | [PhaseCenterOffset](../android/location/GnssAntennaInfo.PhaseCenterOffset.md) Class containing information about the antenna phase center offset (PCO). |
| --- | --- |
| | [SphericalCorrections](../android/location/GnssAntennaInfo.SphericalCorrections.md) Represents corrections on a spherical mapping. |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/location/GnssAntennaInfo.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/location/GnssAntennaInfo.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [getCarrierFrequencyMHz](../android/location/GnssAntennaInfo.md))`()` Returns the center frequency of the corresponding carrier frequency band. |
| --- | --- |
| [GnssAntennaInfo.PhaseCenterOffset](../android/location/GnssAntennaInfo.PhaseCenterOffset.md) | [getPhaseCenterOffset](../android/location/GnssAntennaInfo.md))`()` Returns a [PhaseCenterOffset](../android/location/GnssAntennaInfo.PhaseCenterOffset.md) object encapsulating the phase center offset and corresponding uncertainties in millimeters. |
| [GnssAntennaInfo.SphericalCorrections](../android/location/GnssAntennaInfo.SphericalCorrections.md)? | [getPhaseCenterVariationCorrections](../android/location/GnssAntennaInfo.md))`()` Returns a [SphericalCorrections](../android/location/GnssAntennaInfo.SphericalCorrections.md) object encapsulating the phase center variation corrections and corresponding uncertainties in millimeters. |
| [GnssAntennaInfo.SphericalCorrections](../android/location/GnssAntennaInfo.SphericalCorrections.md)? | [getSignalGainCorrections](../android/location/GnssAntennaInfo.md))`()` Returns a [SphericalCorrections](../android/location/GnssAntennaInfo.SphericalCorrections.md) object encapsulating the signal gain corrections and corresponding uncertainties in dBi. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/location/GnssAntennaInfo.md))`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/location/GnssAntennaInfo.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/location/GnssAntennaInfo.md))`(`parcel:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [GnssAntennaInfo](../android/location/GnssAntennaInfo.md)!\> | [CREATOR](../android/location/GnssAntennaInfo.md) <br /> |

## Public methods

### describeContents

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### equals

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getCarrierFrequencyMHz

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCarrierFrequencyMHz(): Double
```

Returns the center frequency of the corresponding carrier frequency band.

| Return ||
|----------------------------------------------------------------------------------|--------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | Value is 0.0f or greater |

### getPhaseCenterOffset

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPhaseCenterOffset(): GnssAntennaInfo.PhaseCenterOffset
```

Returns a [PhaseCenterOffset](../android/location/GnssAntennaInfo.PhaseCenterOffset.md) object encapsulating the phase center offset and corresponding uncertainties in millimeters.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [GnssAntennaInfo.PhaseCenterOffset](../android/location/GnssAntennaInfo.PhaseCenterOffset.md) | [PhaseCenterOffset](../android/location/GnssAntennaInfo.PhaseCenterOffset.md) This value cannot be`null`. |

### getPhaseCenterVariationCorrections

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPhaseCenterVariationCorrections(): GnssAntennaInfo.SphericalCorrections?
```

Returns a [SphericalCorrections](../android/location/GnssAntennaInfo.SphericalCorrections.md) object encapsulating the phase center variation corrections and corresponding uncertainties in millimeters.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [GnssAntennaInfo.SphericalCorrections](../android/location/GnssAntennaInfo.SphericalCorrections.md)? | phase center variation corrections as [SphericalCorrections](../android/location/GnssAntennaInfo.SphericalCorrections.md) This value may be`null`. |

### getSignalGainCorrections

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSignalGainCorrections(): GnssAntennaInfo.SphericalCorrections?
```

Returns a [SphericalCorrections](../android/location/GnssAntennaInfo.SphericalCorrections.md) object encapsulating the signal gain corrections and corresponding uncertainties in dBi.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [GnssAntennaInfo.SphericalCorrections](../android/location/GnssAntennaInfo.SphericalCorrections.md)? | signal gain corrections as [SphericalCorrections](../android/location/GnssAntennaInfo.SphericalCorrections.md) This value may be`null`. |

### hashCode

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### toString

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    parcel: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |
| `parcel` | [Parcel](../android/os/Parcel.md):This value cannot be`null`. |
| --- | --- |

## Properties

### CREATOR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<GnssAntennaInfo!>
```
