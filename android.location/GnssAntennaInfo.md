# GnssAntennaInfo

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GnssAntennaInfo

Kotlin| [Java](https://developer.android.com/reference/android/location/GnssAntennaInfo "View this page in Java") 

```
class GnssAntennaInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.location.GnssAntennaInfo](https://developer.android.com/reference/kotlin/android/location/GnssAntennaInfo#) |

A class that contains information about a GNSS antenna. GNSS antenna characteristics can change with device configuration, such as when a device is folded open or closed. Antenna information is delivered to registered instances of [Listener](https://developer.android.com/reference/kotlin/android/location/GnssAntennaInfo.Listener).

Antenna info parameters are measured for each specific device model by the device manufacturers and provided to the Android framework.

[GnssAntennaInfo](https://developer.android.com/reference/kotlin/android/location/GnssAntennaInfo#) is returned per frequency band at the center frequency of the band.

## Summary

| Nested classes ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/location/GnssAntennaInfo.Builder) Builder class for GnssAntennaInfo. |
| abstract | [Listener](https://developer.android.com/reference/kotlin/android/location/GnssAntennaInfo.Listener) Used for receiving GNSS antenna info from the GNSS engine. |
| | [PhaseCenterOffset](https://developer.android.com/reference/kotlin/android/location/GnssAntennaInfo.PhaseCenterOffset) Class containing information about the antenna phase center offset (PCO). |
| | [SphericalCorrections](https://developer.android.com/reference/kotlin/android/location/GnssAntennaInfo.SphericalCorrections) Represents corrections on a spherical mapping. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/location/GnssAntennaInfo#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/location/GnssAntennaInfo#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [getCarrierFrequencyMHz](https://developer.android.com/reference/kotlin/android/location/GnssAntennaInfo#getCarrierFrequencyMHz())`()` Returns the center frequency of the corresponding carrier frequency band. |
| [GnssAntennaInfo.PhaseCenterOffset](https://developer.android.com/reference/kotlin/android/location/GnssAntennaInfo.PhaseCenterOffset) | [getPhaseCenterOffset](https://developer.android.com/reference/kotlin/android/location/GnssAntennaInfo#getPhaseCenterOffset())`()` Returns a [PhaseCenterOffset](https://developer.android.com/reference/kotlin/android/location/GnssAntennaInfo.PhaseCenterOffset) object encapsulating the phase center offset and corresponding uncertainties in millimeters. |
| [GnssAntennaInfo.SphericalCorrections](https://developer.android.com/reference/kotlin/android/location/GnssAntennaInfo.SphericalCorrections)? | [getPhaseCenterVariationCorrections](https://developer.android.com/reference/kotlin/android/location/GnssAntennaInfo#getPhaseCenterVariationCorrections())`()` Returns a [SphericalCorrections](https://developer.android.com/reference/kotlin/android/location/GnssAntennaInfo.SphericalCorrections) object encapsulating the phase center variation corrections and corresponding uncertainties in millimeters. |
| [GnssAntennaInfo.SphericalCorrections](https://developer.android.com/reference/kotlin/android/location/GnssAntennaInfo.SphericalCorrections)? | [getSignalGainCorrections](https://developer.android.com/reference/kotlin/android/location/GnssAntennaInfo#getSignalGainCorrections())`()` Returns a [SphericalCorrections](https://developer.android.com/reference/kotlin/android/location/GnssAntennaInfo.SphericalCorrections) object encapsulating the signal gain corrections and corresponding uncertainties in dBi. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/location/GnssAntennaInfo#hashCode())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/location/GnssAntennaInfo#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/location/GnssAntennaInfo#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`parcel:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [GnssAntennaInfo](https://developer.android.com/reference/kotlin/android/location/GnssAntennaInfo#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/location/GnssAntennaInfo#CREATOR:android.os.Parcelable.Creator) <br /> |

## Public methods

### describeContents

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

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

Returns a [PhaseCenterOffset](https://developer.android.com/reference/kotlin/android/location/GnssAntennaInfo.PhaseCenterOffset) object encapsulating the phase center offset and corresponding uncertainties in millimeters.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [GnssAntennaInfo.PhaseCenterOffset](https://developer.android.com/reference/kotlin/android/location/GnssAntennaInfo.PhaseCenterOffset) | [PhaseCenterOffset](https://developer.android.com/reference/kotlin/android/location/GnssAntennaInfo.PhaseCenterOffset) This value cannot be`null`. |

### getPhaseCenterVariationCorrections

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPhaseCenterVariationCorrections(): GnssAntennaInfo.SphericalCorrections?
```

Returns a [SphericalCorrections](https://developer.android.com/reference/kotlin/android/location/GnssAntennaInfo.SphericalCorrections) object encapsulating the phase center variation corrections and corresponding uncertainties in millimeters.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [GnssAntennaInfo.SphericalCorrections](https://developer.android.com/reference/kotlin/android/location/GnssAntennaInfo.SphericalCorrections)? | phase center variation corrections as [SphericalCorrections](https://developer.android.com/reference/kotlin/android/location/GnssAntennaInfo.SphericalCorrections) This value may be`null`. |

### getSignalGainCorrections

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSignalGainCorrections(): GnssAntennaInfo.SphericalCorrections?
```

Returns a [SphericalCorrections](https://developer.android.com/reference/kotlin/android/location/GnssAntennaInfo.SphericalCorrections) object encapsulating the signal gain corrections and corresponding uncertainties in dBi.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [GnssAntennaInfo.SphericalCorrections](https://developer.android.com/reference/kotlin/android/location/GnssAntennaInfo.SphericalCorrections)? | signal gain corrections as [SphericalCorrections](https://developer.android.com/reference/kotlin/android/location/GnssAntennaInfo.SphericalCorrections) This value may be`null`. |

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
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |
| `parcel` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):This value cannot be`null`. |

## Properties

### CREATOR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<GnssAntennaInfo!>
```
