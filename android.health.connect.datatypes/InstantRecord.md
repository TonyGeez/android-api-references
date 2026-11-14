Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

# InstantRecord

```
abstract class InstantRecord : Record
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.health.connect.datatypes.Record](../android/health/connect/datatypes/Record.md) ||
| | ↳ | [android.health.connect.datatypes.InstantRecord](../android/health/connect/datatypes/InstantRecord.md) |

| Known Direct Subclasses [BasalBodyTemperatureRecord](../android/health/connect/datatypes/BasalBodyTemperatureRecord.md), [BasalMetabolicRateRecord](../android/health/connect/datatypes/BasalMetabolicRateRecord.md), [BloodGlucoseRecord](../android/health/connect/datatypes/BloodGlucoseRecord.md), [BloodPressureRecord](../android/health/connect/datatypes/BloodPressureRecord.md), [BodyFatRecord](../android/health/connect/datatypes/BodyFatRecord.md), [BodyTemperatureRecord](../android/health/connect/datatypes/BodyTemperatureRecord.md), [BodyWaterMassRecord](../android/health/connect/datatypes/BodyWaterMassRecord.md), [BoneMassRecord](../android/health/connect/datatypes/BoneMassRecord.md), [CervicalMucusRecord](../android/health/connect/datatypes/CervicalMucusRecord.md), [HeartRateVariabilityRmssdRecord](../android/health/connect/datatypes/HeartRateVariabilityRmssdRecord.md), [HeightRecord](../android/health/connect/datatypes/HeightRecord.md), [IntermenstrualBleedingRecord](../android/health/connect/datatypes/IntermenstrualBleedingRecord.md), and 9 others. |---|---| | [BasalBodyTemperatureRecord](../android/health/connect/datatypes/BasalBodyTemperatureRecord.md) | Captures the body temperature of a user when at rest (for example, immediately after waking up). | | [BasalMetabolicRateRecord](../android/health/connect/datatypes/BasalMetabolicRateRecord.md) | Captures the BMR of a user. | | [BloodGlucoseRecord](../android/health/connect/datatypes/BloodGlucoseRecord.md) | Captures the concentration of glucose in the blood. | | [BloodPressureRecord](../android/health/connect/datatypes/BloodPressureRecord.md) | Captures the blood pressure of a user. | | [BodyFatRecord](../android/health/connect/datatypes/BodyFatRecord.md) | Captures the body fat percentage of a user. | | [BodyTemperatureRecord](../android/health/connect/datatypes/BodyTemperatureRecord.md) | Captures the body temperature of a user. | | [BodyWaterMassRecord](../android/health/connect/datatypes/BodyWaterMassRecord.md) | Captures the user's body water mass. | | [BoneMassRecord](../android/health/connect/datatypes/BoneMassRecord.md) | Captures the user's bone mass. | | [CervicalMucusRecord](../android/health/connect/datatypes/CervicalMucusRecord.md) | Captures the description of cervical mucus. | | [HeartRateVariabilityRmssdRecord](../android/health/connect/datatypes/HeartRateVariabilityRmssdRecord.md) | Captures the user's heart rate variability RMSSD. | | [HeightRecord](../android/health/connect/datatypes/HeightRecord.md) | Captures the user's height. | | [IntermenstrualBleedingRecord](../android/health/connect/datatypes/IntermenstrualBleedingRecord.md) | Captures the user's inter-menstrual bleeding. | | [LeanBodyMassRecord](../android/health/connect/datatypes/LeanBodyMassRecord.md) | Captures the user's lean body mass. | | [MenstruationFlowRecord](../android/health/connect/datatypes/MenstruationFlowRecord.md) | Captures a description of how heavy a user's menstrual flow was (spotting, light, medium, or heavy). | | [OvulationTestRecord](../android/health/connect/datatypes/OvulationTestRecord.md) | Each record represents the result of an ovulation test. | | [OxygenSaturationRecord](../android/health/connect/datatypes/OxygenSaturationRecord.md) | Captures the amount of oxygen circulating in the blood, measured as a percentage of oxygen-saturated hemoglobin. | | [RespiratoryRateRecord](../android/health/connect/datatypes/RespiratoryRateRecord.md) | Captures the user's respiratory rate. | | [RestingHeartRateRecord](../android/health/connect/datatypes/RestingHeartRateRecord.md) | Captures the user's resting heart rate. | | [SexualActivityRecord](../android/health/connect/datatypes/SexualActivityRecord.md) | Captures an occurrence of sexual activity. | | [Vo2MaxRecord](../android/health/connect/datatypes/Vo2MaxRecord.md) | Capture user's VO2 max score and optionally the measurement method. | | [WeightRecord](../android/health/connect/datatypes/WeightRecord.md) | Captures the user's weight. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A record that contains a measurement recorded as an instance .

## Summary

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_INSTANT:kotlin.Int` The record represents an instantaneous event. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_INTERVAL:kotlin.Int` The record represents an event over an interval. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_LOCAL_DATE:kotlin.Int` The record represents an event that occurred on a specific date. <br /> | ||

| Public methods ||
|---|---|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/InstantRecord#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| open [Instant](../java/time/Instant.md) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/InstantRecord#getTime()()` <br /> |
| open [ZoneOffset](../java/time/ZoneOffset.md) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/InstantRecord#getZoneOffset()()` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/InstantRecord#hashCode()()` Returns a hash code value for the object. |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record` |---|---| | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Metadata` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#getMetadata()()` <br /> | ||

## Public methods

### equals

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |
| `object` | the reference object with which to compare. This value may be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj |

### getTime

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
open fun getTime(): Instant
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/Instant.html#` | Time of the activity. This value cannot be `null`. |

### getZoneOffset

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
open fun getZoneOffset(): ZoneOffset
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#` | Zone offset of the user when the activity happened. This value cannot be `null`. |

### hashCode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hashCode(): Int
```

Returns a hash code value for the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |
