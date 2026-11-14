# GnssCapabilities

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GnssCapabilities

Kotlin| [Java](https://developer.android.com/reference/android/location/GnssCapabilities "View this page in Java") 

```
class GnssCapabilities : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.location.GnssCapabilities](https://developer.android.com/reference/kotlin/android/location/GnssCapabilities#) |

GNSS chipset capabilities.

## Summary

| Nested classes ||
|---|-----------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/location/GnssCapabilities.Builder) Builder for GnssCapabilities. |

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CAPABILITY_SUPPORTED](https://developer.android.com/reference/kotlin/android/location/GnssCapabilities#CAPABILITY_SUPPORTED:kotlin.Int) The capability is supported. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CAPABILITY_UNKNOWN](https://developer.android.com/reference/kotlin/android/location/GnssCapabilities#CAPABILITY_UNKNOWN:kotlin.Int) The capability is unknown to be supported or not. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CAPABILITY_UNSUPPORTED](https://developer.android.com/reference/kotlin/android/location/GnssCapabilities#CAPABILITY_UNSUPPORTED:kotlin.Int) The capability is not supported. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/location/GnssCapabilities#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/location/GnssCapabilities#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [GnssSignalType](https://developer.android.com/reference/kotlin/android/location/GnssSignalType)!\> | [getGnssSignalTypes](https://developer.android.com/reference/kotlin/android/location/GnssCapabilities#getGnssSignalTypes())`()` Returns the list of [GnssSignalType](https://developer.android.com/reference/kotlin/android/location/GnssSignalType) s that the GNSS chipset supports. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hasAccumulatedDeltaRange](https://developer.android.com/reference/kotlin/android/location/GnssCapabilities#hasAccumulatedDeltaRange())`()` Returns [CAPABILITY_SUPPORTED](https://developer.android.com/reference/kotlin/android/location/GnssCapabilities#CAPABILITY_SUPPORTED:kotlin.Int) if GNSS chipset supports accumulated delta range, [CAPABILITY_UNSUPPORTED](https://developer.android.com/reference/kotlin/android/location/GnssCapabilities#CAPABILITY_UNSUPPORTED:kotlin.Int) if GNSS chipset does not support accumulated delta range, and [CAPABILITY_UNKNOWN](https://developer.android.com/reference/kotlin/android/location/GnssCapabilities#CAPABILITY_UNKNOWN:kotlin.Int) if it is unknown, which means GNSS chipset may or may not support accumulated delta range. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasAntennaInfo](https://developer.android.com/reference/kotlin/android/location/GnssCapabilities#hasAntennaInfo())`()` Returns`true`if GNSS chipset supports antenna info,`false`otherwise. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasGeofencing](https://developer.android.com/reference/kotlin/android/location/GnssCapabilities#hasGeofencing())`()` Returns`true`if GNSS chipset supports geofencing,`false`otherwise. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasGnssAntennaInfo](https://developer.android.com/reference/kotlin/android/location/GnssCapabilities#hasGnssAntennaInfo())`()` Returns`true`if GNSS chipset supports antenna info,`false`otherwise. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasLowPowerMode](https://developer.android.com/reference/kotlin/android/location/GnssCapabilities#hasLowPowerMode())`()` Returns`true`if GNSS chipset supports low power mode,`false`otherwise. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasMeasurementCorrections](https://developer.android.com/reference/kotlin/android/location/GnssCapabilities#hasMeasurementCorrections())`()` Returns`true`if GNSS chipset supports measurement corrections,`false`otherwise. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasMeasurementCorrectionsExcessPathLength](https://developer.android.com/reference/kotlin/android/location/GnssCapabilities#hasMeasurementCorrectionsExcessPathLength())`()` Returns`true`if GNSS chipset supports per satellite excess-path-length measurement corrections,`false`otherwise. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasMeasurementCorrectionsForDriving](https://developer.android.com/reference/kotlin/android/location/GnssCapabilities#hasMeasurementCorrectionsForDriving())`()` Returns`true`if GNSS chipset will benefit from measurement corrections for driving use case if provided,`false`otherwise. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasMeasurementCorrectionsLosSats](https://developer.android.com/reference/kotlin/android/location/GnssCapabilities#hasMeasurementCorrectionsLosSats())`()` Returns`true`if GNSS chipset supports line-of-sight satellite identification measurement corrections,`false`otherwise. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasMeasurementCorrectionsReflectingPlane](https://developer.android.com/reference/kotlin/android/location/GnssCapabilities#hasMeasurementCorrectionsReflectingPlane())`()` Returns`true`if GNSS chipset supports reflecting plane measurement corrections,`false`otherwise. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasMeasurementCorrelationVectors](https://developer.android.com/reference/kotlin/android/location/GnssCapabilities#hasMeasurementCorrelationVectors())`()` Returns`true`if GNSS chipset supports correlation vectors as part of measurements outputs,`false`otherwise. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasMeasurements](https://developer.android.com/reference/kotlin/android/location/GnssCapabilities#hasMeasurements())`()` Returns`true`if GNSS chipset supports measurements,`false`otherwise. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasMsa](https://developer.android.com/reference/kotlin/android/location/GnssCapabilities#hasMsa())`()` Returns`true`if GNSS chipset supports Mobile Station Assisted assitance,`false`otherwise. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasMsb](https://developer.android.com/reference/kotlin/android/location/GnssCapabilities#hasMsb())`()` Returns`true`if GNSS chipset supports Mobile Station Based assistance,`false`otherwise. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasNavigationMessages](https://developer.android.com/reference/kotlin/android/location/GnssCapabilities#hasNavigationMessages())`()` Returns`true`if GNSS chipset supports navigation messages,`false`otherwise. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasOnDemandTime](https://developer.android.com/reference/kotlin/android/location/GnssCapabilities#hasOnDemandTime())`()` Returns`true`if GNSS chipset requests periodic time signal injection from the platform in addition to on-demand and occasional time updates,`false`otherwise. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasPowerMultibandAcquisition](https://developer.android.com/reference/kotlin/android/location/GnssCapabilities#hasPowerMultibandAcquisition())`()` Returns`true`if GNSS chipset supports measuring multi-band acquisition power,`false`otherwise. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasPowerMultibandTracking](https://developer.android.com/reference/kotlin/android/location/GnssCapabilities#hasPowerMultibandTracking())`()` Returns`true`if GNSS chipset supports measuring multi-band tracking power,`false`otherwise. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasPowerOtherModes](https://developer.android.com/reference/kotlin/android/location/GnssCapabilities#hasPowerOtherModes())`()` Returns`true`if GNSS chipset supports measuring OEM defined mode power,`false`otherwise. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasPowerSinglebandAcquisition](https://developer.android.com/reference/kotlin/android/location/GnssCapabilities#hasPowerSinglebandAcquisition())`()` Returns`true`if GNSS chipset supports measuring single-band acquisition power,`false`otherwise. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasPowerSinglebandTracking](https://developer.android.com/reference/kotlin/android/location/GnssCapabilities#hasPowerSinglebandTracking())`()` Returns`true`if GNSS chipset supports measuring single-band tracking power,`false`otherwise. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasPowerTotal](https://developer.android.com/reference/kotlin/android/location/GnssCapabilities#hasPowerTotal())`()` Returns`true`if GNSS chipset supports measuring power totals,`false`otherwise. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasSatelliteBlocklist](https://developer.android.com/reference/kotlin/android/location/GnssCapabilities#hasSatelliteBlocklist())`()` Returns`true`if GNSS chipset supports satellite blocklists,`false`otherwise. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasSatellitePvt](https://developer.android.com/reference/kotlin/android/location/GnssCapabilities#hasSatellitePvt())`()` Returns`true`if GNSS chipset supports satellite PVT,`false`otherwise. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasScheduling](https://developer.android.com/reference/kotlin/android/location/GnssCapabilities#hasScheduling())`()` Returns`true`if GNSS chipset supports scheduling,`false`otherwise. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasSingleShotFix](https://developer.android.com/reference/kotlin/android/location/GnssCapabilities#hasSingleShotFix())`()` Returns`true`if GNSS chipset supports single shot locating,`false`otherwise. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/location/GnssCapabilities#hashCode())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/location/GnssCapabilities#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/location/GnssCapabilities#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`parcel:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [GnssCapabilities](https://developer.android.com/reference/kotlin/android/location/GnssCapabilities#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/location/GnssCapabilities#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### CAPABILITY_SUPPORTED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CAPABILITY_SUPPORTED: Int
```

The capability is supported. 

 Value: 1

### CAPABILITY_UNKNOWN

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CAPABILITY_UNKNOWN: Int
```

The capability is unknown to be supported or not. 

 Value: 0

### CAPABILITY_UNSUPPORTED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CAPABILITY_UNSUPPORTED: Int
```

The capability is not supported. 

 Value: 2

## Public methods

### describeContents

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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

### getGnssSignalTypes

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getGnssSignalTypes(): MutableList<GnssSignalType!>
```

Returns the list of [GnssSignalType](https://developer.android.com/reference/kotlin/android/location/GnssSignalType) s that the GNSS chipset supports.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [GnssSignalType](https://developer.android.com/reference/kotlin/android/location/GnssSignalType)!> | This value cannot be`null`. |

### hasAccumulatedDeltaRange

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasAccumulatedDeltaRange(): Int
```

Returns [CAPABILITY_SUPPORTED](https://developer.android.com/reference/kotlin/android/location/GnssCapabilities#CAPABILITY_SUPPORTED:kotlin.Int) if GNSS chipset supports accumulated delta range, [CAPABILITY_UNSUPPORTED](https://developer.android.com/reference/kotlin/android/location/GnssCapabilities#CAPABILITY_UNSUPPORTED:kotlin.Int) if GNSS chipset does not support accumulated delta range, and [CAPABILITY_UNKNOWN](https://developer.android.com/reference/kotlin/android/location/GnssCapabilities#CAPABILITY_UNKNOWN:kotlin.Int) if it is unknown, which means GNSS chipset may or may not support accumulated delta range.

The accumulated delta range information can be queried in [android.location.GnssMeasurement#getAccumulatedDeltaRangeState()](https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getAccumulatedDeltaRangeState()), [android.location.GnssMeasurement#getAccumulatedDeltaRangeMeters()](https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getAccumulatedDeltaRangeMeters()), and [android.location.GnssMeasurement#getAccumulatedDeltaRangeUncertaintyMeters()](https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#getAccumulatedDeltaRangeUncertaintyMeters()).

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is either`0`or a combination of [android.location.GnssCapabilities#CAPABILITY_UNKNOWN](https://developer.android.com/reference/kotlin/android/location/GnssCapabilities#CAPABILITY_UNKNOWN:kotlin.Int), [android.location.GnssCapabilities#CAPABILITY_SUPPORTED](https://developer.android.com/reference/kotlin/android/location/GnssCapabilities#CAPABILITY_SUPPORTED:kotlin.Int), and [android.location.GnssCapabilities#CAPABILITY_UNSUPPORTED](https://developer.android.com/reference/kotlin/android/location/GnssCapabilities#CAPABILITY_UNSUPPORTED:kotlin.Int) |

### hasAntennaInfo

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasAntennaInfo(): Boolean
```

Returns`true`if GNSS chipset supports antenna info,`false`otherwise. 
**See Also**

- [android.location.LocationManager#registerAntennaInfoListener(Executor, GnssAntennaInfo.Listener)](https://developer.android.com/reference/kotlin/android/location/LocationManager#registerAntennaInfoListener(java.util.concurrent.Executor,%20android.location.GnssAntennaInfo.Listener)) 

### hasGeofencing

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasGeofencing(): Boolean
```

Returns`true`if GNSS chipset supports geofencing,`false`otherwise. 

### hasGnssAntennaInfo

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasGnssAntennaInfo(): Boolean
```

**Deprecated:** *Use [hasAntennaInfo()](https://developer.android.com/reference/kotlin/android/location/GnssCapabilities#hasAntennaInfo())instead.*

Returns`true`if GNSS chipset supports antenna info,`false`otherwise. 

### hasLowPowerMode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasLowPowerMode(): Boolean
```

Returns`true`if GNSS chipset supports low power mode,`false`otherwise.

The low power mode is defined in GNSS HAL. When the low power mode is active, the GNSS hardware must make strong tradeoffs to substantially restrict power use. 

### hasMeasurementCorrections

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasMeasurementCorrections(): Boolean
```

Returns`true`if GNSS chipset supports measurement corrections,`false`otherwise. 

### hasMeasurementCorrectionsExcessPathLength

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasMeasurementCorrectionsExcessPathLength(): Boolean
```

Returns`true`if GNSS chipset supports per satellite excess-path-length measurement corrections,`false`otherwise. 

### hasMeasurementCorrectionsForDriving

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasMeasurementCorrectionsForDriving(): Boolean
```

Returns`true`if GNSS chipset will benefit from measurement corrections for driving use case if provided,`false`otherwise. 

### hasMeasurementCorrectionsLosSats

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasMeasurementCorrectionsLosSats(): Boolean
```

Returns`true`if GNSS chipset supports line-of-sight satellite identification measurement corrections,`false`otherwise. 

### hasMeasurementCorrectionsReflectingPlane

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasMeasurementCorrectionsReflectingPlane(): Boolean
```

Returns`true`if GNSS chipset supports reflecting plane measurement corrections,`false`otherwise. 

### hasMeasurementCorrelationVectors

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasMeasurementCorrelationVectors(): Boolean
```

Returns`true`if GNSS chipset supports correlation vectors as part of measurements outputs,`false`otherwise. 

### hasMeasurements

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasMeasurements(): Boolean
```

Returns`true`if GNSS chipset supports measurements,`false`otherwise. 
**See Also**

- [android.location.LocationManager#registerGnssMeasurementsCallback(Executor, GnssMeasurementsEvent.Callback)](https://developer.android.com/reference/kotlin/android/location/LocationManager#registerGnssMeasurementsCallback(java.util.concurrent.Executor,%20android.location.GnssMeasurementsEvent.Callback)) 

### hasMsa

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasMsa(): Boolean
```

Returns`true`if GNSS chipset supports Mobile Station Assisted assitance,`false`otherwise. 

### hasMsb

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasMsb(): Boolean
```

Returns`true`if GNSS chipset supports Mobile Station Based assistance,`false`otherwise. 

### hasNavigationMessages

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasNavigationMessages(): Boolean
```

Returns`true`if GNSS chipset supports navigation messages,`false`otherwise. 
**See Also**

- [android.location.LocationManager#registerGnssNavigationMessageCallback(Executor, GnssNavigationMessage.Callback)](https://developer.android.com/reference/kotlin/android/location/LocationManager#registerGnssNavigationMessageCallback(java.util.concurrent.Executor,%20android.location.GnssNavigationMessage.Callback)) 

### hasOnDemandTime

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasOnDemandTime(): Boolean
```

Returns`true`if GNSS chipset requests periodic time signal injection from the platform in addition to on-demand and occasional time updates,`false`otherwise.

*Note: The naming of this capability and the behavior it controls differ substantially. This is the result of a historic implementation bug, b/73893222.* 

### hasPowerMultibandAcquisition

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasPowerMultibandAcquisition(): Boolean
```

Returns`true`if GNSS chipset supports measuring multi-band acquisition power,`false`otherwise. 

### hasPowerMultibandTracking

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasPowerMultibandTracking(): Boolean
```

Returns`true`if GNSS chipset supports measuring multi-band tracking power,`false`otherwise. 

### hasPowerOtherModes

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasPowerOtherModes(): Boolean
```

Returns`true`if GNSS chipset supports measuring OEM defined mode power,`false`otherwise. 

### hasPowerSinglebandAcquisition

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasPowerSinglebandAcquisition(): Boolean
```

Returns`true`if GNSS chipset supports measuring single-band acquisition power,`false`otherwise. 

### hasPowerSinglebandTracking

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasPowerSinglebandTracking(): Boolean
```

Returns`true`if GNSS chipset supports measuring single-band tracking power,`false`otherwise. 

### hasPowerTotal

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasPowerTotal(): Boolean
```

Returns`true`if GNSS chipset supports measuring power totals,`false`otherwise. 

### hasSatelliteBlocklist

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasSatelliteBlocklist(): Boolean
```

Returns`true`if GNSS chipset supports satellite blocklists,`false`otherwise. 

### hasSatellitePvt

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasSatellitePvt(): Boolean
```

Returns`true`if GNSS chipset supports satellite PVT,`false`otherwise. 

### hasScheduling

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasScheduling(): Boolean
```

Returns`true`if GNSS chipset supports scheduling,`false`otherwise. 

### hasSingleShotFix

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasSingleShotFix(): Boolean
```

Returns`true`if GNSS chipset supports single shot locating,`false`otherwise. 

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

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<GnssCapabilities!>
```
