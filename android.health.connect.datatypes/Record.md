Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

# Record

```
abstract class Record
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.health.connect.datatypes.Record](../android/health/connect/datatypes/Record.md) |

| Known Direct Subclasses [InstantRecord](../android/health/connect/datatypes/InstantRecord.md), [IntervalRecord](../android/health/connect/datatypes/IntervalRecord.md) |---|---| | [InstantRecord](../android/health/connect/datatypes/InstantRecord.md) | A record that contains a measurement recorded as an instance . | | [IntervalRecord](../android/health/connect/datatypes/IntervalRecord.md) | A record that contains a measurement with a time interval. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [ActiveCaloriesBurnedRecord](../android/health/connect/datatypes/ActiveCaloriesBurnedRecord.md), [ActivityIntensityRecord](../android/health/connect/datatypes/ActivityIntensityRecord.md), [AlcoholConsumptionRecord](../android/health/connect/datatypes/AlcoholConsumptionRecord.md), [BasalBodyTemperatureRecord](../android/health/connect/datatypes/BasalBodyTemperatureRecord.md), [BasalMetabolicRateRecord](../android/health/connect/datatypes/BasalMetabolicRateRecord.md), [BloodGlucoseRecord](../android/health/connect/datatypes/BloodGlucoseRecord.md), [BloodPressureRecord](../android/health/connect/datatypes/BloodPressureRecord.md), [BodyFatRecord](../android/health/connect/datatypes/BodyFatRecord.md), [BodyTemperatureRecord](../android/health/connect/datatypes/BodyTemperatureRecord.md), [BodyWaterMassRecord](../android/health/connect/datatypes/BodyWaterMassRecord.md), [BoneMassRecord](../android/health/connect/datatypes/BoneMassRecord.md), [CervicalMucusRecord](../android/health/connect/datatypes/CervicalMucusRecord.md), and 33 others. |---|---| | [ActiveCaloriesBurnedRecord](../android/health/connect/datatypes/ActiveCaloriesBurnedRecord.md) | Captures the estimated active energy burned by the user (in kilocalories), excluding basal metabolic rate (BMR). | | [ActivityIntensityRecord](../android/health/connect/datatypes/ActivityIntensityRecord.md) | Represents intensity of an activity. | | [AlcoholConsumptionRecord](../android/health/connect/datatypes/AlcoholConsumptionRecord.md) | Captures a user's alcohol consumption. | | [BasalBodyTemperatureRecord](../android/health/connect/datatypes/BasalBodyTemperatureRecord.md) | Captures the body temperature of a user when at rest (for example, immediately after waking up). | | [BasalMetabolicRateRecord](../android/health/connect/datatypes/BasalMetabolicRateRecord.md) | Captures the BMR of a user. | | [BloodGlucoseRecord](../android/health/connect/datatypes/BloodGlucoseRecord.md) | Captures the concentration of glucose in the blood. | | [BloodPressureRecord](../android/health/connect/datatypes/BloodPressureRecord.md) | Captures the blood pressure of a user. | | [BodyFatRecord](../android/health/connect/datatypes/BodyFatRecord.md) | Captures the body fat percentage of a user. | | [BodyTemperatureRecord](../android/health/connect/datatypes/BodyTemperatureRecord.md) | Captures the body temperature of a user. | | [BodyWaterMassRecord](../android/health/connect/datatypes/BodyWaterMassRecord.md) | Captures the user's body water mass. | | [BoneMassRecord](../android/health/connect/datatypes/BoneMassRecord.md) | Captures the user's bone mass. | | [CervicalMucusRecord](../android/health/connect/datatypes/CervicalMucusRecord.md) | Captures the description of cervical mucus. | | [CyclingPedalingCadenceRecord](../android/health/connect/datatypes/CyclingPedalingCadenceRecord.md) | Captures the user's cycling pedaling cadence. | | [DistanceRecord](../android/health/connect/datatypes/DistanceRecord.md) | Captures distance travelled by the user since the last reading. | | [ElevationGainedRecord](../android/health/connect/datatypes/ElevationGainedRecord.md) | Captures the elevation gained by the user since the last reading. | | [ExerciseSessionRecord](../android/health/connect/datatypes/ExerciseSessionRecord.md) | Captures exercise or a sequence of exercises. | | [FloorsClimbedRecord](../android/health/connect/datatypes/FloorsClimbedRecord.md) | Captures the number of floors climbed by the user between the start and end time. | | [HeartRateRecord](../android/health/connect/datatypes/HeartRateRecord.md) | Captures the user's heart rate. | | [HeartRateVariabilityRmssdRecord](../android/health/connect/datatypes/HeartRateVariabilityRmssdRecord.md) | Captures the user's heart rate variability RMSSD. | | [HeightRecord](../android/health/connect/datatypes/HeightRecord.md) | Captures the user's height. | | [HydrationRecord](../android/health/connect/datatypes/HydrationRecord.md) | Captures the amount of liquids user had in a single drink. | | [IntermenstrualBleedingRecord](../android/health/connect/datatypes/IntermenstrualBleedingRecord.md) | Captures the user's inter-menstrual bleeding. | | [LeanBodyMassRecord](../android/health/connect/datatypes/LeanBodyMassRecord.md) | Captures the user's lean body mass. | | [MenstrualCyclePhaseRecord](../android/health/connect/datatypes/MenstrualCyclePhaseRecord.md) | Represents a user's menstrual cycle phase for a specific day. | | [MenstruationFlowRecord](../android/health/connect/datatypes/MenstruationFlowRecord.md) | Captures a description of how heavy a user's menstrual flow was (spotting, light, medium, or heavy). | | [MenstruationPeriodRecord](../android/health/connect/datatypes/MenstruationPeriodRecord.md) | Captures the menstruation period record. | | [MindfulnessSessionRecord](../android/health/connect/datatypes/MindfulnessSessionRecord.md) | Captures a mindfulness session. | | [NutritionRecord](../android/health/connect/datatypes/NutritionRecord.md) | Captures what nutrients were consumed as part of a meal or a food item. | | [OvulationTestRecord](../android/health/connect/datatypes/OvulationTestRecord.md) | Each record represents the result of an ovulation test. | | [OxygenSaturationRecord](../android/health/connect/datatypes/OxygenSaturationRecord.md) | Captures the amount of oxygen circulating in the blood, measured as a percentage of oxygen-saturated hemoglobin. | | [PlannedExerciseSessionRecord](../android/health/connect/datatypes/PlannedExerciseSessionRecord.md) | Captures a planned exercise session, also commonly referred to as a training plan. | | [PowerRecord](../android/health/connect/datatypes/PowerRecord.md) | Captures the power generated by the user, e. | | [RespiratoryRateRecord](../android/health/connect/datatypes/RespiratoryRateRecord.md) | Captures the user's respiratory rate. | | [RestingHeartRateRecord](../android/health/connect/datatypes/RestingHeartRateRecord.md) | Captures the user's resting heart rate. | | [SexualActivityRecord](../android/health/connect/datatypes/SexualActivityRecord.md) | Captures an occurrence of sexual activity. | | [SkinTemperatureRecord](../android/health/connect/datatypes/SkinTemperatureRecord.md) | Captures the skin temperature of a user. | | [SleepSessionRecord](../android/health/connect/datatypes/SleepSessionRecord.md) | Captures the user's sleep length and its stages. | | [SpeedRecord](../android/health/connect/datatypes/SpeedRecord.md) | Captures the user's speed, e. | | [StepsCadenceRecord](../android/health/connect/datatypes/StepsCadenceRecord.md) | Captures the user's steps cadence. | | [StepsRecord](../android/health/connect/datatypes/StepsRecord.md) | Captures the number of steps taken since the last reading. | | [SymptomRecord](../android/health/connect/datatypes/SymptomRecord.md) | Captures a description of a user's symptom. | | [TotalCaloriesBurnedRecord](../android/health/connect/datatypes/TotalCaloriesBurnedRecord.md) | Total energy burned by the user in `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Energy`, including active \& basal energy burned (BMR). | | [Vo2MaxRecord](../android/health/connect/datatypes/Vo2MaxRecord.md) | Capture user's VO2 max score and optionally the measurement method. | | [WeightRecord](../android/health/connect/datatypes/WeightRecord.md) | Captures the user's weight. | | [WheelchairPushesRecord](../android/health/connect/datatypes/WheelchairPushesRecord.md) | Captures the number of wheelchair pushes done over a time interval. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A base class for all record classes

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_INSTANT:kotlin.Int` The record represents an instantaneous event. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_INTERVAL:kotlin.Int` The record represents an event over an interval. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_LOCAL_DATE:kotlin.Int` The record represents an event that occurred on a specific date. |
| --- | --- |

| Public methods ||
|---|---|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| open [Metadata](../android/health/connect/datatypes/Metadata.md) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#getMetadata()()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#hashCode()()` Returns a hash code value for the object. |
| --- | --- |

## Constants

### RECORD_TEMPORAL_TYPE_INSTANT

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 23](https://developer.android.com/sdkExtensions)

```
static val RECORD_TEMPORAL_TYPE_INSTANT: Int
```

The record represents an instantaneous event.

 Value: 0

### RECORD_TEMPORAL_TYPE_INTERVAL

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 23](https://developer.android.com/sdkExtensions)

```
static val RECORD_TEMPORAL_TYPE_INTERVAL: Int
```

The record represents an event over an interval.

 Value: 1

### RECORD_TEMPORAL_TYPE_LOCAL_DATE

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 23](https://developer.android.com/sdkExtensions)

```
static val RECORD_TEMPORAL_TYPE_LOCAL_DATE: Int
```

The record represents an event that occurred on a specific date.

 Value: 2

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

### getMetadata

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
open fun getMetadata(): Metadata
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Metadata` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Metadata` for this record. This value cannot be `null`. |

### hashCode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hashCode(): Int
```

Returns a hash code value for the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |
