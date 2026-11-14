Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

# InstantRecord

```
abstract class InstantRecord : Record
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [android.health.connect.datatypes.Record](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record) ||
| | ↳ | [android.health.connect.datatypes.InstantRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/InstantRecord#) |

| Known Direct Subclasses [BasalBodyTemperatureRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/BasalBodyTemperatureRecord), [BasalMetabolicRateRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/BasalMetabolicRateRecord), [BloodGlucoseRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/BloodGlucoseRecord), [BloodPressureRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/BloodPressureRecord), [BodyFatRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/BodyFatRecord), [BodyTemperatureRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/BodyTemperatureRecord), [BodyWaterMassRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/BodyWaterMassRecord), [BoneMassRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/BoneMassRecord), [CervicalMucusRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/CervicalMucusRecord), [HeartRateVariabilityRmssdRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/HeartRateVariabilityRmssdRecord), [HeightRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/HeightRecord), [IntermenstrualBleedingRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/IntermenstrualBleedingRecord), and 9 others. |---|---| | [BasalBodyTemperatureRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/BasalBodyTemperatureRecord) | Captures the body temperature of a user when at rest (for example, immediately after waking up). | | [BasalMetabolicRateRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/BasalMetabolicRateRecord) | Captures the BMR of a user. | | [BloodGlucoseRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/BloodGlucoseRecord) | Captures the concentration of glucose in the blood. | | [BloodPressureRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/BloodPressureRecord) | Captures the blood pressure of a user. | | [BodyFatRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/BodyFatRecord) | Captures the body fat percentage of a user. | | [BodyTemperatureRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/BodyTemperatureRecord) | Captures the body temperature of a user. | | [BodyWaterMassRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/BodyWaterMassRecord) | Captures the user's body water mass. | | [BoneMassRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/BoneMassRecord) | Captures the user's bone mass. | | [CervicalMucusRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/CervicalMucusRecord) | Captures the description of cervical mucus. | | [HeartRateVariabilityRmssdRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/HeartRateVariabilityRmssdRecord) | Captures the user's heart rate variability RMSSD. | | [HeightRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/HeightRecord) | Captures the user's height. | | [IntermenstrualBleedingRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/IntermenstrualBleedingRecord) | Captures the user's inter-menstrual bleeding. | | [LeanBodyMassRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/LeanBodyMassRecord) | Captures the user's lean body mass. | | [MenstruationFlowRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MenstruationFlowRecord) | Captures a description of how heavy a user's menstrual flow was (spotting, light, medium, or heavy). | | [OvulationTestRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/OvulationTestRecord) | Each record represents the result of an ovulation test. | | [OxygenSaturationRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/OxygenSaturationRecord) | Captures the amount of oxygen circulating in the blood, measured as a percentage of oxygen-saturated hemoglobin. | | [RespiratoryRateRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/RespiratoryRateRecord) | Captures the user's respiratory rate. | | [RestingHeartRateRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/RestingHeartRateRecord) | Captures the user's resting heart rate. | | [SexualActivityRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/SexualActivityRecord) | Captures an occurrence of sexual activity. | | [Vo2MaxRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Vo2MaxRecord) | Capture user's VO2 max score and optionally the measurement method. | | [WeightRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/WeightRecord) | Captures the user's weight. | |

A record that contains a measurement recorded as an instance .

## Summary

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_INSTANT:kotlin.Int` The record represents an instantaneous event. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_INTERVAL:kotlin.Int` The record represents an event over an interval. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_LOCAL_DATE:kotlin.Int` The record represents an event that occurred on a specific date. <br /> | ||

| Public methods ||
|---|---|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/InstantRecord#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| open [Instant](https://developer.android.com/reference/kotlin/java/time/Instant.html#) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/InstantRecord#getTime()()` <br /> |
| open [ZoneOffset](https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/InstantRecord#getZoneOffset()()` <br /> |
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
