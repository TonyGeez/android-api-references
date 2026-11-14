# GnssMeasurementsEvent

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GnssMeasurementsEvent

Kotlin| [Java](../android/location/GnssMeasurementsEvent.md) 
| --- | --- |

```
class GnssMeasurementsEvent : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.location.GnssMeasurementsEvent](../android/location/GnssMeasurementsEvent.md) |

A class implementing a container for data associated with a measurement event. Events are delivered to registered instances of [Callback](../android/location/GnssMeasurementsEvent.Callback.md).

## Summary

| Nested classes ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/location/GnssMeasurementsEvent.Builder.md) Builder for [GnssMeasurementsEvent](../android/location/GnssMeasurementsEvent.md) |
| abstract | [Callback](../android/location/GnssMeasurementsEvent.Callback.md) Used for receiving GNSS satellite measurements from the GNSS engine. |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/location/GnssMeasurementsEvent.md))`()` <br /> |
| [GnssClock](../android/location/GnssClock.md) | [getClock](../android/location/GnssMeasurementsEvent.md))`()` Gets the GNSS receiver clock information associated with the measurements for the current event. |
| [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [GnssAutomaticGainControl](../android/location/GnssAutomaticGainControl.md)!\> | [getGnssAutomaticGainControls](../android/location/GnssMeasurementsEvent.md))`()` Gets the collection of [GnssAutomaticGainControl](../android/location/GnssAutomaticGainControl.md) associated with the current event. |
| --- | --- |
| [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [GnssMeasurement](../android/location/GnssMeasurement.md)!\> | [getMeasurements](../android/location/GnssMeasurementsEvent.md))`()` Gets the collection of measurements associated with the current event. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasIsFullTracking](../android/location/GnssMeasurementsEvent.md))`()` Return`true`if [isFullTracking()](../android/location/GnssMeasurementsEvent.md))is available,`false`otherwise. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isFullTracking](../android/location/GnssMeasurementsEvent.md))`()` True indicates that this event was produced while the chipset was in full tracking mode, ie, the GNSS chipset switched off duty cycling. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/location/GnssMeasurementsEvent.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/location/GnssMeasurementsEvent.md))`(`parcel:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [GnssMeasurementsEvent](../android/location/GnssMeasurementsEvent.md)!\> | [CREATOR](../android/location/GnssMeasurementsEvent.md) <br /> |

## Public methods

### describeContents

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### getClock

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getClock(): GnssClock
```

Gets the GNSS receiver clock information associated with the measurements for the current event.

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------|
| [GnssClock](../android/location/GnssClock.md) | This value cannot be`null`. |

### getGnssAutomaticGainControls

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getGnssAutomaticGainControls(): MutableCollection<GnssAutomaticGainControl!>
```

Gets the collection of [GnssAutomaticGainControl](../android/location/GnssAutomaticGainControl.md) associated with the current event.

This field must be reported when the GNSS measurement engine is running, even when the GnssMeasurement or GnssClock fields are not reported yet. E.g., when a GNSS signal is too weak to be acquired, the AGC value must still be reported.

For devices that do not support this field, an empty collection is returned. In that case, please use [GnssMeasurement.hasAutomaticGainControlLevelDb()](../android/location/GnssMeasurement.md))and GnssMeasuremen#getAutomaticGainControlLevelDb().

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)< [GnssAutomaticGainControl](../android/location/GnssAutomaticGainControl.md)!> | This value cannot be`null`. |

### getMeasurements

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMeasurements(): MutableCollection<GnssMeasurement!>
```

Gets the collection of measurements associated with the current event.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)< [GnssMeasurement](../android/location/GnssMeasurement.md)!> | This value cannot be`null`. |

### hasIsFullTracking

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasIsFullTracking(): Boolean
```

Return`true`if [isFullTracking()](../android/location/GnssMeasurementsEvent.md))is available,`false`otherwise. 

### isFullTracking

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isFullTracking(): Boolean
```

True indicates that this event was produced while the chipset was in full tracking mode, ie, the GNSS chipset switched off duty cycling. In this mode, no clock discontinuities are expected and, when supported, carrier phase should be continuous in good signal conditions. All non-blocklisted, healthy constellations, satellites and frequency bands that are meaningful to positioning accuracy must be tracked and reported in this mode. False indicates that the GNSS chipset may optimize power via duty cycling, constellations and frequency limits, etc.

The value is only available if [hasIsFullTracking()](../android/location/GnssMeasurementsEvent.md))is`true`. 

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
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<GnssMeasurementsEvent!>
```
