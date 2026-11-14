Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

# BloodPressureRecord

```
class BloodPressureRecord : InstantRecord
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [android.health.connect.datatypes.Record](Record.md) |||
| | ↳ | [android.health.connect.datatypes.InstantRecord](InstantRecord.md) ||
| | | ↳ | [android.health.connect.datatypes.BloodPressureRecord](BloodPressureRecord.md) |
| --- | --- | --- | --- |

Captures the blood pressure of a user. Each record represents a single instantaneous blood pressure reading.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/BloodPressureRecord.BloodPressureMeasurementLocation` Identifier for Blood Pressure Measurement Location |
| | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/BloodPressureRecord.BodyPosition` Identifier for body position |
| | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/BloodPressureRecord.Builder` Builder class for BloodPressureRecord |
| --- | --- |

| Inherited constants ||
|---|---|
| From class Record |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_INSTANT:kotlin.Int` The record represents an instantaneous event. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_INTERVAL:kotlin.Int` The record represents an event over an interval. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_LOCAL_DATE:kotlin.Int` The record represents an event that occurred on a specific date. <br /> | ||

| Public methods ||
|---|---|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | equals Indicates whether some other object is "equal to" this one. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getBodyPosition <br /> |
| [Pressure](../android.health.connect.datatypes.units/Pressure.md) | getDiastolic <br /> |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getMeasurementLocation <br /> |
| [Pressure](../android.health.connect.datatypes.units/Pressure.md) | getSystolic <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | hashCode Returns a hash code value for the object. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class Record |---|---| | Metadata | getMetadata <br /> | ||
| From class InstantRecord |---|---| | `https://developer.android.com/reference/kotlin/java/time/Instant.html#` | getTime <br /> | | `https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#` | getZoneOffset <br /> | ||

| Properties ||
|---|---|
| static [AggregationType](AggregationType.md)\< [Pressure](../android.health.connect.datatypes.units/Pressure.md)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/BloodPressureRecord#DIASTOLIC_AVG:android.health.connect.datatypes.AggregationType` Metric identifier to get average diastolic pressure using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| static [AggregationType](AggregationType.md)\< [Pressure](../android.health.connect.datatypes.units/Pressure.md)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/BloodPressureRecord#DIASTOLIC_MAX:android.health.connect.datatypes.AggregationType` Metric identifier to get maximum diastolic pressure using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| static [AggregationType](AggregationType.md)\< [Pressure](../android.health.connect.datatypes.units/Pressure.md)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/BloodPressureRecord#DIASTOLIC_MIN:android.health.connect.datatypes.AggregationType` Metric identifier to get minimum diastolic pressure using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| --- | --- |
| static [AggregationType](AggregationType.md)\< [Pressure](../android.health.connect.datatypes.units/Pressure.md)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/BloodPressureRecord#SYSTOLIC_AVG:android.health.connect.datatypes.AggregationType` Metric identifier to get average systolic pressure using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| static [AggregationType](AggregationType.md)\< [Pressure](../android.health.connect.datatypes.units/Pressure.md)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/BloodPressureRecord#SYSTOLIC_MAX:android.health.connect.datatypes.AggregationType` Metric identifier to get maximum systolic pressure using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| static [AggregationType](AggregationType.md)\< [Pressure](../android.health.connect.datatypes.units/Pressure.md)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/BloodPressureRecord#SYSTOLIC_MIN:android.health.connect.datatypes.AggregationType` Metric identifier to get minimum systolic pressure using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| --- | --- |

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
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj |

### getBodyPosition

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getBodyPosition(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | bodyPosition. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/BloodPressureRecord.BodyPosition#BODY_POSITION_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/BloodPressureRecord.BodyPosition#BODY_POSITION_STANDING_UP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/BloodPressureRecord.BodyPosition#BODY_POSITION_SITTING_DOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/BloodPressureRecord.BodyPosition#BODY_POSITION_LYING_DOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/BloodPressureRecord.BodyPosition#BODY_POSITION_RECLINING:kotlin.Int` |

### getDiastolic

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getDiastolic(): Pressure
```

| Return ||
|---|---|
| Pressure | diastolic. This value cannot be `null`. |

### getMeasurementLocation

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getMeasurementLocation(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | measurementLocation. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/BloodPressureRecord.BloodPressureMeasurementLocation#BLOOD_PRESSURE_MEASUREMENT_LOCATION_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/BloodPressureRecord.BloodPressureMeasurementLocation#BLOOD_PRESSURE_MEASUREMENT_LOCATION_LEFT_WRIST:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/BloodPressureRecord.BloodPressureMeasurementLocation#BLOOD_PRESSURE_MEASUREMENT_LOCATION_RIGHT_WRIST:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/BloodPressureRecord.BloodPressureMeasurementLocation#BLOOD_PRESSURE_MEASUREMENT_LOCATION_LEFT_UPPER_ARM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/BloodPressureRecord.BloodPressureMeasurementLocation#BLOOD_PRESSURE_MEASUREMENT_LOCATION_RIGHT_UPPER_ARM:kotlin.Int` |

### getSystolic

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getSystolic(): Pressure
```

| Return ||
|---|---|
| Pressure | systolic. This value cannot be `null`. |

### hashCode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

Returns a hash code value for the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

## Properties

### DIASTOLIC_AVG

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 10](https://developer.android.com/sdkExtensions)

```
static val DIASTOLIC_AVG: AggregationType<Pressure!>
```

Metric identifier to get average diastolic pressure using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`

### DIASTOLIC_MAX

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 10](https://developer.android.com/sdkExtensions)

```
static val DIASTOLIC_MAX: AggregationType<Pressure!>
```

Metric identifier to get maximum diastolic pressure using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`

### DIASTOLIC_MIN

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 10](https://developer.android.com/sdkExtensions)

```
static val DIASTOLIC_MIN: AggregationType<Pressure!>
```

Metric identifier to get minimum diastolic pressure using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`

### SYSTOLIC_AVG

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 10](https://developer.android.com/sdkExtensions)

```
static val SYSTOLIC_AVG: AggregationType<Pressure!>
```

Metric identifier to get average systolic pressure using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`

### SYSTOLIC_MAX

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 10](https://developer.android.com/sdkExtensions)

```
static val SYSTOLIC_MAX: AggregationType<Pressure!>
```

Metric identifier to get maximum systolic pressure using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`

### SYSTOLIC_MIN

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 10](https://developer.android.com/sdkExtensions)

```
static val SYSTOLIC_MIN: AggregationType<Pressure!>
```

Metric identifier to get minimum systolic pressure using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`
