Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

# FloorsClimbedRecord

```
class FloorsClimbedRecord : IntervalRecord
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [android.health.connect.datatypes.Record](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record) |||
| | ↳ | [android.health.connect.datatypes.IntervalRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/IntervalRecord) ||
| | | ↳ | [android.health.connect.datatypes.FloorsClimbedRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FloorsClimbedRecord#) |
| --- | --- | --- | --- |

Captures the number of floors climbed by the user between the start and end time.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FloorsClimbedRecord.Builder` Builder class for `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FloorsClimbedRecord#` |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_INSTANT:kotlin.Int` The record represents an instantaneous event. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_INTERVAL:kotlin.Int` The record represents an event over an interval. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_LOCAL_DATE:kotlin.Int` The record represents an event that occurred on a specific date. <br /> | ||

| Public methods ||
|---|---|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FloorsClimbedRecord#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FloorsClimbedRecord#getFloors()()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FloorsClimbedRecord#hashCode()()` <br /> |
| --- | --- |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/IntervalRecord` |---|---| | `https://developer.android.com/reference/kotlin/java/time/Instant.html#` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/IntervalRecord#getEndTime()()` <br /> | | `https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/IntervalRecord#getEndZoneOffset()()` <br /> | | `https://developer.android.com/reference/kotlin/java/time/Instant.html#` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/IntervalRecord#getStartTime()()` <br /> | | `https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/IntervalRecord#getStartZoneOffset()()` <br /> | ||
| From class `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record` |---|---| | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Metadata` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#getMetadata()()` <br /> | ||

| Properties ||
|---|---|
| static [AggregationType](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType)\< [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FloorsClimbedRecord#FLOORS_CLIMBED_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total floors climbed using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |

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

### getFloors

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getFloors(): Double
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | number of floors climbed. Value is between 0.0f and 1000000.0f inclusive |

### hashCode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

## Properties

### FLOORS_CLIMBED_TOTAL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val FLOORS_CLIMBED_TOTAL: AggregationType<Double!>
```

Metric identifier to get total floors climbed using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`
