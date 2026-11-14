Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

# StepsCadenceRecord

```
class StepsCadenceRecord : IntervalRecord
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [android.health.connect.datatypes.Record](Record.md) |||
| | ↳ | [android.health.connect.datatypes.IntervalRecord](IntervalRecord.md) ||
| | | ↳ | [android.health.connect.datatypes.StepsCadenceRecord](StepsCadenceRecord.md) |
| --- | --- | --- | --- |

Captures the user's steps cadence.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/StepsCadenceRecord.Builder` Builder class for `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/StepsCadenceRecord#` |
| | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/StepsCadenceRecord.StepsCadenceRecordSample` Represents a single measurement of the steps cadence. |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_INSTANT:kotlin.Int` The record represents an instantaneous event. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_INTERVAL:kotlin.Int` The record represents an event over an interval. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_LOCAL_DATE:kotlin.Int` The record represents an event that occurred on a specific date. <br /> | ||

| Public methods ||
|---|---|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/StepsCadenceRecord#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [StepsCadenceRecord.StepsCadenceRecordSample](../android/health/connect/datatypes/StepsCadenceRecord.StepsCadenceRecordSample.md)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/StepsCadenceRecord#getSamples()()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/StepsCadenceRecord#hashCode()()` Returns a hash code value for the object. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/IntervalRecord` |---|---| | `https://developer.android.com/reference/kotlin/java/time/Instant.html#` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/IntervalRecord#getEndTime()()` <br /> | | `https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/IntervalRecord#getEndZoneOffset()()` <br /> | | `https://developer.android.com/reference/kotlin/java/time/Instant.html#` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/IntervalRecord#getStartTime()()` <br /> | | `https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/IntervalRecord#getStartZoneOffset()()` <br /> | ||
| From class `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record` |---|---| | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Metadata` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#getMetadata()()` <br /> | ||

| Properties ||
|---|---|
| static [AggregationType](AggregationType.md)\< [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/StepsCadenceRecord#STEPS_CADENCE_RATE_AVG:android.health.connect.datatypes.AggregationType` Metric identifier to retrieve average Steps cadence rate using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| static [AggregationType](AggregationType.md)\< [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/StepsCadenceRecord#STEPS_CADENCE_RATE_MAX:android.health.connect.datatypes.AggregationType` Metric identifier to retrieve maximum Steps cadence rate using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| static [AggregationType](AggregationType.md)\< [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/StepsCadenceRecord#STEPS_CADENCE_RATE_MIN:android.health.connect.datatypes.AggregationType` Metric identifier to retrieve minimum Steps cadence rate using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
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

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj |

### getSamples

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getSamples(): MutableList<StepsCadenceRecord.StepsCadenceRecordSample!>
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/health/connect/datatypes/StepsCadenceRecord.StepsCadenceRecordSample!>` | StepsCadenceRecord samples corresponding to this record, in ascending time order. This value cannot be `null`. |

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

### STEPS_CADENCE_RATE_AVG

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 10](https://developer.android.com/sdkExtensions)

```
static val STEPS_CADENCE_RATE_AVG: AggregationType<Double!>
```

Metric identifier to retrieve average Steps cadence rate using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`

### STEPS_CADENCE_RATE_MAX

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 10](https://developer.android.com/sdkExtensions)

```
static val STEPS_CADENCE_RATE_MAX: AggregationType<Double!>
```

Metric identifier to retrieve maximum Steps cadence rate using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`

### STEPS_CADENCE_RATE_MIN

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 10](https://developer.android.com/sdkExtensions)

```
static val STEPS_CADENCE_RATE_MIN: AggregationType<Double!>
```

Metric identifier to retrieve minimum Steps cadence rate using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`
