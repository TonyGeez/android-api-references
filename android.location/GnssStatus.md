Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GnssStatus

```
class GnssStatus : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.location.GnssStatus](GnssStatus.md) |

This class represents the current state of the GNSS engine and is used in conjunction with `https://developer.android.com/reference/kotlin/android/location/GnssStatus.Callback`.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/location/GnssStatus.Builder` Builder class to help create new GnssStatus instances. |
| abstract | `https://developer.android.com/reference/kotlin/android/location/GnssStatus.Callback` Used for receiving notifications when GNSS events happen. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssStatus#CONSTELLATION_BEIDOU:kotlin.Int` Constellation type constant for Beidou. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssStatus#CONSTELLATION_GALILEO:kotlin.Int` Constellation type constant for Galileo. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssStatus#CONSTELLATION_GLONASS:kotlin.Int` Constellation type constant for Glonass. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssStatus#CONSTELLATION_GPS:kotlin.Int` Constellation type constant for GPS. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssStatus#CONSTELLATION_IRNSS:kotlin.Int` Constellation type constant for IRNSS. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssStatus#CONSTELLATION_QZSS:kotlin.Int` Constellation type constant for QZSS. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssStatus#CONSTELLATION_SBAS:kotlin.Int` Constellation type constant for SBAS. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/location/GnssStatus#CONSTELLATION_UNKNOWN:kotlin.Int` Unknown constellation type. |

Inherited constants From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int`

Descriptor bit used with describeContents: indicates that the Parcelable object's flattened representation includes a file descriptor.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`

Flag for use with writeToParcel: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point.

<br />

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | describeContents Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | equals Indicates whether some other object is "equal to" this one. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | getAzimuthDegrees Retrieves the azimuth the satellite at the specified index. |
| --- | --- |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | getBasebandCn0DbHz Retrieves the baseband carrier-to-noise density of the satellite at the specified index in dB-Hz. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | getCarrierFrequencyHz Gets the carrier frequency of the signal tracked. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | getCn0DbHz Retrieves the carrier-to-noise density at the antenna of the satellite at the specified index in dB-Hz. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | getCodeType Gets the code type as defined in getCodeType of the satellite at the specified index. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getConstellationType Retrieves the constellation type of the satellite at the specified index. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | getElapsedRealtimeNanos Returns the elapsed real-time of this GnssStatus since system boot, in nanoseconds. |
| --- | --- |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | getElapsedRealtimeUncertaintyNanos Returns the estimate of the relative precision of the alignment of the #getElapsedRealtimeNanos() timestamp, with the reported GnssStatus in nanoseconds (68% confidence). |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | getElevationDegrees Retrieves the elevation of the satellite at the specified index. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getSatelliteCount Gets the total number of satellites in satellite list. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getSvid Gets the identification number for the satellite at the specific index. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasAlmanacData Reports whether the satellite at the specified index has almanac data. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasBasebandCn0DbHz Reports whether a valid getBasebandCn0DbHz is available. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasCarrierFrequencyHz Reports whether a valid getCarrierFrequencyHz is available. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasCodeType Reports whether a valid #getCodeType() is available. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasElapsedRealtimeNanos Returns `true` if #getElapsedRealtimeNanos() is available, `false` otherwise. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasElapsedRealtimeUncertaintyNanos Returns `true` if #getElapsedRealtimeUncertaintyNanos() is available, `false` otherwise. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasEphemerisData Reports whether the satellite at the specified index has ephemeris data. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | hashCode Returns a hash code value for the object. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | usedInFix Reports whether the satellite at the specified index was used in the calculation of the most recent position fix. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeToParcel Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [GnssStatus](GnssStatus.md)!\> | `https://developer.android.com/reference/kotlin/android/location/GnssStatus#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### CONSTELLATION_BEIDOU

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONSTELLATION_BEIDOU: Int
```

Constellation type constant for Beidou.

 Value: 5

### CONSTELLATION_GALILEO

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONSTELLATION_GALILEO: Int
```

Constellation type constant for Galileo.

 Value: 6

### CONSTELLATION_GLONASS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONSTELLATION_GLONASS: Int
```

Constellation type constant for Glonass.

 Value: 3

### CONSTELLATION_GPS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONSTELLATION_GPS: Int
```

Constellation type constant for GPS.

 Value: 1

### CONSTELLATION_IRNSS

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONSTELLATION_IRNSS: Int
```

Constellation type constant for IRNSS.

 Value: 7

### CONSTELLATION_QZSS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONSTELLATION_QZSS: Int
```

Constellation type constant for QZSS.

 Value: 4

### CONSTELLATION_SBAS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONSTELLATION_SBAS: Int
```

Constellation type constant for SBAS.

 Value: 2

### CONSTELLATION_UNKNOWN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONSTELLATION_UNKNOWN: Int
```

Unknown constellation type.

 Value: 0

## Public methods

### describeContents

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of writeToParcel, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### equals

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The `equals` method implements an equivalence relation on non-null object references:

- It is *reflexive* : for any non-null reference value `x`, `x.equals(x)` should return `true`.
- It is *symmetric* : for any non-null reference values `x` and `y`, `x.equals(y)` should return `true` if and only if `y.equals(x)` returns `true`.
- It is *transitive* : for any non-null reference values `x`, `y`, and `z`, if `x.equals(y)` returns `true` and `y.equals(z)` returns `true`, then `x.equals(z)` should return `true`.
- It is *consistent* : for any non-null reference values `x` and `y`, multiple invocations of `x.equals(y)` consistently return `true` or consistently return `false`, provided no information used in `equals` comparisons on the objects is modified.
- For any non-null reference value `x`, `x.equals(null)` should return `false`.

An equivalence relation partitions the elements it operates on into *equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

### getAzimuthDegrees

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAzimuthDegrees(satelliteIndex: Int): Float
```

Retrieves the azimuth the satellite at the specified index.

| Parameters ||
|---|---|
| `satelliteIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): An index from zero to getSatelliteCount - 1. Value is 0 or greater |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | Value is between 0.0f and 360.0f inclusive |

### getBasebandCn0DbHz

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getBasebandCn0DbHz(satelliteIndex: Int): Float
```

Retrieves the baseband carrier-to-noise density of the satellite at the specified index in dB-Hz.

| Parameters ||
|---|---|
| `satelliteIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): An index from zero to getSatelliteCount - 1. Value is 0 or greater |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | Value is between 0.0f and 63.0f inclusive |

### getCarrierFrequencyHz

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCarrierFrequencyHz(satelliteIndex: Int): Float
```

Gets the carrier frequency of the signal tracked.

For example it can be the GPS central frequency for L1 = 1575.45 MHz, or L2 = 1227.60 MHz, L5 = 1176.45 MHz, varying GLO channels, etc.

The value is only available if hasCarrierFrequencyHz is `true`.

| Parameters ||
|---|---|
| `satelliteIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): An index from zero to getSatelliteCount - 1. Value is 0 or greater |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | Value is 0.0f or greater |

### getCn0DbHz

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCn0DbHz(satelliteIndex: Int): Float
```

Retrieves the carrier-to-noise density at the antenna of the satellite at the specified index in dB-Hz.

| Parameters ||
|---|---|
| `satelliteIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): An index from zero to getSatelliteCount - 1. Value is 0 or greater |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | Value is between 0.0f and 63.0f inclusive |

### getCodeType

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCodeType(satelliteIndex: Int): String
```

Gets the code type as defined in getCodeType of the satellite at the specified index.

| Parameters ||
|---|---|
| `satelliteIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): An index from zero to getSatelliteCount - 1. Value is 0 or greater |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | This value cannot be `null`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#CODE_TYPE_A:kotlin.String` - `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#CODE_TYPE_B:kotlin.String` - `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#CODE_TYPE_C:kotlin.String` - `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#CODE_TYPE_D:kotlin.String` - `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#CODE_TYPE_E:kotlin.String` - `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#CODE_TYPE_I:kotlin.String` - `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#CODE_TYPE_L:kotlin.String` - `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#CODE_TYPE_M:kotlin.String` - `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#CODE_TYPE_N:kotlin.String` - `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#CODE_TYPE_P:kotlin.String` - `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#CODE_TYPE_Q:kotlin.String` - `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#CODE_TYPE_S:kotlin.String` - `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#CODE_TYPE_W:kotlin.String` - `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#CODE_TYPE_X:kotlin.String` - `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#CODE_TYPE_Y:kotlin.String` - `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#CODE_TYPE_Z:kotlin.String` - `https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#CODE_TYPE_UNKNOWN:kotlin.String` |

### getConstellationType

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getConstellationType(satelliteIndex: Int): Int
```

Retrieves the constellation type of the satellite at the specified index.

| Parameters ||
|---|---|
| `satelliteIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): An index from zero to getSatelliteCount - 1. Value is 0 or greater |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/location/GnssStatus#CONSTELLATION_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/location/GnssStatus#CONSTELLATION_GPS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/location/GnssStatus#CONSTELLATION_SBAS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/location/GnssStatus#CONSTELLATION_GLONASS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/location/GnssStatus#CONSTELLATION_QZSS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/location/GnssStatus#CONSTELLATION_BEIDOU:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/location/GnssStatus#CONSTELLATION_GALILEO:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/location/GnssStatus#CONSTELLATION_IRNSS:kotlin.Int` |

### getElapsedRealtimeNanos

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getElapsedRealtimeNanos(satelliteIndex: Int): Long
```

Returns the elapsed real-time of this GnssStatus since system boot, in nanoseconds.

| Parameters ||
|---|---|
| `satelliteIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): An index from zero to getSatelliteCount - 1 The value is only available if #hasElapsedRealtimeNanos() is `true`. Value is 0 or greater |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | Value is 0 or greater |

### getElapsedRealtimeUncertaintyNanos

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getElapsedRealtimeUncertaintyNanos(satelliteIndex: Int): Double
```

Returns the estimate of the relative precision of the alignment of the #getElapsedRealtimeNanos() timestamp, with the reported GnssStatus in nanoseconds (68% confidence).

| Parameters ||
|---|---|
| `satelliteIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): An index from zero to getSatelliteCount - 1 The value is only available if #hasElapsedRealtimeUncertaintyNanos() is `true`. Value is 0 or greater |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | Value is 0.0f or greater |

### getElevationDegrees

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getElevationDegrees(satelliteIndex: Int): Float
```

Retrieves the elevation of the satellite at the specified index.

| Parameters ||
|---|---|
| `satelliteIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): An index from zero to getSatelliteCount - 1. Value is 0 or greater |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | Value is between -90.0f and 90.0f inclusive |

### getSatelliteCount

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSatelliteCount(): Int
```

Gets the total number of satellites in satellite list.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is 0 or greater |

### getSvid

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSvid(satelliteIndex: Int): Int
```

Gets the identification number for the satellite at the specific index.

This svid is pseudo-random number for most constellations. It is FCN \& OSN number for Glonass.

The distinction is made by looking at constellation field getConstellationType Expected values are in the range of:

- GPS: 1-32
- SBAS: 120-151, 183-192
- GLONASS: One of: OSN, or FCN+100
 - 1-25 as the orbital slot number (OSN) (preferred, if known)
 - 93-106 as the frequency channel number (FCN) (-7 to +6) plus 100. i.e. encode FCN of -7 as 93, 0 as 100, and +6 as 106
- QZSS: 183-212
- Galileo: 1-36
- Beidou: 1-63
- IRNSS: 1-14

See [RINEX (The Receiver Independent Exchange Format) Version 4.00](https://files.igs.org/pub/data/format/rinex_4.00.pdf).

| Parameters ||
|---|---|
| `satelliteIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): An index from zero to getSatelliteCount - 1. Value is 0 or greater |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is 1 or greater |

### hasAlmanacData

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasAlmanacData(satelliteIndex: Int): Boolean
```

Reports whether the satellite at the specified index has almanac data.

| Parameters ||
|---|---|
| `satelliteIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): An index from zero to getSatelliteCount - 1. Value is 0 or greater |

### hasBasebandCn0DbHz

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasBasebandCn0DbHz(satelliteIndex: Int): Boolean
```

Reports whether a valid getBasebandCn0DbHz is available.

| Parameters ||
|---|---|
| `satelliteIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): An index from zero to getSatelliteCount - 1. Value is 0 or greater |

### hasCarrierFrequencyHz

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasCarrierFrequencyHz(satelliteIndex: Int): Boolean
```

Reports whether a valid getCarrierFrequencyHz is available.

| Parameters ||
|---|---|
| `satelliteIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): An index from zero to getSatelliteCount - 1. Value is 0 or greater |

### hasCodeType

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasCodeType(satelliteIndex: Int): Boolean
```

Reports whether a valid #getCodeType() is available.

| Parameters ||
|---|---|
| `satelliteIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): An index from zero to getSatelliteCount - 1. Value is 0 or greater |

### hasElapsedRealtimeNanos

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasElapsedRealtimeNanos(satelliteIndex: Int): Boolean
```

Returns `true` if #getElapsedRealtimeNanos() is available, `false` otherwise.

| Parameters ||
|---|---|
| `satelliteIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is 0 or greater |

### hasElapsedRealtimeUncertaintyNanos

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasElapsedRealtimeUncertaintyNanos(satelliteIndex: Int): Boolean
```

Returns `true` if #getElapsedRealtimeUncertaintyNanos() is available, `false` otherwise.

| Parameters ||
|---|---|
| `satelliteIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is 0 or greater |

### hasEphemerisData

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasEphemerisData(satelliteIndex: Int): Boolean
```

Reports whether the satellite at the specified index has ephemeris data.

| Parameters ||
|---|---|
| `satelliteIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): An index from zero to getSatelliteCount - 1. Value is 0 or greater |

### hashCode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by `https://developer.android.com/reference/kotlin/java/util/HashMap.html#`.

The general contract of `hashCode` is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the `hashCode` method must consistently return the same integer, provided no information used in `equals` comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the equals method, then calling the `hashCode` method on each of the two objects must produce the same integer result.
- It is *not* required that if two objects are unequal according to the equals method, then calling the `hashCode` method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

### usedInFix

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun usedInFix(satelliteIndex: Int): Boolean
```

Reports whether the satellite at the specified index was used in the calculation of the most recent position fix.

This flag must be set to true only if both of the following conditions are met:

1. Fresh data from the respective satellite arrives at the Position Engine (PE).
2. The PE uses this fresh data.

Data is considered fresh as long as it arrives from the Measurement Engine (ME) less than 1 second ago.

If this flag is true, then there must be a corresponding GnssMeasurement reported less than 1 second ago. However, raw measurements reporting must not be affected by this flag.

Note that the PE might use an older measurement for an extended time, but this flag must be set to false in that case.

| Parameters ||
|---|---|
| `satelliteIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): An index from zero to getSatelliteCount - 1. Value is 0 or greater |

### writeToParcel

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    parcel: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |
| `parcel` | [Parcel](../android.os/Parcel.md): This value cannot be `null`. |
| --- | --- |

## Properties

### CREATOR

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<GnssStatus!>
```
