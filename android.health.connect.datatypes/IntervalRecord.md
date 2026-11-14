Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

# IntervalRecord

```
abstract class IntervalRecord : Record
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.health.connect.datatypes.Record](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record) ||
| | ↳ | [android.health.connect.datatypes.IntervalRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/IntervalRecord#) |

| Known Direct Subclasses [ActiveCaloriesBurnedRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ActiveCaloriesBurnedRecord), [ActivityIntensityRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ActivityIntensityRecord), [AlcoholConsumptionRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AlcoholConsumptionRecord), [CyclingPedalingCadenceRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/CyclingPedalingCadenceRecord), [DistanceRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/DistanceRecord), [ElevationGainedRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ElevationGainedRecord), [ExerciseSessionRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionRecord), [FloorsClimbedRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FloorsClimbedRecord), [HeartRateRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/HeartRateRecord), [HydrationRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/HydrationRecord), [MenstrualCyclePhaseRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MenstrualCyclePhaseRecord), [MenstruationPeriodRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MenstruationPeriodRecord), and 12 others. |---|---| | [ActiveCaloriesBurnedRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ActiveCaloriesBurnedRecord) | Captures the estimated active energy burned by the user (in kilocalories), excluding basal metabolic rate (BMR). | | [ActivityIntensityRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ActivityIntensityRecord) | Represents intensity of an activity. | | [AlcoholConsumptionRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AlcoholConsumptionRecord) | Captures a user's alcohol consumption. | | [CyclingPedalingCadenceRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/CyclingPedalingCadenceRecord) | Captures the user's cycling pedaling cadence. | | [DistanceRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/DistanceRecord) | Captures distance travelled by the user since the last reading. | | [ElevationGainedRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ElevationGainedRecord) | Captures the elevation gained by the user since the last reading. | | [ExerciseSessionRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionRecord) | Captures exercise or a sequence of exercises. | | [FloorsClimbedRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/FloorsClimbedRecord) | Captures the number of floors climbed by the user between the start and end time. | | [HeartRateRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/HeartRateRecord) | Captures the user's heart rate. | | [HydrationRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/HydrationRecord) | Captures the amount of liquids user had in a single drink. | | [MenstrualCyclePhaseRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MenstrualCyclePhaseRecord) | Represents a user's menstrual cycle phase for a specific day. | | [MenstruationPeriodRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MenstruationPeriodRecord) | Captures the menstruation period record. | | [MindfulnessSessionRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MindfulnessSessionRecord) | Captures a mindfulness session. | | [NutritionRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/NutritionRecord) | Captures what nutrients were consumed as part of a meal or a food item. | | [PlannedExerciseSessionRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/PlannedExerciseSessionRecord) | Captures a planned exercise session, also commonly referred to as a training plan. | | [PowerRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/PowerRecord) | Captures the power generated by the user, e. | | [SkinTemperatureRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/SkinTemperatureRecord) | Captures the skin temperature of a user. | | [SleepSessionRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/SleepSessionRecord) | Captures the user's sleep length and its stages. | | [SpeedRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/SpeedRecord) | Captures the user's speed, e. | | [StepsCadenceRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/StepsCadenceRecord) | Captures the user's steps cadence. | | [StepsRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/StepsRecord) | Captures the number of steps taken since the last reading. | | [SymptomRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/SymptomRecord) | Captures a description of a user's symptom. | | [TotalCaloriesBurnedRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/TotalCaloriesBurnedRecord) | Total energy burned by the user in `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/units/Energy`, including active \& basal energy burned (BMR). | | [WheelchairPushesRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/WheelchairPushesRecord) | Captures the number of wheelchair pushes done over a time interval. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A record that contains a measurement with a time interval.

## Summary

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_INSTANT:kotlin.Int` The record represents an instantaneous event. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_INTERVAL:kotlin.Int` The record represents an event over an interval. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_LOCAL_DATE:kotlin.Int` The record represents an event that occurred on a specific date. <br /> | ||

| Public methods ||
|---|---|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/IntervalRecord#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| open [Instant](https://developer.android.com/reference/kotlin/java/time/Instant.html#) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/IntervalRecord#getEndTime()()` <br /> |
| open [ZoneOffset](https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/IntervalRecord#getEndZoneOffset()()` <br /> |
| --- | --- |
| open [Instant](https://developer.android.com/reference/kotlin/java/time/Instant.html#) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/IntervalRecord#getStartTime()()` <br /> |
| open [ZoneOffset](https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/IntervalRecord#getStartZoneOffset()()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/IntervalRecord#hashCode()()` Returns a hash code value for the object. |
| --- | --- |

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

### getEndTime

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
open fun getEndTime(): Instant
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/Instant.html#` | End time of the activity. This value cannot be `null`. |

### getEndZoneOffset

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
open fun getEndZoneOffset(): ZoneOffset
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#` | End time's zone offset of the activity. This value cannot be `null`. |

### getStartTime

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
open fun getStartTime(): Instant
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/Instant.html#` | Start time of the activity. This value cannot be `null`. |

### getStartZoneOffset

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
open fun getStartZoneOffset(): ZoneOffset
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#` | Start time's zone offset of the activity. This value cannot be `null`. |

### hashCode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hashCode(): Int
```

Returns a hash code value for the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |
