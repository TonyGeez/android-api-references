Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GnssClock

Kotlin | [Java](GnssClock.md)
| --- | --- |

```
class GnssClock : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.location.GnssClock](GnssClock.md) |

A class containing a GNSS clock timestamp.

It represents a measurement of the GNSS receiver's clock.

## Summary

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with describeContents: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with writeToParcel: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | describeContents Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | getBiasNanos Gets the clock's sub-nanosecond bias. |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | getBiasUncertaintyNanos Gets the clock's Bias Uncertainty (1-Sigma) in nanoseconds. |
| --- | --- |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | getDriftNanosPerSecond Gets the clock's Drift in nanoseconds per second. |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | getDriftUncertaintyNanosPerSecond Gets the clock's Drift Uncertainty (1-Sigma) in nanoseconds per second. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | getElapsedRealtimeNanos Returns the elapsed real-time of this clock since system boot, in nanoseconds. |
| --- | --- |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | getElapsedRealtimeUncertaintyNanos Gets the estimate of the relative precision of the alignment of the getElapsedRealtimeNanos timestamp, with the reported measurements in nanoseconds (68% confidence). |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | getFullBiasNanos Gets the difference between hardware clock (getTimeNanos) inside GPS receiver and the true GPS time since 0000Z, January 6, 1980, in nanoseconds. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getHardwareClockDiscontinuityCount Gets count of hardware clock discontinuities. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getLeapSecond Gets the leap second associated with the clock's time. |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | getReferenceCarrierFrequencyHzForIsb Returns the reference carrier frequency in Hz for inter-signal bias. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | getReferenceCodeTypeForIsb Returns the reference code type for inter-signal bias. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getReferenceConstellationTypeForIsb Returns the reference constellation type for inter-signal bias. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | getTimeNanos Gets the GNSS receiver internal hardware clock value in nanoseconds. |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | getTimeUncertaintyNanos Gets the clock's time Uncertainty (1-Sigma) in nanoseconds. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasBiasNanos Returns `true` if getBiasNanos is available, `false` otherwise. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasBiasUncertaintyNanos Returns `true` if getBiasUncertaintyNanos is available, `false` otherwise. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasDriftNanosPerSecond Returns `true` if getDriftNanosPerSecond is available, `false` otherwise. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasDriftUncertaintyNanosPerSecond Returns `true` if getDriftUncertaintyNanosPerSecond is available, `false` otherwise. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasElapsedRealtimeNanos Returns `true` if getElapsedRealtimeNanos is available, `false` otherwise. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasElapsedRealtimeUncertaintyNanos Returns `true` if getElapsedRealtimeUncertaintyNanos is available, `false` otherwise. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasFullBiasNanos Returns `true` if getFullBiasNanos is available, `false` otherwise. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasLeapSecond Returns `true` if getLeapSecond is available, `false` otherwise. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasReferenceCarrierFrequencyHzForIsb Returns `true` if getReferenceCarrierFrequencyHzForIsb is available, `false` otherwise. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasReferenceCodeTypeForIsb Returns `true` if getReferenceCodeTypeForIsb is available, `false` otherwise. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasReferenceConstellationTypeForIsb Returns `true` if getReferenceConstellationTypeForIsb is available, `false` otherwise. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasTimeUncertaintyNanos Returns `true` if getTimeUncertaintyNanos is available, `false` otherwise. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | toString Returns a string representation of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeToParcel Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [GnssClock](GnssClock.md)!\> | `https://developer.android.com/reference/kotlin/android/location/GnssClock#CREATOR:android.os.Parcelable.Creator` <br /> |

## Public methods

### describeContents

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of writeToParcel, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getBiasNanos

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getBiasNanos(): Double
```

Gets the clock's sub-nanosecond bias.

See the description of how this field is part of converting from hardware clock time, to GPS time, in getFullBiasNanos.

The error estimate for the sum of this field and getFullBiasNanos is getBiasUncertaintyNanos.

The value is only available if hasBiasNanos is `true`.

### getBiasUncertaintyNanos

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getBiasUncertaintyNanos(): Double
```

Gets the clock's Bias Uncertainty (1-Sigma) in nanoseconds.

See the description of how this field provides the error estimate in the conversion from hardware clock time, to GPS time, in getFullBiasNanos.

The value is only available if hasBiasUncertaintyNanos is `true`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | Value is 0.0f or greater |

### getDriftNanosPerSecond

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDriftNanosPerSecond(): Double
```

Gets the clock's Drift in nanoseconds per second.

This value is the instantaneous time-derivative of the value provided by the sum of getFullBiasNanos and getBiasNanos.

A positive value indicates that the frequency is higher than the nominal (e.g. GPS master clock) frequency. The error estimate for this reported drift is getDriftUncertaintyNanosPerSecond.

The value is only available if hasDriftNanosPerSecond is `true`.

### getDriftUncertaintyNanosPerSecond

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDriftUncertaintyNanosPerSecond(): Double
```

Gets the clock's Drift Uncertainty (1-Sigma) in nanoseconds per second.

The value is only available if hasDriftUncertaintyNanosPerSecond is `true`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | Value is 0.0f or greater |

### getElapsedRealtimeNanos

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getElapsedRealtimeNanos(): Long
```

Returns the elapsed real-time of this clock since system boot, in nanoseconds.

The value is only available if hasElapsedRealtimeNanos is `true`.

### getElapsedRealtimeUncertaintyNanos

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getElapsedRealtimeUncertaintyNanos(): Double
```

Gets the estimate of the relative precision of the alignment of the getElapsedRealtimeNanos timestamp, with the reported measurements in nanoseconds (68% confidence).

The value is only available if hasElapsedRealtimeUncertaintyNanos is `true`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | Value is 0.0f or greater |

### getFullBiasNanos

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getFullBiasNanos(): Long
```

Gets the difference between hardware clock (getTimeNanos) inside GPS receiver and the true GPS time since 0000Z, January 6, 1980, in nanoseconds.

This value is available if the receiver has estimated GPS time. If the computed time is for a non-GPS constellation, the time offset of that constellation to GPS has to be applied to fill this value. The value is only available if hasFullBiasNanos is `true`.

The error estimate for the sum of this field and getBiasNanos is getBiasUncertaintyNanos.

The sign of the value is defined by the following equation:

```kotlin
local estimate of GPS time = TimeNanos - (FullBiasNanos + BiasNanos)
```

### getHardwareClockDiscontinuityCount

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getHardwareClockDiscontinuityCount(): Int
```

Gets count of hardware clock discontinuities.

When this value stays the same, vs. a value in a previously reported GnssClock, it can be safely assumed that the `TimeNanos` value has been derived from a clock that has been running continuously - e.g. a single continuously powered crystal oscillator, and thus the `(FullBiasNanos + BiasNanos)` offset can be modelled with traditional clock bias \& drift models.

Each time this value changes, vs. the value in a previously reported GnssClock, that suggests the hardware clock may have experienced a discontinuity (e.g. a power cycle or other anomaly), so that any assumptions about modelling a smoothly changing `(FullBiasNanos + BiasNanos)` offset, and a smoothly growing `(TimeNanos)` between this and the previously reported `GnssClock`, should be reset.

### getLeapSecond

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getLeapSecond(): Int
```

Gets the leap second associated with the clock's time.

The sign of the value is defined by the following equation:

```kotlin
UtcTimeNanos = TimeNanos - (FullBiasNanos + BiasNanos) - LeapSecond * 1,000,000,000
```

The value is only available if hasLeapSecond is `true`.

### getReferenceCarrierFrequencyHzForIsb

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getReferenceCarrierFrequencyHzForIsb(): Double
```

Returns the reference carrier frequency in Hz for inter-signal bias.

The value is only available if hasReferenceCarrierFrequencyHzForIsb is `true`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | Value is 0.0f or greater |

### getReferenceCodeTypeForIsb

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getReferenceCodeTypeForIsb(): String
```

Returns the reference code type for inter-signal bias.

The value is only available if hasReferenceCodeTypeForIsb is `true`.

The return value is one of those constants defined in getCodeType.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | This value cannot be `null`. |

### getReferenceConstellationTypeForIsb

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getReferenceConstellationTypeForIsb(): Int
```

Returns the reference constellation type for inter-signal bias.

The value is only available if hasReferenceConstellationTypeForIsb is `true`.

The return value is one of those constants with `CONSTELLATION_` prefix in GnssStatus.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/location/GnssStatus#CONSTELLATION_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/location/GnssStatus#CONSTELLATION_GPS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/location/GnssStatus#CONSTELLATION_SBAS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/location/GnssStatus#CONSTELLATION_GLONASS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/location/GnssStatus#CONSTELLATION_QZSS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/location/GnssStatus#CONSTELLATION_BEIDOU:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/location/GnssStatus#CONSTELLATION_GALILEO:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/location/GnssStatus#CONSTELLATION_IRNSS:kotlin.Int` |

### getTimeNanos

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTimeNanos(): Long
```

Gets the GNSS receiver internal hardware clock value in nanoseconds.

This value is expected to be monotonically increasing while the hardware clock remains powered on. For the case of a hardware clock that is not continuously on, see the getHardwareClockDiscontinuityCount field. The GPS time can be derived by subtracting the sum of getFullBiasNanos and getBiasNanos (when they are available) from this value. Sub-nanosecond accuracy can be provided by means of getBiasNanos.

The error estimate for this value (if applicable) is getTimeUncertaintyNanos.

### getTimeUncertaintyNanos

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTimeUncertaintyNanos(): Double
```

Gets the clock's time Uncertainty (1-Sigma) in nanoseconds.

The uncertainty is represented as an absolute (single sided) value.

The value is only available if hasTimeUncertaintyNanos is `true`.

This value is often effectively zero (it is the reference clock by which all other times and time uncertainties are measured), and thus this field may often be 0, or not provided.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | Value is 0.0f or greater |

### hasBiasNanos

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasBiasNanos(): Boolean
```

Returns `true` if getBiasNanos is available, `false` otherwise.

### hasBiasUncertaintyNanos

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasBiasUncertaintyNanos(): Boolean
```

Returns `true` if getBiasUncertaintyNanos is available, `false` otherwise.

### hasDriftNanosPerSecond

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasDriftNanosPerSecond(): Boolean
```

Returns `true` if getDriftNanosPerSecond is available, `false` otherwise.

### hasDriftUncertaintyNanosPerSecond

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasDriftUncertaintyNanosPerSecond(): Boolean
```

Returns `true` if getDriftUncertaintyNanosPerSecond is available, `false` otherwise.

### hasElapsedRealtimeNanos

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasElapsedRealtimeNanos(): Boolean
```

Returns `true` if getElapsedRealtimeNanos is available, `false` otherwise.

### hasElapsedRealtimeUncertaintyNanos

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasElapsedRealtimeUncertaintyNanos(): Boolean
```

Returns `true` if getElapsedRealtimeUncertaintyNanos is available, `false` otherwise.

### hasFullBiasNanos

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasFullBiasNanos(): Boolean
```

Returns `true` if getFullBiasNanos is available, `false` otherwise.

### hasLeapSecond

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasLeapSecond(): Boolean
```

Returns `true` if getLeapSecond is available, `false` otherwise.

### hasReferenceCarrierFrequencyHzForIsb

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasReferenceCarrierFrequencyHzForIsb(): Boolean
```

Returns `true` if getReferenceCarrierFrequencyHzForIsb is available, `false` otherwise.

### hasReferenceCodeTypeForIsb

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasReferenceCodeTypeForIsb(): Boolean
```

Returns `true` if getReferenceCodeTypeForIsb is available, `false` otherwise.

### hasReferenceConstellationTypeForIsb

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasReferenceConstellationTypeForIsb(): Boolean
```

Returns `true` if getReferenceConstellationTypeForIsb is available, `false` otherwise.

### hasTimeUncertaintyNanos

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasTimeUncertaintyNanos(): Boolean
```

Returns `true` if getTimeUncertaintyNanos is available, `false` otherwise.

### toString

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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

## Properties

### CREATOR

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<GnssClock!>
```
