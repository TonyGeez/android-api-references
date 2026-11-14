Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

# Record

```
abstract class Record
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.health.connect.datatypes.Record](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#) |

| Known Direct Subclasses [InstantRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/InstantRecord), [IntervalRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/IntervalRecord) |---|---| | [InstantRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/InstantRecord) | A record that contains a measurement recorded as an instance . | | [IntervalRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/IntervalRecord) | A record that contains a measurement with a time interval. | |

| Known Indirect Subclasses [ActiveCaloriesBurnedRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ActiveCaloriesBurnedRecord), [ActivityIntensityRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ActivityIntensityRecord), [AlcoholConsumptionRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AlcoholConsumptionRecord), [BasalBodyTemperatureRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/BasalBodyTemperatureRecord), [BasalMetabolicRateRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/BasalMetabolicRateRecord), [BloodGlucoseRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/BloodGlucoseRecord), [BloodPressureRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/BloodPressureRecord), [BodyFatRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/BodyFatRecord), [BodyTemperatureRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/BodyTemperatureRecord), [BodyWaterMassRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/BodyWaterMassRecord), [BoneMassRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/BoneMassRecord), [CervicalMucusRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/CervicalMucusRecord), and 33 others. |---|---| | [ActiveCaloriesBurnedRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ActiveCaloriesBurnedRecord) | Captures the estimated active energy burned by the user (in kilocalories), excluding basal metabolic rate (BMR). | | [ActivityIntensityRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ActivityIntensityRecord) | Represents intensity of an activity. | | [AlcoholConsumptionRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AlcoholConsumptionRecord) | Captures a user's alcohol consumption. | | [BasalBodyTemperatureRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/BasalBodyTemperatureRecord) | Captures the body temperature of a user when at rest (for example, immediately after waking up). | | [BasalMetabolicRateRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/BasalMetabolicRateRecord) | Captures the BMR of a user. | | [BloodGlucoseRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/BloodGlucoseRecord) | Captures the concentration of glucose in the blood. | | [BloodPressureRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/BloodPressureRecord) | Captures the blood pressure of a user. | | [BodyFatRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/BodyFatRecord) | Captures the body fat percentage of a user. | | [BodyTemperatureRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/BodyTemperatureRecord) | Captures the body temperature of a user. | | [BodyWaterMassRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/BodyWaterMassRecord) | Captures the user's body water mass. | | [BoneMassRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/BoneMassRecord) | Captures the user's bone mass. | | [CervicalMucusRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/CervicalMucusRecord) | Captures the description of cervical mucus. | | [CyclingPedalingCadenceRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/CyclingPedalingCadenceRecord) | Captures the user's cycling pedaling cadence. | | [DistanceRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/DistanceRecord) | Captures distance travelled by the user since the last reading. | | [ElevationGainedRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ElevationGainedRecord) | Captures the elevation gained by the user since the last reading. | | [ExerciseSessionRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionRecord) | Captures exercise or a sequence of exercises. | | [FloorsClimbedRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FloorsClimbedRecord) | Captures the number of floors climbed by the user between the start and end time. | | [HeartRateRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/HeartRateRecord) | Captures the user's heart rate. | | [HeartRateVariabilityRmssdRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/HeartRateVariabilityRmssdRecord) | Captures the user's heart rate variability RMSSD. | | [HeightRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/HeightRecord) | Captures the user's height. | | [HydrationRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/HydrationRecord) | Captures the amount of liquids user had in a single drink. | | [IntermenstrualBleedingRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/IntermenstrualBleedingRecord) | Captures the user's inter-menstrual bleeding. | | [LeanBodyMassRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/LeanBodyMassRecord) | Captures the user's lean body mass. | | [MenstrualCyclePhaseRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MenstrualCyclePhaseRecord) | Represents a user's menstrual cycle phase for a specific day. | | [MenstruationFlowRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MenstruationFlowRecord) | Captures a description of how heavy a user's menstrual flow was (spotting, light, medium, or heavy). | | [MenstruationPeriodRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MenstruationPeriodRecord) | Captures the menstruation period record. | | [MindfulnessSessionRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MindfulnessSessionRecord) | Captures a mindfulness session. | | [NutritionRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord) | Captures what nutrients were consumed as part of a meal or a food item. | | [OvulationTestRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/OvulationTestRecord) | Each record represents the result of an ovulation test. | | [OxygenSaturationRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/OxygenSaturationRecord) | Captures the amount of oxygen circulating in the blood, measured as a percentage of oxygen-saturated hemoglobin. | | [PlannedExerciseSessionRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/PlannedExerciseSessionRecord) | Captures a planned exercise session, also commonly referred to as a training plan. | | [PowerRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/PowerRecord) | Captures the power generated by the user, e. | | [RespiratoryRateRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/RespiratoryRateRecord) | Captures the user's respiratory rate. | | [RestingHeartRateRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/RestingHeartRateRecord) | Captures the user's resting heart rate. | | [SexualActivityRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/SexualActivityRecord) | Captures an occurrence of sexual activity. | | [SkinTemperatureRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/SkinTemperatureRecord) | Captures the skin temperature of a user. | | [SleepSessionRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/SleepSessionRecord) | Captures the user's sleep length and its stages. | | [SpeedRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/SpeedRecord) | Captures the user's speed, e. | | [StepsCadenceRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/StepsCadenceRecord) | Captures the user's steps cadence. | | [StepsRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/StepsRecord) | Captures the number of steps taken since the last reading. | | [SymptomRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/SymptomRecord) | Captures a description of a user's symptom. | | [TotalCaloriesBurnedRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/TotalCaloriesBurnedRecord) | Total energy burned by the user in `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Energy`, including active \& basal energy burned (BMR). | | [Vo2MaxRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Vo2MaxRecord) | Capture user's VO2 max score and optionally the measurement method. | | [WeightRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/WeightRecord) | Captures the user's weight. | | [WheelchairPushesRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/WheelchairPushesRecord) | Captures the number of wheelchair pushes done over a time interval. | |

A base class for all record classes

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_INSTANT:kotlin.Int` The record represents an instantaneous event. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_INTERVAL:kotlin.Int` The record represents an event over an interval. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_LOCAL_DATE:kotlin.Int` The record represents an event that occurred on a specific date. |

| Public methods ||
|---|---|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| open [Metadata](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Metadata) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#getMetadata()()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#hashCode()()` Returns a hash code value for the object. |

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
