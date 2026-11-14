Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

# Record

```
abstract class Record
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.health.connect.datatypes.Record](Record.md) |

| Known Direct Subclasses [InstantRecord](InstantRecord.md), [IntervalRecord](IntervalRecord.md) |---|---| | [InstantRecord](InstantRecord.md) | A record that contains a measurement recorded as an instance . | | [IntervalRecord](IntervalRecord.md) | A record that contains a measurement with a time interval. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [ActiveCaloriesBurnedRecord](ActiveCaloriesBurnedRecord.md), [ActivityIntensityRecord](ActivityIntensityRecord.md), [AlcoholConsumptionRecord](../android/health/connect/datatypes/AlcoholConsumptionRecord.md), [BasalBodyTemperatureRecord](BasalBodyTemperatureRecord.md), [BasalMetabolicRateRecord](BasalMetabolicRateRecord.md), [BloodGlucoseRecord](BloodGlucoseRecord.md), [BloodPressureRecord](BloodPressureRecord.md), [BodyFatRecord](BodyFatRecord.md), [BodyTemperatureRecord](BodyTemperatureRecord.md), [BodyWaterMassRecord](BodyWaterMassRecord.md), [BoneMassRecord](BoneMassRecord.md), [CervicalMucusRecord](CervicalMucusRecord.md), and 33 others. |---|---| | [ActiveCaloriesBurnedRecord](ActiveCaloriesBurnedRecord.md) | Captures the estimated active energy burned by the user (in kilocalories), excluding basal metabolic rate (BMR). | | [ActivityIntensityRecord](ActivityIntensityRecord.md) | Represents intensity of an activity. | | [AlcoholConsumptionRecord](../android/health/connect/datatypes/AlcoholConsumptionRecord.md) | Captures a user's alcohol consumption. | | [BasalBodyTemperatureRecord](BasalBodyTemperatureRecord.md) | Captures the body temperature of a user when at rest (for example, immediately after waking up). | | [BasalMetabolicRateRecord](BasalMetabolicRateRecord.md) | Captures the BMR of a user. | | [BloodGlucoseRecord](BloodGlucoseRecord.md) | Captures the concentration of glucose in the blood. | | [BloodPressureRecord](BloodPressureRecord.md) | Captures the blood pressure of a user. | | [BodyFatRecord](BodyFatRecord.md) | Captures the body fat percentage of a user. | | [BodyTemperatureRecord](BodyTemperatureRecord.md) | Captures the body temperature of a user. | | [BodyWaterMassRecord](BodyWaterMassRecord.md) | Captures the user's body water mass. | | [BoneMassRecord](BoneMassRecord.md) | Captures the user's bone mass. | | [CervicalMucusRecord](CervicalMucusRecord.md) | Captures the description of cervical mucus. | | [CyclingPedalingCadenceRecord](CyclingPedalingCadenceRecord.md) | Captures the user's cycling pedaling cadence. | | [DistanceRecord](DistanceRecord.md) | Captures distance travelled by the user since the last reading. | | [ElevationGainedRecord](ElevationGainedRecord.md) | Captures the elevation gained by the user since the last reading. | | [ExerciseSessionRecord](ExerciseSessionRecord.md) | Captures exercise or a sequence of exercises. | | [FloorsClimbedRecord](FloorsClimbedRecord.md) | Captures the number of floors climbed by the user between the start and end time. | | [HeartRateRecord](HeartRateRecord.md) | Captures the user's heart rate. | | [HeartRateVariabilityRmssdRecord](HeartRateVariabilityRmssdRecord.md) | Captures the user's heart rate variability RMSSD. | | [HeightRecord](HeightRecord.md) | Captures the user's height. | | [HydrationRecord](HydrationRecord.md) | Captures the amount of liquids user had in a single drink. | | [IntermenstrualBleedingRecord](IntermenstrualBleedingRecord.md) | Captures the user's inter-menstrual bleeding. | | [LeanBodyMassRecord](LeanBodyMassRecord.md) | Captures the user's lean body mass. | | [MenstrualCyclePhaseRecord](../android/health/connect/datatypes/MenstrualCyclePhaseRecord.md) | Represents a user's menstrual cycle phase for a specific day. | | [MenstruationFlowRecord](MenstruationFlowRecord.md) | Captures a description of how heavy a user's menstrual flow was (spotting, light, medium, or heavy). | | [MenstruationPeriodRecord](MenstruationPeriodRecord.md) | Captures the menstruation period record. | | [MindfulnessSessionRecord](MindfulnessSessionRecord.md) | Captures a mindfulness session. | | [NutritionRecord](NutritionRecord.md) | Captures what nutrients were consumed as part of a meal or a food item. | | [OvulationTestRecord](OvulationTestRecord.md) | Each record represents the result of an ovulation test. | | [OxygenSaturationRecord](OxygenSaturationRecord.md) | Captures the amount of oxygen circulating in the blood, measured as a percentage of oxygen-saturated hemoglobin. | | [PlannedExerciseSessionRecord](PlannedExerciseSessionRecord.md) | Captures a planned exercise session, also commonly referred to as a training plan. | | [PowerRecord](PowerRecord.md) | Captures the power generated by the user, e. | | [RespiratoryRateRecord](RespiratoryRateRecord.md) | Captures the user's respiratory rate. | | [RestingHeartRateRecord](RestingHeartRateRecord.md) | Captures the user's resting heart rate. | | [SexualActivityRecord](SexualActivityRecord.md) | Captures an occurrence of sexual activity. | | [SkinTemperatureRecord](SkinTemperatureRecord.md) | Captures the skin temperature of a user. | | [SleepSessionRecord](SleepSessionRecord.md) | Captures the user's sleep length and its stages. | | [SpeedRecord](SpeedRecord.md) | Captures the user's speed, e. | | [StepsCadenceRecord](StepsCadenceRecord.md) | Captures the user's steps cadence. | | [StepsRecord](StepsRecord.md) | Captures the number of steps taken since the last reading. | | [SymptomRecord](../android/health/connect/datatypes/SymptomRecord.md) | Captures a description of a user's symptom. | | [TotalCaloriesBurnedRecord](TotalCaloriesBurnedRecord.md) | Total energy burned by the user in `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Energy`, including active \& basal energy burned (BMR). | | [Vo2MaxRecord](Vo2MaxRecord.md) | Capture user's VO2 max score and optionally the measurement method. | | [WeightRecord](WeightRecord.md) | Captures the user's weight. | | [WheelchairPushesRecord](WheelchairPushesRecord.md) | Captures the number of wheelchair pushes done over a time interval. | |
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
| open [Metadata](Metadata.md) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#getMetadata()()` <br /> |
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
