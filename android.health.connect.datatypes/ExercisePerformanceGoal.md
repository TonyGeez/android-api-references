# ExercisePerformanceGoal

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 13](https://developer.android.com/sdkExtensions)

# ExercisePerformanceGoal

Kotlin| [Java](ExercisePerformanceGoal.md) 
| --- | --- |

```
abstract class ExercisePerformanceGoal
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.health.connect.datatypes.ExercisePerformanceGoal](ExercisePerformanceGoal.md) |

| Known Direct Subclasses [ExercisePerformanceGoal.AmrapGoal](../android/health/connect/datatypes/ExercisePerformanceGoal.AmrapGoal.md), [ExercisePerformanceGoal.CadenceGoal](../android/health/connect/datatypes/ExercisePerformanceGoal.CadenceGoal.md), [ExercisePerformanceGoal.HeartRateGoal](../android/health/connect/datatypes/ExercisePerformanceGoal.HeartRateGoal.md), [ExercisePerformanceGoal.PowerGoal](../android/health/connect/datatypes/ExercisePerformanceGoal.PowerGoal.md), [ExercisePerformanceGoal.RateOfPerceivedExertionGoal](../android/health/connect/datatypes/ExercisePerformanceGoal.RateOfPerceivedExertionGoal.md), [ExercisePerformanceGoal.SpeedGoal](../android/health/connect/datatypes/ExercisePerformanceGoal.SpeedGoal.md), [ExercisePerformanceGoal.UnknownGoal](../android/health/connect/datatypes/ExercisePerformanceGoal.UnknownGoal.md), [ExercisePerformanceGoal.WeightGoal](../android/health/connect/datatypes/ExercisePerformanceGoal.WeightGoal.md) |--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ExercisePerformanceGoal.AmrapGoal](../android/health/connect/datatypes/ExercisePerformanceGoal.AmrapGoal.md) | An [ExercisePerformanceGoal](ExercisePerformanceGoal.md) that requires completing as many repetitions as possible. | | [ExercisePerformanceGoal.CadenceGoal](../android/health/connect/datatypes/ExercisePerformanceGoal.CadenceGoal.md) | An [ExercisePerformanceGoal](ExercisePerformanceGoal.md) that requires a target cadence range to be met during the associated [PlannedExerciseStep](PlannedExerciseStep.md). | | [ExercisePerformanceGoal.HeartRateGoal](../android/health/connect/datatypes/ExercisePerformanceGoal.HeartRateGoal.md) | An [ExercisePerformanceGoal](ExercisePerformanceGoal.md) that requires a target heart rate range, in BPM, to be met during the associated [PlannedExerciseStep](PlannedExerciseStep.md). | | [ExercisePerformanceGoal.PowerGoal](../android/health/connect/datatypes/ExercisePerformanceGoal.PowerGoal.md) | An [ExercisePerformanceGoal](ExercisePerformanceGoal.md) that requires a target power range to be met during the associated [PlannedExerciseStep](PlannedExerciseStep.md). | | [ExercisePerformanceGoal.RateOfPerceivedExertionGoal](../android/health/connect/datatypes/ExercisePerformanceGoal.RateOfPerceivedExertionGoal.md) | An [ExercisePerformanceGoal](ExercisePerformanceGoal.md) that requires a target RPE (rate of perceived exertion) to be met during the associated [PlannedExerciseStep](PlannedExerciseStep.md). | | [ExercisePerformanceGoal.SpeedGoal](../android/health/connect/datatypes/ExercisePerformanceGoal.SpeedGoal.md) | An [ExercisePerformanceGoal](ExercisePerformanceGoal.md) that requires a target speed range to be met during the associated [PlannedExerciseStep](PlannedExerciseStep.md). | | [ExercisePerformanceGoal.UnknownGoal](../android/health/connect/datatypes/ExercisePerformanceGoal.UnknownGoal.md) | An [ExercisePerformanceGoal](ExercisePerformanceGoal.md) that is unknown. | | [ExercisePerformanceGoal.WeightGoal](../android/health/connect/datatypes/ExercisePerformanceGoal.WeightGoal.md) | An [ExercisePerformanceGoal](ExercisePerformanceGoal.md) that requires a target weight to be lifted during the associated [PlannedExerciseStep](PlannedExerciseStep.md). | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A goal which should be aimed for during a [PlannedExerciseStep](PlannedExerciseStep.md).

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [AmrapGoal](../android/health/connect/datatypes/ExercisePerformanceGoal.AmrapGoal.md) An [ExercisePerformanceGoal](ExercisePerformanceGoal.md) that requires completing as many repetitions as possible. |
| | [CadenceGoal](../android/health/connect/datatypes/ExercisePerformanceGoal.CadenceGoal.md) An [ExercisePerformanceGoal](ExercisePerformanceGoal.md) that requires a target cadence range to be met during the associated [PlannedExerciseStep](PlannedExerciseStep.md). |
| | [HeartRateGoal](../android/health/connect/datatypes/ExercisePerformanceGoal.HeartRateGoal.md) An [ExercisePerformanceGoal](ExercisePerformanceGoal.md) that requires a target heart rate range, in BPM, to be met during the associated [PlannedExerciseStep](PlannedExerciseStep.md). |
| --- | --- |
| | [PowerGoal](../android/health/connect/datatypes/ExercisePerformanceGoal.PowerGoal.md) An [ExercisePerformanceGoal](ExercisePerformanceGoal.md) that requires a target power range to be met during the associated [PlannedExerciseStep](PlannedExerciseStep.md). |
| | [RateOfPerceivedExertionGoal](../android/health/connect/datatypes/ExercisePerformanceGoal.RateOfPerceivedExertionGoal.md) An [ExercisePerformanceGoal](ExercisePerformanceGoal.md) that requires a target RPE (rate of perceived exertion) to be met during the associated [PlannedExerciseStep](PlannedExerciseStep.md). |
| | [SpeedGoal](../android/health/connect/datatypes/ExercisePerformanceGoal.SpeedGoal.md) An [ExercisePerformanceGoal](ExercisePerformanceGoal.md) that requires a target speed range to be met during the associated [PlannedExerciseStep](PlannedExerciseStep.md). |
| --- | --- |
| | [UnknownGoal](../android/health/connect/datatypes/ExercisePerformanceGoal.UnknownGoal.md) An [ExercisePerformanceGoal](ExercisePerformanceGoal.md) that is unknown. |
| | [WeightGoal](../android/health/connect/datatypes/ExercisePerformanceGoal.WeightGoal.md) An [ExercisePerformanceGoal](ExercisePerformanceGoal.md) that requires a target weight to be lifted during the associated [PlannedExerciseStep](PlannedExerciseStep.md). |
