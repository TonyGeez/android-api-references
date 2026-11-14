Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 13](https://developer.android.com/sdkExtensions)

# SkinTemperatureRecord

```
class SkinTemperatureRecord : IntervalRecord
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| ↳ | [android.health.connect.datatypes.Record](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record) |||
| | ↳ | [android.health.connect.datatypes.IntervalRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/IntervalRecord) ||
| | | ↳ | [android.health.connect.datatypes.SkinTemperatureRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/SkinTemperatureRecord#) |

Captures the skin temperature of a user. Each record can represent a series of measurements of temperature differences.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/SkinTemperatureRecord.Builder` Builder class for `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/SkinTemperatureRecord#` |
| | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/SkinTemperatureRecord.Delta` Skin temperature delta entry of `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/SkinTemperatureRecord#`. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/SkinTemperatureRecord#MEASUREMENT_LOCATION_FINGER:kotlin.Int` Skin temperature measurement location finger. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/SkinTemperatureRecord#MEASUREMENT_LOCATION_TOE:kotlin.Int` Skin temperature measurement location toe. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/SkinTemperatureRecord#MEASUREMENT_LOCATION_UNKNOWN:kotlin.Int` Skin temperature measurement location unknown. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/SkinTemperatureRecord#MEASUREMENT_LOCATION_WRIST:kotlin.Int` Skin temperature measurement location wrist. |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_INSTANT:kotlin.Int` The record represents an instantaneous event. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_INTERVAL:kotlin.Int` The record represents an event over an interval. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_LOCAL_DATE:kotlin.Int` The record represents an event that occurred on a specific date. <br /> | ||

| Public methods ||
|---|---|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/SkinTemperatureRecord#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| [Temperature](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Temperature)? | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/SkinTemperatureRecord#getBaseline()()` <br /> |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [SkinTemperatureRecord.Delta](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/SkinTemperatureRecord.Delta)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/SkinTemperatureRecord#getDeltas()()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/SkinTemperatureRecord#getMeasurementLocation()()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/SkinTemperatureRecord#hashCode()()` <br /> |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/IntervalRecord` |---|---| | `https://developer.android.com/reference/kotlin/java/time/Instant.html#` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/IntervalRecord#getEndTime()()` <br /> | | `https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/IntervalRecord#getEndZoneOffset()()` <br /> | | `https://developer.android.com/reference/kotlin/java/time/Instant.html#` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/IntervalRecord#getStartTime()()` <br /> | | `https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/IntervalRecord#getStartZoneOffset()()` <br /> | ||
| From class `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record` |---|---| | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Metadata` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#getMetadata()()` <br /> | ||

| Properties ||
|---|---|
| static [AggregationType](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType)\< [TemperatureDelta](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/TemperatureDelta)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/SkinTemperatureRecord#SKIN_TEMPERATURE_DELTA_AVG:android.health.connect.datatypes.AggregationType` Metric identifier to retrieve average skin temperature delta using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`. |
| static [AggregationType](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType)\< [TemperatureDelta](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/TemperatureDelta)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/SkinTemperatureRecord#SKIN_TEMPERATURE_DELTA_MAX:android.health.connect.datatypes.AggregationType` Metric identifier to retrieve maximum skin temperature delta using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`. |
| static [AggregationType](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType)\< [TemperatureDelta](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/TemperatureDelta)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/SkinTemperatureRecord#SKIN_TEMPERATURE_DELTA_MIN:android.health.connect.datatypes.AggregationType` Metric identifier to retrieve minimum skin temperature delta using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`. |

## Constants

### MEASUREMENT_LOCATION_FINGER

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 13](https://developer.android.com/sdkExtensions)

```
static val MEASUREMENT_LOCATION_FINGER: Int
```

Skin temperature measurement location finger.

 Value: 1

### MEASUREMENT_LOCATION_TOE

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 13](https://developer.android.com/sdkExtensions)

```
static val MEASUREMENT_LOCATION_TOE: Int
```

Skin temperature measurement location toe.

 Value: 2

### MEASUREMENT_LOCATION_UNKNOWN

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 13](https://developer.android.com/sdkExtensions)

```
static val MEASUREMENT_LOCATION_UNKNOWN: Int
```

Skin temperature measurement location unknown.

 Value: 0

### MEASUREMENT_LOCATION_WRIST

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 13](https://developer.android.com/sdkExtensions)

```
static val MEASUREMENT_LOCATION_WRIST: Int
```

Skin temperature measurement location wrist.

 Value: 3

## Public methods

### equals

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |
| `object` | the reference object with which to compare. This value may be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the object. |

### getBaseline

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 13](https://developer.android.com/sdkExtensions)

```
fun getBaseline(): Temperature?
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Temperature?` | baseline skin temperature in `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Temperature` unit. This value may be `null`. |

### getDeltas

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 13](https://developer.android.com/sdkExtensions)

```
fun getDeltas(): MutableList<SkinTemperatureRecord.Delta!>
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/health/connect/datatypes/SkinTemperatureRecord.Delta!>` | an unmodified list of skin temperature deltas in `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/TemperatureDelta` unit. This value cannot be `null`. |

### getMeasurementLocation

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 13](https://developer.android.com/sdkExtensions)

```
fun getMeasurementLocation(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | measurementLocation. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/SkinTemperatureRecord#MEASUREMENT_LOCATION_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/SkinTemperatureRecord#MEASUREMENT_LOCATION_FINGER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/SkinTemperatureRecord#MEASUREMENT_LOCATION_TOE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/SkinTemperatureRecord#MEASUREMENT_LOCATION_WRIST:kotlin.Int` |

### hashCode

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for the object. |

## Properties

### SKIN_TEMPERATURE_DELTA_AVG

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 13](https://developer.android.com/sdkExtensions)

```
static val SKIN_TEMPERATURE_DELTA_AVG: AggregationType<TemperatureDelta!>
```

Metric identifier to retrieve average skin temperature delta using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`.

### SKIN_TEMPERATURE_DELTA_MAX

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 13](https://developer.android.com/sdkExtensions)

```
static val SKIN_TEMPERATURE_DELTA_MAX: AggregationType<TemperatureDelta!>
```

Metric identifier to retrieve maximum skin temperature delta using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`.

### SKIN_TEMPERATURE_DELTA_MIN

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 13](https://developer.android.com/sdkExtensions)

```
static val SKIN_TEMPERATURE_DELTA_MIN: AggregationType<TemperatureDelta!>
```

Metric identifier to retrieve minimum skin temperature delta using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`.
