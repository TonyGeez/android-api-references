Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

# WeightRecord

```
class WeightRecord : InstantRecord
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [android.health.connect.datatypes.Record](Record.md) |||
| | ↳ | [android.health.connect.datatypes.InstantRecord](InstantRecord.md) ||
| | | ↳ | [android.health.connect.datatypes.WeightRecord](WeightRecord.md) |
| --- | --- | --- | --- |

Captures the user's weight.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/WeightRecord.Builder` Builder class for WeightRecord |

| Inherited constants ||
|---|---|
| From class Record |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_INSTANT:kotlin.Int` The record represents an instantaneous event. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_INTERVAL:kotlin.Int` The record represents an event over an interval. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_LOCAL_DATE:kotlin.Int` The record represents an event that occurred on a specific date. <br /> | ||

| Public methods ||
|---|---|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | equals Indicates whether some other object is "equal to" this one. |
| [Mass](../android.health.connect.datatypes.units/Mass.md) | getWeight <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | hashCode Returns a hash code value for the object. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class Record |---|---| | Metadata | getMetadata <br /> | ||
| From class InstantRecord |---|---| | `https://developer.android.com/reference/kotlin/java/time/Instant.html#` | getTime <br /> | | `https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#` | getZoneOffset <br /> | ||

| Properties ||
|---|---|
| static [AggregationType](AggregationType.md)\< [Mass](../android.health.connect.datatypes.units/Mass.md)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/WeightRecord#WEIGHT_AVG:android.health.connect.datatypes.AggregationType` Metric identifier to get average weight using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| static [AggregationType](AggregationType.md)\< [Mass](../android.health.connect.datatypes.units/Mass.md)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/WeightRecord#WEIGHT_MAX:android.health.connect.datatypes.AggregationType` Metric identifier to get maximum weight using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
| static [AggregationType](AggregationType.md)\< [Mass](../android.health.connect.datatypes.units/Mass.md)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/WeightRecord#WEIGHT_MIN:android.health.connect.datatypes.AggregationType` Metric identifier to get minimum weight using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#` |
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

### getWeight

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getWeight(): Mass
```

| Return ||
|---|---|
| Mass | weight in Mass unit. This value cannot be `null`. |

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

### WEIGHT_AVG

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val WEIGHT_AVG: AggregationType<Mass!>
```

Metric identifier to get average weight using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`

### WEIGHT_MAX

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val WEIGHT_MAX: AggregationType<Mass!>
```

Metric identifier to get maximum weight using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`

### WEIGHT_MIN

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val WEIGHT_MIN: AggregationType<Mass!>
```

Metric identifier to get minimum weight using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`
