Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

# TotalCaloriesBurnedRecord

```
class TotalCaloriesBurnedRecord : IntervalRecord
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [android.health.connect.datatypes.Record](Record.md) |||
| | ↳ | [android.health.connect.datatypes.IntervalRecord](IntervalRecord.md) ||
| | | ↳ | [android.health.connect.datatypes.TotalCaloriesBurnedRecord](TotalCaloriesBurnedRecord.md) |
| --- | --- | --- | --- |

Total energy burned by the user in Energy, including active \& basal energy burned (BMR). Each record represents the total kilocalories burned over a time interval.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/TotalCaloriesBurnedRecord.Builder` Builder class for TotalCaloriesBurnedRecord |

| Inherited constants ||
|---|---|
| From class Record |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_INSTANT:kotlin.Int` The record represents an instantaneous event. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_INTERVAL:kotlin.Int` The record represents an event over an interval. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_LOCAL_DATE:kotlin.Int` The record represents an event that occurred on a specific date. <br /> | ||

| Public methods ||
|---|---|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | equals Indicates whether some other object is "equal to" this one. |
| [Energy](../android.health.connect.datatypes.units/Energy.md) | getEnergy <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | hashCode Returns a hash code value for the object. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class IntervalRecord |---|---| | `https://developer.android.com/reference/kotlin/java/time/Instant.html#` | getEndTime <br /> | | `https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#` | getEndZoneOffset <br /> | | `https://developer.android.com/reference/kotlin/java/time/Instant.html#` | getStartTime <br /> | | `https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#` | getStartZoneOffset <br /> | ||
| From class Record |---|---| | Metadata | getMetadata <br /> | ||

| Properties ||
|---|---|
| static [AggregationType](AggregationType.md)\< [Energy](../android.health.connect.datatypes.units/Energy.md)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/TotalCaloriesBurnedRecord#ENERGY_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to get total energy from total calories burned using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |

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
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the object argument; `false` otherwise. |

### getEnergy

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getEnergy(): Energy
```

| Return ||
|---|---|
| Energy | energy burned during this activity in Energy unit. This value cannot be `null`. |

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

### ENERGY_TOTAL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val ENERGY_TOTAL: AggregationType<Energy!>
```

Metric identifier to get total energy from total calories burned using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`
