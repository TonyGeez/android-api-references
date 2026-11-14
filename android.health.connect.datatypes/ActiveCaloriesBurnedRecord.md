Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

# ActiveCaloriesBurnedRecord

```
class ActiveCaloriesBurnedRecord : IntervalRecord
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [android.health.connect.datatypes.Record](Record.md) |||
| | ↳ | [android.health.connect.datatypes.IntervalRecord](IntervalRecord.md) ||
| | | ↳ | [android.health.connect.datatypes.ActiveCaloriesBurnedRecord](ActiveCaloriesBurnedRecord.md) |
| --- | --- | --- | --- |

Captures the estimated active energy burned by the user (in kilocalories), excluding basal metabolic rate (BMR).

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ActiveCaloriesBurnedRecord.Builder` Builder class for ActiveCaloriesBurnedRecord |

| Inherited constants ||
|---|---|
| From class Record |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_INSTANT:kotlin.Int` The record represents an instantaneous event. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_INTERVAL:kotlin.Int` The record represents an event over an interval. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_LOCAL_DATE:kotlin.Int` The record represents an event that occurred on a specific date. <br /> | ||

| Public methods ||
|---|---|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | equals Indicates whether some other object is "equal to" this one. |
| [Energy](../android.health.connect.datatypes.units/Energy.md) | getEnergy <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | hashCode <br /> |
| --- | --- |

| Inherited functions ||
|---|---|
| From class IntervalRecord |---|---| | `https://developer.android.com/reference/kotlin/java/time/Instant.html#` | getEndTime <br /> | | `https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#` | getEndZoneOffset <br /> | | `https://developer.android.com/reference/kotlin/java/time/Instant.html#` | getStartTime <br /> | | `https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#` | getStartZoneOffset <br /> | ||
| From class Record |---|---| | Metadata | getMetadata <br /> | ||

| Properties ||
|---|---|
| static [AggregationType](AggregationType.md)\< [Energy](../android.health.connect.datatypes.units/Energy.md)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ActiveCaloriesBurnedRecord#ACTIVE_CALORIES_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total active calories burnt using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |

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

### getEnergy

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getEnergy(): Energy
```

| Return ||
|---|---|
| Energy | energy in Energy unit. This value cannot be `null`. |

### hashCode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

## Properties

### ACTIVE_CALORIES_TOTAL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val ACTIVE_CALORIES_TOTAL: AggregationType<Energy!>
```

Metric identifier to get total active calories burnt using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`
