Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

# SleepSessionRecord

```
class SleepSessionRecord : IntervalRecord
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [android.health.connect.datatypes.Record](Record.md) |||
| | ↳ | [android.health.connect.datatypes.IntervalRecord](IntervalRecord.md) ||
| | | ↳ | [android.health.connect.datatypes.SleepSessionRecord](SleepSessionRecord.md) |
| --- | --- | --- | --- |

Captures the user's sleep length and its stages. Each record represents a time interval for a full sleep session.

All `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/SleepSessionRecord.Stage` time intervals should fall within the sleep session interval. Time intervals for stages don't need to be continuous but shouldn't overlap.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/SleepSessionRecord.Builder` Builder class for SleepSessionRecord |
| | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/SleepSessionRecord.Stage` Captures the user's length and type of sleep. |
| | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/SleepSessionRecord.StageType` Identifier for sleeping stage, as returned by getType. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class Record |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_INSTANT:kotlin.Int` The record represents an instantaneous event. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_INTERVAL:kotlin.Int` The record represents an event over an interval. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_LOCAL_DATE:kotlin.Int` The record represents an event that occurred on a specific date. <br /> | ||

| Public methods ||
|---|---|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | equals Indicates whether some other object is "equal to" this one. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | getNotes Returns notes for the sleep session. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [SleepSessionRecord.Stage](../android/health/connect/datatypes/SleepSessionRecord.Stage.md)!\> | getStages Returns stages of the sleep session. |
| --- | --- |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | getTitle Returns title of the sleep session. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | hashCode Returns a hash code value for the object. |

| Inherited functions ||
|---|---|
| From class IntervalRecord |---|---| | `https://developer.android.com/reference/kotlin/java/time/Instant.html#` | getEndTime <br /> | | `https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#` | getEndZoneOffset <br /> | | `https://developer.android.com/reference/kotlin/java/time/Instant.html#` | getStartTime <br /> | | `https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#` | getStartZoneOffset <br /> | ||
| From class Record |---|---| | Metadata | getMetadata <br /> | ||

| Properties ||
|---|---|
| static [AggregationType](AggregationType.md)\< [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/SleepSessionRecord#SLEEP_DURATION_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to retrieve total sleep session duration using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`. |

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
| `o` | This value may be `null`. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj |

### getNotes

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getNotes(): CharSequence?
```

Returns notes for the sleep session. Returns null if no notes was specified.

### getStages

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getStages(): MutableList<SleepSessionRecord.Stage!>
```

Returns stages of the sleep session.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/health/connect/datatypes/SleepSessionRecord.Stage!>` | This value cannot be `null`. |

### getTitle

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getTitle(): CharSequence?
```

Returns title of the sleep session. Returns null if no notes was specified.

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

### SLEEP_DURATION_TOTAL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val SLEEP_DURATION_TOTAL: AggregationType<Long!>
```

Metric identifier to retrieve total sleep session duration using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`. Calculated in milliseconds.
