Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions)

# ActivityIntensityRecord

```
class ActivityIntensityRecord : IntervalRecord
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [android.health.connect.datatypes.Record](Record.md) |||
| | ↳ | [android.health.connect.datatypes.IntervalRecord](IntervalRecord.md) ||
| | | ↳ | [android.health.connect.datatypes.ActivityIntensityRecord](ActivityIntensityRecord.md) |
| --- | --- | --- | --- |

Represents intensity of an activity.

Intensity can be either moderate or vigorous.

Each record requires the start time, the end time and the activity intensity type.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ActivityIntensityRecord.Builder` Builder class for `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ActivityIntensityRecord#` |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ActivityIntensityRecord#ACTIVITY_INTENSITY_TYPE_MODERATE:kotlin.Int` Moderate activity intensity. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ActivityIntensityRecord#ACTIVITY_INTENSITY_TYPE_VIGOROUS:kotlin.Int` Vigorous activity intensity. |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_INSTANT:kotlin.Int` The record represents an instantaneous event. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_INTERVAL:kotlin.Int` The record represents an event over an interval. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_LOCAL_DATE:kotlin.Int` The record represents an event that occurred on a specific date. <br /> | ||

| Public methods ||
|---|---|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ActivityIntensityRecord#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ActivityIntensityRecord#getActivityIntensityType()()` Returns the type of the activity intensity. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ActivityIntensityRecord#hashCode()()` Returns a hash code value for the object. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/IntervalRecord` |---|---| | `https://developer.android.com/reference/kotlin/java/time/Instant.html#` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/IntervalRecord#getEndTime()()` <br /> | | `https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/IntervalRecord#getEndZoneOffset()()` <br /> | | `https://developer.android.com/reference/kotlin/java/time/Instant.html#` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/IntervalRecord#getStartTime()()` <br /> | | `https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/IntervalRecord#getStartZoneOffset()()` <br /> | ||
| From class `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record` |---|---| | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Metadata` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#getMetadata()()` <br /> | ||

| Properties ||
|---|---|
| static [AggregationType](AggregationType.md)\< [Duration](../java.time/Duration.md)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ActivityIntensityRecord#DURATION_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to retrieve the total duration of activity intensity regardless of the type using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`. |
| static [AggregationType](AggregationType.md)\< [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ActivityIntensityRecord#INTENSITY_MINUTES_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to retrieve the number of weighted intensity minutes using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`. |
| static [AggregationType](AggregationType.md)\< [Duration](../java.time/Duration.md)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ActivityIntensityRecord#MODERATE_DURATION_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to retrieve the total duration of moderate activity intensity using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`. |
| --- | --- |
| static [AggregationType](AggregationType.md)\< [Duration](../java.time/Duration.md)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ActivityIntensityRecord#VIGOROUS_DURATION_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to retrieve the total duration of vigorous activity intensity using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`. |

## Constants

### ACTIVITY_INTENSITY_TYPE_MODERATE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions)

```
static val ACTIVITY_INTENSITY_TYPE_MODERATE: Int
```

Moderate activity intensity.

 Value: 0

### ACTIVITY_INTENSITY_TYPE_VIGOROUS

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions)

```
static val ACTIVITY_INTENSITY_TYPE_VIGOROUS: Int
```

Vigorous activity intensity.

 Value: 1

## Public methods

### equals

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |
| `object` | the reference object with which to compare. This value may be `null`. |
| `o` | This value may be `null`. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj |

### getActivityIntensityType

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions)

```
fun getActivityIntensityType(): Int
```

Returns the type of the activity intensity.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ActivityIntensityRecord#ACTIVITY_INTENSITY_TYPE_MODERATE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ActivityIntensityRecord#ACTIVITY_INTENSITY_TYPE_VIGOROUS:kotlin.Int` |

### hashCode

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

Returns a hash code value for the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

## Properties

### DURATION_TOTAL

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions)

```
static val DURATION_TOTAL: AggregationType<Duration!>
```

Metric identifier to retrieve the total duration of activity intensity regardless of the type using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`.

Equivalent to `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ActivityIntensityRecord#MODERATE_DURATION_TOTAL:android.health.connect.datatypes.AggregationType` + `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ActivityIntensityRecord#VIGOROUS_DURATION_TOTAL:android.health.connect.datatypes.AggregationType`.

### INTENSITY_MINUTES_TOTAL

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions)

```
static val INTENSITY_MINUTES_TOTAL: AggregationType<Long!>
```

Metric identifier to retrieve the number of weighted intensity minutes using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`.

Records of type `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ActivityIntensityRecord#ACTIVITY_INTENSITY_TYPE_MODERATE:kotlin.Int` contribute their full duration to the result, while records of type `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ActivityIntensityRecord#ACTIVITY_INTENSITY_TYPE_VIGOROUS:kotlin.Int` contribute double their duration.

Equivalent to `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ActivityIntensityRecord#MODERATE_DURATION_TOTAL:android.health.connect.datatypes.AggregationType` + 2 \* `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ActivityIntensityRecord#VIGOROUS_DURATION_TOTAL:android.health.connect.datatypes.AggregationType` rounded to minutes.

Calculated in minutes.

### MODERATE_DURATION_TOTAL

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions)

```
static val MODERATE_DURATION_TOTAL: AggregationType<Duration!>
```

Metric identifier to retrieve the total duration of moderate activity intensity using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`.

### VIGOROUS_DURATION_TOTAL

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 16](https://developer.android.com/sdkExtensions)

```
static val VIGOROUS_DURATION_TOTAL: AggregationType<Duration!>
```

Metric identifier to retrieve the total duration of vigorous activity intensity using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`.
