# ResponderLocation

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ResponderLocation

Kotlin| [Java](https://developer.android.com/reference/android/net/wifi/rtt/ResponderLocation "View this page in Java") 
| --- | --- |

```
class ResponderLocation : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.wifi.rtt.ResponderLocation](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderLocation#) |

ResponderLocation is both a Location Configuration Information (LCI) decoder and a Location Civic Report (LCR) decoder for information received from a Wi-Fi Access Point (AP) during Wi-Fi RTT ranging process.

This is based on the IEEE P802.11-REVmc/D8.0 spec section 9.4.2.22, under Measurement Report Element. Subelement location data-fields parsed from separate input LCI and LCR Information Elements are unified in this class.

Note: The information provided by this class is broadcast by a responder (usually an Access Point), and passed on as-is. There is no guarantee this information is accurate or correct, and as a result developers should carefully consider how this information should be used and provide corresponding advice to users.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ALTITUDE_FLOORS](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderLocation#ALTITUDE_FLOORS:kotlin.Int) Responder Altitude is measured in floors. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ALTITUDE_METERS](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderLocation#ALTITUDE_METERS:kotlin.Int) Responder Altitude is measured in meters. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ALTITUDE_UNDEFINED](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderLocation#ALTITUDE_UNDEFINED:kotlin.Int) Altitude is not defined for the Responder. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DATUM_NAD83_MLLW](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderLocation#DATUM_NAD83_MLLW:kotlin.Int) Datum used is NAD83 MLLW. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DATUM_NAD83_NAV88](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderLocation#DATUM_NAD83_NAV88:kotlin.Int) Datum used is NAD83 NAV88. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DATUM_UNDEFINED](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderLocation#DATUM_UNDEFINED:kotlin.Int) Datum is not defined. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DATUM_WGS84](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderLocation#DATUM_WGS84:kotlin.Int) Datum used is WGS84. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LCI_VERSION_1](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderLocation#LCI_VERSION_1:kotlin.Int) Version of the LCI protocol is 1. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LOCATION_FIXED](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderLocation#LOCATION_FIXED:kotlin.Int) Location of responder is fixed (does not move) |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LOCATION_MOVEMENT_UNKNOWN](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderLocation#LOCATION_MOVEMENT_UNKNOWN:kotlin.Int) Location of the responder is not known to be either fixed or variable. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LOCATION_RESERVED](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderLocation#LOCATION_RESERVED:kotlin.Int) Location of the responder status is a reserved value |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LOCATION_VARIABLE](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderLocation#LOCATION_VARIABLE:kotlin.Int) Location of the responder is variable, and may move |
| --- | --- |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderLocation#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderLocation#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [getAltitude](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderLocation#getAltitude())`()` <br /> |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAltitudeType](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderLocation#getAltitudeType())`()` <br /> |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [getAltitudeUncertainty](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderLocation#getAltitudeUncertainty())`()` <br /> |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [MacAddress](https://developer.android.com/reference/kotlin/android/net/MacAddress.html#)!\>! | [getColocatedBssids](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderLocation#getColocatedBssids())`()` <br /> |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDatum](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderLocation#getDatum())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getExpectedToMove](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderLocation#getExpectedToMove())`()` <br /> |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [getFloorNumber](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderLocation#getFloorNumber())`()` <br /> |
| --- | --- |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [getHeightAboveFloorMeters](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderLocation#getHeightAboveFloorMeters())`()` <br /> |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [getHeightAboveFloorUncertaintyMeters](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderLocation#getHeightAboveFloorUncertaintyMeters())`()` <br /> |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [getLatitude](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderLocation#getLatitude())`()` <br /> |
| --- | --- |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [getLatitudeUncertainty](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderLocation#getLatitudeUncertainty())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLciVersion](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderLocation#getLciVersion())`()` <br /> |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [getLongitude](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderLocation#getLongitude())`()` <br /> |
| --- | --- |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [getLongitudeUncertainty](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderLocation#getLongitudeUncertainty())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getMapImageMimeType](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderLocation#getMapImageMimeType())`()` <br /> |
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)? | [getMapImageUri](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderLocation#getMapImageUri())`()` <br /> |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getRegisteredLocationAgreementIndication](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderLocation#getRegisteredLocationAgreementIndication())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderLocation#hashCode())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLciSubelementValid](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderLocation#isLciSubelementValid())`()` <br /> |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isZaxisSubelementValid](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderLocation#isZaxisSubelementValid())`()` <br /> |
| [Address](https://developer.android.com/reference/kotlin/android/location/Address.html#)? | [toCivicLocationAddress](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderLocation#toCivicLocationAddress())`()` <br /> |
| [SparseArray](https://developer.android.com/reference/kotlin/android/util/SparseArray.html#)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>? | [toCivicLocationSparseArray](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderLocation#toCivicLocationSparseArray())`()` <br /> |
| --- | --- |
| [Location](https://developer.android.com/reference/kotlin/android/location/Location.html#) | [toLocation](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderLocation#toLocation())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderLocation#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`parcel:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [ResponderLocation](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderLocation#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderLocation#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### ALTITUDE_FLOORS

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ALTITUDE_FLOORS: Int
```

Responder Altitude is measured in floors. 

 Value: 2

### ALTITUDE_METERS

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ALTITUDE_METERS: Int
```

Responder Altitude is measured in meters. 

 Value: 1

### ALTITUDE_UNDEFINED

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ALTITUDE_UNDEFINED: Int
```

Altitude is not defined for the Responder. The altitude and altitude uncertainty should not be used: see section 2.4 of IETF RFC 6225. 

 Value: 0

### DATUM_NAD83_MLLW

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATUM_NAD83_MLLW: Int
```

Datum used is NAD83 MLLW. 

 Value: 3

### DATUM_NAD83_NAV88

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATUM_NAD83_NAV88: Int
```

Datum used is NAD83 NAV88. 

 Value: 2

### DATUM_UNDEFINED

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATUM_UNDEFINED: Int
```

Datum is not defined. 

 Value: 0

### DATUM_WGS84

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATUM_WGS84: Int
```

Datum used is WGS84. 

 Value: 1

### LCI_VERSION_1

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LCI_VERSION_1: Int
```

Version of the LCI protocol is 1.0, the only defined protocol at this time. 

 Value: 1

### LOCATION_FIXED

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LOCATION_FIXED: Int
```

Location of responder is fixed (does not move) 

 Value: 0

### LOCATION_MOVEMENT_UNKNOWN

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LOCATION_MOVEMENT_UNKNOWN: Int
```

Location of the responder is not known to be either fixed or variable. 

 Value: 2

### LOCATION_RESERVED

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LOCATION_RESERVED: Int
```

Location of the responder status is a reserved value 

 Value: 3

### LOCATION_VARIABLE

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LOCATION_VARIABLE: Int
```

Location of the responder is variable, and may move 

 Value: 1

## Public methods

### describeContents

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### equals

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getAltitude

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAltitude(): Double
```

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the Altitude in units defined by the altitude type. Only valid if [isLciSubelementValid()](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderLocation#isLciSubelementValid())returns true, or will throw an exception. |

### getAltitudeType

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAltitudeType(): Int
```

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the Altitude type. Only valid if [isLciSubelementValid()](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderLocation#isLciSubelementValid())returns true, or will throw an exception. Value is [android.net.wifi.rtt.ResponderLocation#ALTITUDE_UNDEFINED](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderLocation#ALTITUDE_UNDEFINED:kotlin.Int), [android.net.wifi.rtt.ResponderLocation#ALTITUDE_METERS](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderLocation#ALTITUDE_METERS:kotlin.Int), or [android.net.wifi.rtt.ResponderLocation#ALTITUDE_FLOORS](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderLocation#ALTITUDE_FLOORS:kotlin.Int) |

### getAltitudeUncertainty

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAltitudeUncertainty(): Double
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the Altitude uncertainty in meters. Only valid if [isLciSubelementValid()](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderLocation#isLciSubelementValid())returns true, or will throw an exception. An unknown uncertainty is indicated by 0. |

### getColocatedBssids

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getColocatedBssids(): MutableList<MacAddress!>!
```

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [MacAddress](https://developer.android.com/reference/kotlin/android/net/MacAddress.html#)!>! | the Immutable list of colocated BSSIDs at the responder. Will return an empty list when there are no bssids listed. |

### getDatum

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDatum(): Int
```

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the Datum used for the LCI positioning information. Only valid if [isLciSubelementValid()](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderLocation#isLciSubelementValid())returns true, or will throw an exception. Value is [android.net.wifi.rtt.ResponderLocation#DATUM_UNDEFINED](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderLocation#DATUM_UNDEFINED:kotlin.Int), [android.net.wifi.rtt.ResponderLocation#DATUM_WGS84](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderLocation#DATUM_WGS84:kotlin.Int), [android.net.wifi.rtt.ResponderLocation#DATUM_NAD83_NAV88](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderLocation#DATUM_NAD83_NAV88:kotlin.Int), or [android.net.wifi.rtt.ResponderLocation#DATUM_NAD83_MLLW](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderLocation#DATUM_NAD83_MLLW:kotlin.Int) |

### getExpectedToMove

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getExpectedToMove(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | an integer representing the mobility of the responder. Only valid if [isZaxisSubelementValid()](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderLocation#isZaxisSubelementValid())returns true, or will throw an exception. Value is [android.net.wifi.rtt.ResponderLocation#LOCATION_FIXED](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderLocation#LOCATION_FIXED:kotlin.Int), [android.net.wifi.rtt.ResponderLocation#LOCATION_VARIABLE](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderLocation#LOCATION_VARIABLE:kotlin.Int), [android.net.wifi.rtt.ResponderLocation#LOCATION_MOVEMENT_UNKNOWN](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderLocation#LOCATION_MOVEMENT_UNKNOWN:kotlin.Int), or [android.net.wifi.rtt.ResponderLocation#LOCATION_RESERVED](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderLocation#LOCATION_RESERVED:kotlin.Int) |

### getFloorNumber

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFloorNumber(): Double
```

| Return ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the Z sub element Floor Number. Only valid if [isZaxisSubelementValid()](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderLocation#isZaxisSubelementValid())returns true, or will throw an exception. Note: this number can be positive or negative, with value increments of +/- 1/16 of a floor. . |

### getHeightAboveFloorMeters

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getHeightAboveFloorMeters(): Double
```

| Return ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the Z subelement Height above the floor in meters. Only valid if [isZaxisSubelementValid()](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderLocation#isZaxisSubelementValid())returns true, or will throw an exception. This value can be positive or negative. |

### getHeightAboveFloorUncertaintyMeters

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getHeightAboveFloorUncertaintyMeters(): Double
```

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the Z subelement Height above the floor uncertainty in meters. Only valid if [isZaxisSubelementValid()](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderLocation#isZaxisSubelementValid())returns true, or will throw an exception. An unknown uncertainty is indicated by 0. |

### getLatitude

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLatitude(): Double
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the latitude in degrees Only valid if [isLciSubelementValid()](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderLocation#isLciSubelementValid())returns true, or will throw an exception. |

### getLatitudeUncertainty

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLatitudeUncertainty(): Double
```

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the latitude uncertainty in degrees. Only valid if [isLciSubelementValid()](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderLocation#isLciSubelementValid())returns true, or will throw an exception. An unknown uncertainty is indicated by 0. |

### getLciVersion

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLciVersion(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a value greater or equal to 1, indicating the current version number of the LCI protocol. Only valid if [isLciSubelementValid()](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderLocation#isLciSubelementValid())returns true, or will throw an exception. |

### getLongitude

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLongitude(): Double
```

| Return ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the Longitude in degrees.. Only valid if [isLciSubelementValid()](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderLocation#isLciSubelementValid())returns true, or will throw an exception. |

### getLongitudeUncertainty

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLongitudeUncertainty(): Double
```

| Return ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the Longitude uncertainty in degrees. Only valid if [isLciSubelementValid()](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderLocation#isLciSubelementValid())returns true, or will throw an exception. An unknown uncertainty is indicated by 0. |

### getMapImageMimeType

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMapImageMimeType(): String?
```

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | the Map Image file Mime type, referred to by getMapImageUrl(). This value may be`null`. |

### getMapImageUri

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMapImageUri(): Uri?
```

| Return ||
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)? | a URI referencing a map-file showing the local floor plan. Will return a`null`when there is no URI defined. |

### getRegisteredLocationAgreementIndication

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRegisteredLocationAgreementIndication(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the station is operating within a national policy area or an international agreement area near a national border, otherwise false (see 802.11REVmc Section 11.12.3 - Registered STA Operation). Only valid if [isLciSubelementValid()](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderLocation#isLciSubelementValid())returns true, or will throw an exception. |

### hashCode

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### isLciSubelementValid

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isLciSubelementValid(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the LCI subelement (containing Latitude, Longitude and Altitude) is valid. This method tells us if the responder has provided its Location Configuration Information (LCI) directly, and is useful when an external database of responder locations is not available If isLciSubelementValid() returns true, all the LCI values provided by the corresponding getter methods will have been set as described by the responder, or else if false, they should not be used and will throw an IllegalStateException. |

### isZaxisSubelementValid

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isZaxisSubelementValid(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | if the Z subelement (containing mobility, Floor, Height above floor) is valid. |

### toCivicLocationAddress

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toCivicLocationAddress(): Address?
```

| Return ||
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Address](https://developer.android.com/reference/kotlin/android/location/Address.html#)? | the civic location represented as an [Address](https://developer.android.com/reference/kotlin/android/location/Address.html#) object (best effort). Will return a`null`when there is no Civic Location defined. |

### toCivicLocationSparseArray

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toCivicLocationSparseArray(): SparseArray<String!>?
```

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [SparseArray](https://developer.android.com/reference/kotlin/android/util/SparseArray.html#)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>? | the civic location represented as a [SparseArray](https://developer.android.com/reference/kotlin/android/util/SparseArray.html#) Valid keys to access the SparseArray can be found in`CivicLocationKeys`. Will return a`null`when there is no Civic Location defined. |

### toLocation

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toLocation(): Location
```

| Return ||
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Location](https://developer.android.com/reference/kotlin/android/location/Location.html#) | the LCI location represented as a [Location](https://developer.android.com/reference/kotlin/android/location/Location.html#) object (best effort). Only valid if [isLciSubelementValid()](https://developer.android.com/reference/kotlin/android/net/wifi/rtt/ResponderLocation#isLciSubelementValid())returns true, or will throw an exception. This value cannot be`null`. |

### writeToParcel

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    parcel: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<ResponderLocation!>
```
