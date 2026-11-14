# CdmaCellLocation

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CdmaCellLocation

Kotlin| [Java](../android/telephony/cdma/CdmaCellLocation.md) 
| --- | --- |

```
open class CdmaCellLocation : CellLocation
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.telephony.CellLocation](../android/telephony/CellLocation.md) ||
| | ↳ | [android.telephony.cdma.CdmaCellLocation](../android/telephony/cdma/CdmaCellLocation.md) |

| **This class was deprecated in API level 31.**
|
| use [CellIdentity](../android/telephony/CellIdentity.md).

Represents the cell location on a CDMA phone.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CdmaCellLocation](../android/telephony/cdma/CdmaCellLocation.md))`()` Empty constructor. |
| [CdmaCellLocation](../android/telephony/cdma/CdmaCellLocation.md))`(`bundle:` ` [Bundle](../android/os/Bundle.md)!`)` Initialize the object from a bundle. |

| Public methods ||
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [convertQuartSecToDecDegrees](../android/telephony/cdma/CdmaCellLocation.md))`(`quartSec:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Converts latitude or longitude from 0. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/telephony/cdma/CdmaCellLocation.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [fillInNotifierBundle](../android/telephony/cdma/CdmaCellLocation.md))`(`bundleToFill:` ` [Bundle](../android/os/Bundle.md)!`)` Fill the cell location data into the intent notifier Bundle based on service state |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getBaseStationId](../android/telephony/cdma/CdmaCellLocation.md))`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getBaseStationLatitude](../android/telephony/cdma/CdmaCellLocation.md))`()` Latitude is a decimal number as specified in 3GPP2 C. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getBaseStationLongitude](../android/telephony/cdma/CdmaCellLocation.md))`()` Longitude is a decimal number as specified in 3GPP2 C. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getNetworkId](../android/telephony/cdma/CdmaCellLocation.md))`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSystemId](../android/telephony/cdma/CdmaCellLocation.md))`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/telephony/cdma/CdmaCellLocation.md))`()` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCellLocationData](../android/telephony/cdma/CdmaCellLocation.md))`(`baseStationId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `baseStationLatitude:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `baseStationLongitude:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the cell location data. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCellLocationData](../android/telephony/cdma/CdmaCellLocation.md))`(`baseStationId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `baseStationLatitude:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `baseStationLongitude:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `systemId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `networkId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the cell location data. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStateInvalid](../android/telephony/cdma/CdmaCellLocation.md))`()` Invalidate this object. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/telephony/cdma/CdmaCellLocation.md))`()` <br /> |

| Inherited functions ||
|---|---|
| From class [CellLocation](../android/telephony/CellLocation.md) |------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [CellLocation](../android/telephony/CellLocation.md)! | [getEmpty](../android/telephony/CellLocation.md))`()` <br /> Return a new CellLocation object representing an unknown location, or null for unknown/none phone radio types. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestLocationUpdate](../android/telephony/CellLocation.md))`()` <br /> Request an updated CellLocation for callers targeting SDK 30 or older. Whenever Android is aware of location changes, a callback will automatically be sent to all registrants of [PhoneStateListener.LISTEN_CELL_LOCATION](../android/telephony/PhoneStateListener.md). This API requests an additional location update for cases where power saving might cause location updates to be missed. This method is a no-op for callers targeting SDK level 31 or greater. This method is a no-op for callers that target SDK level 29 or 30 and lack [android.Manifest.permission#ACCESS_FINE_LOCATION](../android/Manifest.permission.md). This method is a no-op for callers that target SDK level 28 or below and lack [android.Manifest.permission#ACCESS_COARSE_LOCATION](../android/Manifest.permission.md). <br /> | ||

## Public constructors

### CdmaCellLocation

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CdmaCellLocation()
```

Empty constructor. Initializes the BID, SID, NID and base station latitude and longitude to invalid values. 

### CdmaCellLocation

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CdmaCellLocation(bundle: Bundle!)
```

Initialize the object from a bundle.

## Public methods

### convertQuartSecToDecDegrees

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun convertQuartSecToDecDegrees(quartSec: Int): Double
```

**Deprecated:** *Deprecated in Java.*

Converts latitude or longitude from 0.25 seconds (as defined in the 3GPP2 C.S0005-A v6.0 standard) to decimal degrees

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------|
| `quartSec` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):latitude or longitude in 0.25 seconds units |

| Return ||
|----------------------------------------------------------------------------------|------------------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | latitude or longitude in decimal degrees units |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if value is less than -2592000, greater than 2592000, or is not a number. |

### equals

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### fillInNotifierBundle

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun fillInNotifierBundle(bundleToFill: Bundle!): Unit
```

**Deprecated:** *Deprecated in Java.*

Fill the cell location data into the intent notifier Bundle based on service state

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------|
| `bundleToFill` | [Bundle](../android/os/Bundle.md)!:intent notifier Bundle |

### getBaseStationId

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getBaseStationId(): Int
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | cdma base station identification number, -1 if unknown |

### getBaseStationLatitude

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getBaseStationLatitude(): Int
```

**Deprecated:** *Deprecated in Java.*

Latitude is a decimal number as specified in 3GPP2 C.S0005-A v6.0. (http://www.3gpp2.org/public_html/specs/C.S0005-A_v6.0.pdf) It is represented in units of 0.25 seconds and ranges from -1296000 to 1296000, both values inclusive (corresponding to a range of -90 to +90 degrees). Integer.MAX_VALUE is considered invalid value.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | cdma base station latitude in units of 0.25 seconds, Integer.MAX_VALUE if unknown |

### getBaseStationLongitude

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getBaseStationLongitude(): Int
```

**Deprecated:** *Deprecated in Java.*

Longitude is a decimal number as specified in 3GPP2 C.S0005-A v6.0. (http://www.3gpp2.org/public_html/specs/C.S0005-A_v6.0.pdf) It is represented in units of 0.25 seconds and ranges from -2592000 to 2592000, both values inclusive (corresponding to a range of -180 to +180 degrees). Integer.MAX_VALUE is considered invalid value.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | cdma base station longitude in units of 0.25 seconds, Integer.MAX_VALUE if unknown |

### getNetworkId

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getNetworkId(): Int
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | cdma network identification number, -1 if unknown |

### getSystemId

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSystemId(): Int
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | cdma system identification number, -1 if unknown |

### hashCode

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### setCellLocationData

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setCellLocationData(
    baseStationId: Int, 
    baseStationLatitude: Int, 
    baseStationLongitude: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

Set the cell location data. 

### setCellLocationData

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setCellLocationData(
    baseStationId: Int, 
    baseStationLatitude: Int, 
    baseStationLongitude: Int, 
    systemId: Int, 
    networkId: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

Set the cell location data. 

### setStateInvalid

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setStateInvalid(): Unit
```

**Deprecated:** *Deprecated in Java.*

Invalidate this object. The cell location data is set to invalid values. 

### toString

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |
