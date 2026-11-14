Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

# Vo2MaxRecord

```
class Vo2MaxRecord : InstantRecord
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [android.health.connect.datatypes.Record](../android/health/connect/datatypes/Record.md) |||
| | ↳ | [android.health.connect.datatypes.InstantRecord](../android/health/connect/datatypes/InstantRecord.md) ||
| | | ↳ | [android.health.connect.datatypes.Vo2MaxRecord](../android/health/connect/datatypes/Vo2MaxRecord.md) |
| --- | --- | --- | --- |

Capture user's VO2 max score and optionally the measurement method.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Vo2MaxRecord.Builder` Builder class for `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Vo2MaxRecord#` |
| | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Vo2MaxRecord.Vo2MaxMeasurementMethod` Identifier for V02 max measurement method |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_INSTANT:kotlin.Int` The record represents an instantaneous event. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_INTERVAL:kotlin.Int` The record represents an event over an interval. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_LOCAL_DATE:kotlin.Int` The record represents an event that occurred on a specific date. <br /> | ||

| Public methods ||
|---|---|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Vo2MaxRecord#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Vo2MaxRecord#getMeasurementMethod()()` <br /> |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Vo2MaxRecord#getVo2MillilitersPerMinuteKilogram()()` <br /> |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Vo2MaxRecord#hashCode()()` Returns a hash code value for the object. |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record` |---|---| | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Metadata` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#getMetadata()()` <br /> | ||
| From class `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/InstantRecord` |---|---| | `https://developer.android.com/reference/kotlin/java/time/Instant.html#` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/InstantRecord#getTime()()` <br /> | | `https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/InstantRecord#getZoneOffset()()` <br /> | ||

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

### getMeasurementMethod

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getMeasurementMethod(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | measurementMethod. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Vo2MaxRecord.Vo2MaxMeasurementMethod#MEASUREMENT_METHOD_OTHER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Vo2MaxRecord.Vo2MaxMeasurementMethod#MEASUREMENT_METHOD_METABOLIC_CART:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Vo2MaxRecord.Vo2MaxMeasurementMethod#MEASUREMENT_METHOD_HEART_RATE_RATIO:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Vo2MaxRecord.Vo2MaxMeasurementMethod#MEASUREMENT_METHOD_COOPER_TEST:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Vo2MaxRecord.Vo2MaxMeasurementMethod#MEASUREMENT_METHOD_MULTISTAGE_FITNESS_TEST:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Vo2MaxRecord.Vo2MaxMeasurementMethod#MEASUREMENT_METHOD_ROCKPORT_FITNESS_TEST:kotlin.Int` |

### getVo2MillilitersPerMinuteKilogram

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getVo2MillilitersPerMinuteKilogram(): Double
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | vo2MillilitersPerMinuteKilogram |

### hashCode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

Returns a hash code value for the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |
