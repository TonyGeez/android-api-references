# ExerciseCompletionGoal

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 13](https://developer.android.com/sdkExtensions)

# ExerciseCompletionGoal

Kotlin| [Java](ExerciseCompletionGoal.md) 
| --- | --- |

```
abstract class ExerciseCompletionGoal
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.health.connect.datatypes.ExerciseCompletionGoal](ExerciseCompletionGoal.md) |

| Known Direct Subclasses [ExerciseCompletionGoal.ActiveCaloriesBurnedGoal](../android/health/connect/datatypes/ExerciseCompletionGoal.ActiveCaloriesBurnedGoal.md), [ExerciseCompletionGoal.DistanceGoal](../android/health/connect/datatypes/ExerciseCompletionGoal.DistanceGoal.md), [ExerciseCompletionGoal.DistanceWithVariableRestGoal](../android/health/connect/datatypes/ExerciseCompletionGoal.DistanceWithVariableRestGoal.md), [ExerciseCompletionGoal.DurationGoal](../android/health/connect/datatypes/ExerciseCompletionGoal.DurationGoal.md), [ExerciseCompletionGoal.RepetitionsGoal](../android/health/connect/datatypes/ExerciseCompletionGoal.RepetitionsGoal.md), [ExerciseCompletionGoal.StepsGoal](../android/health/connect/datatypes/ExerciseCompletionGoal.StepsGoal.md), [ExerciseCompletionGoal.TotalCaloriesBurnedGoal](../android/health/connect/datatypes/ExerciseCompletionGoal.TotalCaloriesBurnedGoal.md), [ExerciseCompletionGoal.UnknownGoal](../android/health/connect/datatypes/ExerciseCompletionGoal.UnknownGoal.md), [ExerciseCompletionGoal.UnspecifiedGoal](../android/health/connect/datatypes/ExerciseCompletionGoal.UnspecifiedGoal.md) |--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ExerciseCompletionGoal.ActiveCaloriesBurnedGoal](../android/health/connect/datatypes/ExerciseCompletionGoal.ActiveCaloriesBurnedGoal.md) | An [ExerciseCompletionGoal](ExerciseCompletionGoal.md) that requires a specified number of active calories to be burned. | | [ExerciseCompletionGoal.DistanceGoal](../android/health/connect/datatypes/ExerciseCompletionGoal.DistanceGoal.md) | An [ExerciseCompletionGoal](ExerciseCompletionGoal.md) that requires covering a specified distance. | | [ExerciseCompletionGoal.DistanceWithVariableRestGoal](../android/health/connect/datatypes/ExerciseCompletionGoal.DistanceWithVariableRestGoal.md) | An [ExerciseCompletionGoal](ExerciseCompletionGoal.md) that requires covering a specified distance. | | [ExerciseCompletionGoal.DurationGoal](../android/health/connect/datatypes/ExerciseCompletionGoal.DurationGoal.md) | An [ExerciseCompletionGoal](ExerciseCompletionGoal.md) that requires a specified duration to elapse. | | [ExerciseCompletionGoal.RepetitionsGoal](../android/health/connect/datatypes/ExerciseCompletionGoal.RepetitionsGoal.md) | An [ExerciseCompletionGoal](ExerciseCompletionGoal.md) that requires a specified number of repetitions to be completed. | | [ExerciseCompletionGoal.StepsGoal](../android/health/connect/datatypes/ExerciseCompletionGoal.StepsGoal.md) | An [ExerciseCompletionGoal](ExerciseCompletionGoal.md) that requires completing a specified number of steps. | | [ExerciseCompletionGoal.TotalCaloriesBurnedGoal](../android/health/connect/datatypes/ExerciseCompletionGoal.TotalCaloriesBurnedGoal.md) | An [ExerciseCompletionGoal](ExerciseCompletionGoal.md) that requires a specified number of total calories to be burned. | | [ExerciseCompletionGoal.UnknownGoal](../android/health/connect/datatypes/ExerciseCompletionGoal.UnknownGoal.md) | An [ExerciseCompletionGoal](ExerciseCompletionGoal.md) that is unknown. | | [ExerciseCompletionGoal.UnspecifiedGoal](../android/health/connect/datatypes/ExerciseCompletionGoal.UnspecifiedGoal.md) | An [ExerciseCompletionGoal](ExerciseCompletionGoal.md) that has no specific target metric. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A goal which should be met to complete a [PlannedExerciseStep](PlannedExerciseStep.md).

## Summary

| Nested classes ||
|---|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [ActiveCaloriesBurnedGoal](../android/health/connect/datatypes/ExerciseCompletionGoal.ActiveCaloriesBurnedGoal.md) An [ExerciseCompletionGoal](ExerciseCompletionGoal.md) that requires a specified number of active calories to be burned. |
| | [DistanceGoal](../android/health/connect/datatypes/ExerciseCompletionGoal.DistanceGoal.md) An [ExerciseCompletionGoal](ExerciseCompletionGoal.md) that requires covering a specified distance. |
| | [DistanceWithVariableRestGoal](../android/health/connect/datatypes/ExerciseCompletionGoal.DistanceWithVariableRestGoal.md) An [ExerciseCompletionGoal](ExerciseCompletionGoal.md) that requires covering a specified distance. |
| --- | --- |
| | [DurationGoal](../android/health/connect/datatypes/ExerciseCompletionGoal.DurationGoal.md) An [ExerciseCompletionGoal](ExerciseCompletionGoal.md) that requires a specified duration to elapse. |
| | [RepetitionsGoal](../android/health/connect/datatypes/ExerciseCompletionGoal.RepetitionsGoal.md) An [ExerciseCompletionGoal](ExerciseCompletionGoal.md) that requires a specified number of repetitions to be completed. |
| | [StepsGoal](../android/health/connect/datatypes/ExerciseCompletionGoal.StepsGoal.md) An [ExerciseCompletionGoal](ExerciseCompletionGoal.md) that requires completing a specified number of steps. |
| --- | --- |
| | [TotalCaloriesBurnedGoal](../android/health/connect/datatypes/ExerciseCompletionGoal.TotalCaloriesBurnedGoal.md) An [ExerciseCompletionGoal](ExerciseCompletionGoal.md) that requires a specified number of total calories to be burned. |
| | [UnknownGoal](../android/health/connect/datatypes/ExerciseCompletionGoal.UnknownGoal.md) An [ExerciseCompletionGoal](ExerciseCompletionGoal.md) that is unknown. |
| | [UnspecifiedGoal](../android/health/connect/datatypes/ExerciseCompletionGoal.UnspecifiedGoal.md) An [ExerciseCompletionGoal](ExerciseCompletionGoal.md) that has no specific target metric. |
| --- | --- |
