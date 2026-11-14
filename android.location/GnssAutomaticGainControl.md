# GnssAutomaticGainControl

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GnssAutomaticGainControl

Kotlin| [Java](https://developer.android.com/reference/android/location/GnssAutomaticGainControl "View this page in Java") 

```
class GnssAutomaticGainControl : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.location.GnssAutomaticGainControl](https://developer.android.com/reference/kotlin/android/location/GnssAutomaticGainControl#) |

A class that contains GNSS Automatic Gain Control (AGC) information.

AGC acts as a variable gain amplifier adjusting the power of the incoming signal. The AGC level may be used to indicate potential interference. Higher gain (and/or lower input power) shall be output as a positive number. Hence in cases of strong jamming, in the band of this signal, this value will go more negative. This value must be consistent given the same level of the incoming signal power.

Note: Different hardware designs (e.g. antenna, pre-amplification, or other RF HW components) may also affect the typical output of this value on any given hardware design in an open sky test - the important aspect of this output is that changes in this value are indicative of changes on input signal power in the frequency band for this measurement.

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/location/GnssAutomaticGainControl.Builder) Builder for [GnssAutomaticGainControl](https://developer.android.com/reference/kotlin/android/location/GnssAutomaticGainControl#) |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/location/GnssAutomaticGainControl#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/location/GnssAutomaticGainControl#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getCarrierFrequencyHz](https://developer.android.com/reference/kotlin/android/location/GnssAutomaticGainControl#getCarrierFrequencyHz())`()` Gets the carrier frequency of the tracked signal. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getConstellationType](https://developer.android.com/reference/kotlin/android/location/GnssAutomaticGainControl#getConstellationType())`()` Gets the constellation type. |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [getLevelDb](https://developer.android.com/reference/kotlin/android/location/GnssAutomaticGainControl#getLevelDb())`()` Gets the Automatic Gain Control level in dB. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/location/GnssAutomaticGainControl#hashCode())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/location/GnssAutomaticGainControl#toString())`()` Returns a string representation of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/location/GnssAutomaticGainControl#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`parcel:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flag:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [GnssAutomaticGainControl](https://developer.android.com/reference/kotlin/android/location/GnssAutomaticGainControl#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/location/GnssAutomaticGainControl#CREATOR:android.os.Parcelable.Creator) <br /> |

## Public methods

### describeContents

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### equals

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getCarrierFrequencyHz

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCarrierFrequencyHz(): Long
```

Gets the carrier frequency of the tracked signal.

For example it can be the GPS central frequency for L1 = 1575.45 MHz, or L2 = 1227.60 MHz, L5 = 1176.45 MHz, varying GLO channels, etc.

| Return ||
|------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the carrier frequency of the signal tracked in Hz. Value is 0 or greater |

### getConstellationType

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getConstellationType(): Int
```

Gets the constellation type.

The return value is one of those constants with`CONSTELLATION_`prefix in [GnssStatus](https://developer.android.com/reference/kotlin/android/location/GnssStatus).

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.location.GnssStatus#CONSTELLATION_UNKNOWN](https://developer.android.com/reference/kotlin/android/location/GnssStatus#CONSTELLATION_UNKNOWN:kotlin.Int), [android.location.GnssStatus#CONSTELLATION_GPS](https://developer.android.com/reference/kotlin/android/location/GnssStatus#CONSTELLATION_GPS:kotlin.Int), [android.location.GnssStatus#CONSTELLATION_SBAS](https://developer.android.com/reference/kotlin/android/location/GnssStatus#CONSTELLATION_SBAS:kotlin.Int), [android.location.GnssStatus#CONSTELLATION_GLONASS](https://developer.android.com/reference/kotlin/android/location/GnssStatus#CONSTELLATION_GLONASS:kotlin.Int), [android.location.GnssStatus#CONSTELLATION_QZSS](https://developer.android.com/reference/kotlin/android/location/GnssStatus#CONSTELLATION_QZSS:kotlin.Int), [android.location.GnssStatus#CONSTELLATION_BEIDOU](https://developer.android.com/reference/kotlin/android/location/GnssStatus#CONSTELLATION_BEIDOU:kotlin.Int), [android.location.GnssStatus#CONSTELLATION_GALILEO](https://developer.android.com/reference/kotlin/android/location/GnssStatus#CONSTELLATION_GALILEO:kotlin.Int), or [android.location.GnssStatus#CONSTELLATION_IRNSS](https://developer.android.com/reference/kotlin/android/location/GnssStatus#CONSTELLATION_IRNSS:kotlin.Int) |

### getLevelDb

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLevelDb(): Double
```

Gets the Automatic Gain Control level in dB.

| Return ||
|----------------------------------------------------------------------------------|---------------------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | Value is between -10000.0f and 10000.0f inclusive |

### hashCode

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### toString

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### writeToParcel

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    parcel: Parcel, 
    flag: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |
| `parcel` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):This value cannot be`null`. |

## Properties

### CREATOR

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<GnssAutomaticGainControl!>
```
