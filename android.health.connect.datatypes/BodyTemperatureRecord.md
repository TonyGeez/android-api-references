Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

# BodyTemperatureRecord

```
class BodyTemperatureRecord : InstantRecord
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| ↳ | [android.health.connect.datatypes.Record](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record) |||
| | ↳ | [android.health.connect.datatypes.InstantRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/InstantRecord) ||
| | | ↳ | [android.health.connect.datatypes.BodyTemperatureRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/BodyTemperatureRecord#) |

Captures the body temperature of a user. Each record represents a single instantaneous body temperature measurement.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/BodyTemperatureRecord.Builder` Builder class for `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/BodyTemperatureRecord#` |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_INSTANT:kotlin.Int` The record represents an instantaneous event. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_INTERVAL:kotlin.Int` The record represents an event over an interval. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_LOCAL_DATE:kotlin.Int` The record represents an event that occurred on a specific date. <br /> | ||

| Public methods ||
|---|---|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/BodyTemperatureRecord#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/BodyTemperatureRecord#getMeasurementLocation()()` <br /> |
| [Temperature](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Temperature) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/BodyTemperatureRecord#getTemperature()()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/BodyTemperatureRecord#hashCode()()` Returns a hash code value for the object. |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record` |---|---| | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Metadata` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#getMetadata()()` <br /> | ||
| From class `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/InstantRecord` |---|---| | `https://developer.android.com/reference/kotlin/java/time/Instant.html#` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/InstantRecord#getTime()()` <br /> | | `https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/InstantRecord#getZoneOffset()()` <br /> | ||

## Public methods

### equals

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |
| `object` | the reference object with which to compare. This value may be `null`. |
| `o` | the reference object with which to compare. This value may be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj |

### getMeasurementLocation

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getMeasurementLocation(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | measurementLocation. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/BodyTemperatureMeasurementLocation#MEASUREMENT_LOCATION_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/BodyTemperatureMeasurementLocation#MEASUREMENT_LOCATION_ARMPIT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/BodyTemperatureMeasurementLocation#MEASUREMENT_LOCATION_FINGER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/BodyTemperatureMeasurementLocation#MEASUREMENT_LOCATION_FOREHEAD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/BodyTemperatureMeasurementLocation#MEASUREMENT_LOCATION_MOUTH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/BodyTemperatureMeasurementLocation#MEASUREMENT_LOCATION_RECTUM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/BodyTemperatureMeasurementLocation#MEASUREMENT_LOCATION_TEMPORAL_ARTERY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/BodyTemperatureMeasurementLocation#MEASUREMENT_LOCATION_TOE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/BodyTemperatureMeasurementLocation#MEASUREMENT_LOCATION_EAR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/BodyTemperatureMeasurementLocation#MEASUREMENT_LOCATION_WRIST:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/BodyTemperatureMeasurementLocation#MEASUREMENT_LOCATION_VAGINA:kotlin.Int` |

### getTemperature

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getTemperature(): Temperature
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Temperature` | temperature in `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Temperature` unit. This value cannot be `null`. |

### hashCode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

Returns a hash code value for the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |
