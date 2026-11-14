# android.health.connect.datatypes

# android.health.connect.datatypes

Kotlin| [Java](_package.md)
| --- | --- |

## Classes

| [ActiveCaloriesBurnedRecord](ActiveCaloriesBurnedRecord.md) | Captures the estimated active energy burned by the user (in kilocalories), excluding basal metabolic rate (BMR). |
| --- | --- |
| [ActivityIntensityRecord](ActivityIntensityRecord.md) | Represents intensity of an activity. |
| [AggregationType](AggregationType.md) | Class to represent aggregation types in [Record](Record.md) classes. |
| [AppInfo](AppInfo.md) | Application Info class containing details about a given application |
| --- | --- |
| [BasalBodyTemperatureRecord](BasalBodyTemperatureRecord.md) | Captures the body temperature of a user when at rest (for example, immediately after waking up). |
| [BasalMetabolicRateRecord](BasalMetabolicRateRecord.md) | Captures the BMR of a user. |
| [BloodGlucoseRecord](BloodGlucoseRecord.md) | Captures the concentration of glucose in the blood. |
| --- | --- |
| [BloodPressureRecord](BloodPressureRecord.md) | Captures the blood pressure of a user. |
| [BodyFatRecord](BodyFatRecord.md) | Captures the body fat percentage of a user. |
| [BodyTemperatureMeasurementLocation](BodyTemperatureMeasurementLocation.md) | Where on the user's body a temperature measurement was taken from. |
| --- | --- |
| [BodyTemperatureRecord](BodyTemperatureRecord.md) | Captures the body temperature of a user. |
| [BodyWaterMassRecord](BodyWaterMassRecord.md) | Captures the user's body water mass. |
| [BoneMassRecord](BoneMassRecord.md) | Captures the user's bone mass. |
| --- | --- |
| [CervicalMucusRecord](CervicalMucusRecord.md) | Captures the description of cervical mucus. |
| [CyclingPedalingCadenceRecord](CyclingPedalingCadenceRecord.md) | Captures the user's cycling pedaling cadence. |
| [DataOrigin](DataOrigin.md) | Specifies the contributing source/application of any [Record](Record.md) |
| --- | --- |
| [Device](Device.md) | A physical device (such as phone, watch, scale, or chest strap) which captured associated health data point. |
| [DistanceRecord](DistanceRecord.md) | Captures distance travelled by the user since the last reading. |
| [ElevationGainedRecord](ElevationGainedRecord.md) | Captures the elevation gained by the user since the last reading. |
| --- | --- |
| [ExerciseCompletionGoal](ExerciseCompletionGoal.md) | A goal which should be met to complete a [PlannedExerciseStep](PlannedExerciseStep.md). |
| [ExerciseLap](ExerciseLap.md) | Captures the time of a lap within exercise session. |
| [ExercisePerformanceGoal](ExercisePerformanceGoal.md) | A goal which should be aimed for during a [PlannedExerciseStep](PlannedExerciseStep.md). |
| --- | --- |
| [ExerciseRoute](ExerciseRoute.md) | Route of the exercise session. |
| [ExerciseSegment](ExerciseSegment.md) | Represents particular exercise within exercise session (see [ExerciseSessionRecord](ExerciseSessionRecord.md)). |
| [ExerciseSegmentType](ExerciseSegmentType.md) | Identifier for exercise types, as returned by [ExerciseSegment.getSegmentType()](ExerciseSegment.md)). |
| --- | --- |
| [ExerciseSessionRecord](ExerciseSessionRecord.md) | Captures exercise or a sequence of exercises. |
| [ExerciseSessionType](ExerciseSessionType.md) | Identifier for exercise types, as returned by [ExerciseSessionRecord.getExerciseType()](ExerciseSessionRecord.md)). |
| [FhirResource](FhirResource.md) | A class to capture the FHIR resource data. |
| --- | --- |
| [FhirVersion](FhirVersion.md) | Represents the FHIR version. |
| [FloorsClimbedRecord](FloorsClimbedRecord.md) | Captures the number of floors climbed by the user between the start and end time. |
| [HeartRateRecord](HeartRateRecord.md) | Captures the user's heart rate. |
| --- | --- |
| [HeartRateVariabilityRmssdRecord](HeartRateVariabilityRmssdRecord.md) | Captures the user's heart rate variability RMSSD. |
| [HeightRecord](HeightRecord.md) | Captures the user's height. |
| [HydrationRecord](HydrationRecord.md) | Captures the amount of liquids user had in a single drink. |
| --- | --- |
| [InstantRecord](InstantRecord.md) | A record that contains a measurement recorded as an instance . |
| [IntermenstrualBleedingRecord](IntermenstrualBleedingRecord.md) | Captures the user's inter-menstrual bleeding. |
| [IntervalRecord](IntervalRecord.md) | A record that contains a measurement with a time interval. |
| --- | --- |
| [LeanBodyMassRecord](LeanBodyMassRecord.md) | Captures the user's lean body mass. |
| [MealType](MealType.md) | Identifier for the meal type. |
| [MedicalDataSource](MedicalDataSource.md) | Captures the data source information of medical data. |
| --- | --- |
| [MedicalResource](MedicalResource.md) | A class to capture the user's medical data. |
| [MenstruationFlowRecord](MenstruationFlowRecord.md) | Captures a description of how heavy a user's menstrual flow was (spotting, light, medium, or heavy). |
| [MenstruationPeriodRecord](MenstruationPeriodRecord.md) | Captures the menstruation period record. |
| --- | --- |
| [Metadata](Metadata.md) | Set of shared metadata fields for [Record](Record.md) |
| [MindfulnessSessionRecord](MindfulnessSessionRecord.md) | Captures a mindfulness session. |
| [NutritionRecord](NutritionRecord.md) | Captures what nutrients were consumed as part of a meal or a food item. |
| --- | --- |
| [OvulationTestRecord](OvulationTestRecord.md) | Each record represents the result of an ovulation test. |
| [OxygenSaturationRecord](OxygenSaturationRecord.md) | Captures the amount of oxygen circulating in the blood, measured as a percentage of oxygen-saturated hemoglobin. |
| [PlannedExerciseBlock](PlannedExerciseBlock.md) | Represents a series of [PlannedExerciseStep](PlannedExerciseStep.md). |
| --- | --- |
| [PlannedExerciseSessionRecord](PlannedExerciseSessionRecord.md) | Captures a planned exercise session, also commonly referred to as a training plan. |
| [PlannedExerciseStep](PlannedExerciseStep.md) | A single step within an [PlannedExerciseBlock](PlannedExerciseBlock.md) e. |
| [PowerRecord](PowerRecord.md) | Captures the power generated by the user, e. |
| --- | --- |
| [Record](Record.md) | A base class for all record classes |
| [RespiratoryRateRecord](RespiratoryRateRecord.md) | Captures the user's respiratory rate. |
| [RestingHeartRateRecord](RestingHeartRateRecord.md) | Captures the user's resting heart rate. |
| --- | --- |
| [SexualActivityRecord](SexualActivityRecord.md) | Captures an occurrence of sexual activity. |
| [SkinTemperatureRecord](SkinTemperatureRecord.md) | Captures the skin temperature of a user. |
| [SleepSessionRecord](SleepSessionRecord.md) | Captures the user's sleep length and its stages. |
| --- | --- |
| [SpeedRecord](SpeedRecord.md) | Captures the user's speed, e. |
| [StepsCadenceRecord](StepsCadenceRecord.md) | Captures the user's steps cadence. |
| [StepsRecord](StepsRecord.md) | Captures the number of steps taken since the last reading. |
| --- | --- |
| [TotalCaloriesBurnedRecord](TotalCaloriesBurnedRecord.md) | Total energy burned by the user in [Energy](../android.health.connect.datatypes.units/Energy.md), including active \& basal energy burned (BMR). |
| [Vo2MaxRecord](Vo2MaxRecord.md) | Capture user's VO2 max score and optionally the measurement method. |
| [WeightRecord](WeightRecord.md) | Captures the user's weight. |
| --- | --- |
| [WheelchairPushesRecord](WheelchairPushesRecord.md) | Captures the number of wheelchair pushes done over a time interval. |
