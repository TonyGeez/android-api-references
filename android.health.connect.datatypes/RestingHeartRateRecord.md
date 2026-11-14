Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

# RestingHeartRateRecord

```
class RestingHeartRateRecord : InstantRecord
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [android.health.connect.datatypes.Record](Record.md) |||
| | ↳ | [android.health.connect.datatypes.InstantRecord](InstantRecord.md) ||
| | | ↳ | [android.health.connect.datatypes.RestingHeartRateRecord](RestingHeartRateRecord.md) |
| --- | --- | --- | --- |

Captures the user's resting heart rate. Each record represents a single instantaneous measurement.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/RestingHeartRateRecord.Builder` Builder class for `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/RestingHeartRateRecord#` |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_INSTANT:kotlin.Int` The record represents an instantaneous event. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_INTERVAL:kotlin.Int` The record represents an event over an interval. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_LOCAL_DATE:kotlin.Int` The record represents an event that occurred on a specific date. <br /> | ||

| Public methods ||
|---|---|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/RestingHeartRateRecord#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/RestingHeartRateRecord#getBeatsPerMinute()()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/RestingHeartRateRecord#hashCode()()` Returns a hash code value for the object. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record` |---|---| | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Metadata` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#getMetadata()()` <br /> | ||
| From class `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/InstantRecord` |---|---| | `https://developer.android.com/reference/kotlin/java/time/Instant.html#` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/InstantRecord#getTime()()` <br /> | | `https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/InstantRecord#getZoneOffset()()` <br /> | ||

| Properties ||
|---|---|
| static [AggregationType](AggregationType.md)\< [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/RestingHeartRateRecord#BPM_AVG:android.health.connect.datatypes.AggregationType` Metric identifier to get average resting heart rate in beats per minute using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| static [AggregationType](AggregationType.md)\< [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/RestingHeartRateRecord#BPM_MAX:android.health.connect.datatypes.AggregationType` Metric identifier to get max resting heart rate in beats per minute using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| static [AggregationType](AggregationType.md)\< [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/RestingHeartRateRecord#BPM_MIN:android.health.connect.datatypes.AggregationType` Metric identifier to get min resting heart rate in beats per minute using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
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

### getBeatsPerMinute

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getBeatsPerMinute(): Long
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | beatsPerMinute |

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

### BPM_AVG

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val BPM_AVG: AggregationType<Long!>
```

Metric identifier to get average resting heart rate in beats per minute using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`

### BPM_MAX

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val BPM_MAX: AggregationType<Long!>
```

Metric identifier to get max resting heart rate in beats per minute using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`

### BPM_MIN

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val BPM_MIN: AggregationType<Long!>
```

Metric identifier to get min resting heart rate in beats per minute using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`
