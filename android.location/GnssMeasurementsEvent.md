# GnssMeasurementsEvent

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GnssMeasurementsEvent

Kotlin| [Java](https://developer.android.com/reference/android/location/GnssMeasurementsEvent "View this page in Java") 
| --- | --- |

```
class GnssMeasurementsEvent : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.location.GnssMeasurementsEvent](https://developer.android.com/reference/kotlin/android/location/GnssMeasurementsEvent#) |

A class implementing a container for data associated with a measurement event. Events are delivered to registered instances of [Callback](https://developer.android.com/reference/kotlin/android/location/GnssMeasurementsEvent.Callback).

## Summary

| Nested classes ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/location/GnssMeasurementsEvent.Builder) Builder for [GnssMeasurementsEvent](https://developer.android.com/reference/kotlin/android/location/GnssMeasurementsEvent#) |
| abstract | [Callback](https://developer.android.com/reference/kotlin/android/location/GnssMeasurementsEvent.Callback) Used for receiving GNSS satellite measurements from the GNSS engine. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/location/GnssMeasurementsEvent#describeContents())`()` <br /> |
| [GnssClock](https://developer.android.com/reference/kotlin/android/location/GnssClock) | [getClock](https://developer.android.com/reference/kotlin/android/location/GnssMeasurementsEvent#getClock())`()` Gets the GNSS receiver clock information associated with the measurements for the current event. |
| [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [GnssAutomaticGainControl](https://developer.android.com/reference/kotlin/android/location/GnssAutomaticGainControl)!\> | [getGnssAutomaticGainControls](https://developer.android.com/reference/kotlin/android/location/GnssMeasurementsEvent#getGnssAutomaticGainControls())`()` Gets the collection of [GnssAutomaticGainControl](https://developer.android.com/reference/kotlin/android/location/GnssAutomaticGainControl) associated with the current event. |
| --- | --- |
| [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [GnssMeasurement](https://developer.android.com/reference/kotlin/android/location/GnssMeasurement)!\> | [getMeasurements](https://developer.android.com/reference/kotlin/android/location/GnssMeasurementsEvent#getMeasurements())`()` Gets the collection of measurements associated with the current event. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasIsFullTracking](https://developer.android.com/reference/kotlin/android/location/GnssMeasurementsEvent#hasIsFullTracking())`()` Return`true`if [isFullTracking()](https://developer.android.com/reference/kotlin/android/location/GnssMeasurementsEvent#isFullTracking())is available,`false`otherwise. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isFullTracking](https://developer.android.com/reference/kotlin/android/location/GnssMeasurementsEvent#isFullTracking())`()` True indicates that this event was produced while the chipset was in full tracking mode, ie, the GNSS chipset switched off duty cycling. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/location/GnssMeasurementsEvent#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/location/GnssMeasurementsEvent#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`parcel:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [GnssMeasurementsEvent](https://developer.android.com/reference/kotlin/android/location/GnssMeasurementsEvent#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/location/GnssMeasurementsEvent#CREATOR:android.os.Parcelable.Creator) <br /> |

## Public methods

### describeContents

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getClock

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getClock(): GnssClock
```

Gets the GNSS receiver clock information associated with the measurements for the current event.

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------|
| [GnssClock](https://developer.android.com/reference/kotlin/android/location/GnssClock) | This value cannot be`null`. |

### getGnssAutomaticGainControls

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getGnssAutomaticGainControls(): MutableCollection<GnssAutomaticGainControl!>
```

Gets the collection of [GnssAutomaticGainControl](https://developer.android.com/reference/kotlin/android/location/GnssAutomaticGainControl) associated with the current event.

This field must be reported when the GNSS measurement engine is running, even when the GnssMeasurement or GnssClock fields are not reported yet. E.g., when a GNSS signal is too weak to be acquired, the AGC value must still be reported.

For devices that do not support this field, an empty collection is returned. In that case, please use [GnssMeasurement.hasAutomaticGainControlLevelDb()](https://developer.android.com/reference/kotlin/android/location/GnssMeasurement#hasAutomaticGainControlLevelDb())and GnssMeasuremen#getAutomaticGainControlLevelDb().

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)< [GnssAutomaticGainControl](https://developer.android.com/reference/kotlin/android/location/GnssAutomaticGainControl)!> | This value cannot be`null`. |

### getMeasurements

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMeasurements(): MutableCollection<GnssMeasurement!>
```

Gets the collection of measurements associated with the current event.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)< [GnssMeasurement](https://developer.android.com/reference/kotlin/android/location/GnssMeasurement)!> | This value cannot be`null`. |

### hasIsFullTracking

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasIsFullTracking(): Boolean
```

Return`true`if [isFullTracking()](https://developer.android.com/reference/kotlin/android/location/GnssMeasurementsEvent#isFullTracking())is available,`false`otherwise. 

### isFullTracking

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isFullTracking(): Boolean
```

True indicates that this event was produced while the chipset was in full tracking mode, ie, the GNSS chipset switched off duty cycling. In this mode, no clock discontinuities are expected and, when supported, carrier phase should be continuous in good signal conditions. All non-blocklisted, healthy constellations, satellites and frequency bands that are meaningful to positioning accuracy must be tracked and reported in this mode. False indicates that the GNSS chipset may optimize power via duty cycling, constellations and frequency limits, etc.

The value is only available if [hasIsFullTracking()](https://developer.android.com/reference/kotlin/android/location/GnssMeasurementsEvent#hasIsFullTracking())is`true`. 

### toString

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<GnssMeasurementsEvent!>
```
