Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

# DistanceRecord

```
class DistanceRecord : IntervalRecord
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [android.health.connect.datatypes.Record](Record.md) |||
| | ↳ | [android.health.connect.datatypes.IntervalRecord](IntervalRecord.md) ||
| | | ↳ | [android.health.connect.datatypes.DistanceRecord](DistanceRecord.md) |
| --- | --- | --- | --- |

Captures distance travelled by the user since the last reading. The total distance over an interval can be calculated by adding together all the values during the interval. The start time of each record should represent the start of the interval in which the distance was covered.

If break downs are preferred in scenario of a long workout, consider writing multiple distance records. The start time of each record should be equal to or greater than the end time of the previous record.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/DistanceRecord.Builder` Builder class for `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/DistanceRecord#` |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_INSTANT:kotlin.Int` The record represents an instantaneous event. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_INTERVAL:kotlin.Int` The record represents an event over an interval. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_LOCAL_DATE:kotlin.Int` The record represents an event that occurred on a specific date. <br /> | ||

| Public methods ||
|---|---|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/DistanceRecord#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| [Length](../android.health.connect.datatypes.units/Length.md) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/DistanceRecord#getDistance()()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/DistanceRecord#hashCode()()` <br /> |
| --- | --- |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/IntervalRecord` |---|---| | `https://developer.android.com/reference/kotlin/java/time/Instant.html#` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/IntervalRecord#getEndTime()()` <br /> | | `https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/IntervalRecord#getEndZoneOffset()()` <br /> | | `https://developer.android.com/reference/kotlin/java/time/Instant.html#` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/IntervalRecord#getStartTime()()` <br /> | | `https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/IntervalRecord#getStartZoneOffset()()` <br /> | ||
| From class `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record` |---|---| | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Metadata` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#getMetadata()()` <br /> | ||

| Properties ||
|---|---|
| static [AggregationType](AggregationType.md)\< [Length](../android.health.connect.datatypes.units/Length.md)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/DistanceRecord#DISTANCE_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total distance using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |

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

### getDistance

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getDistance(): Length
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Length` | distance of this activity in `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Length` unit. This value cannot be `null`. |

### hashCode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

## Properties

### DISTANCE_TOTAL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val DISTANCE_TOTAL: AggregationType<Length!>
```

Metric identifier to get total distance using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`
