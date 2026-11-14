# PlannedExerciseStep

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 13](https://developer.android.com/sdkExtensions)

# PlannedExerciseStep

Kotlin| [Java](../android/health/connect/datatypes/PlannedExerciseStep.md) 
| --- | --- |

```
class PlannedExerciseStep
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.health.connect.datatypes.PlannedExerciseStep](../android/health/connect/datatypes/PlannedExerciseStep.md) |

A single step within an [PlannedExerciseBlock](../android/health/connect/datatypes/PlannedExerciseBlock.md) e.g. 8x 60kg barbell squats.

## Summary

| Nested classes ||
|---|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/health/connect/datatypes/PlannedExerciseStep.Builder.md) Builder of [PlannedExerciseStep](../android/health/connect/datatypes/PlannedExerciseStep.md). |

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EXERCISE_CATEGORY_ACTIVE](../android/health/connect/datatypes/PlannedExerciseStep.md) Active exercise. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EXERCISE_CATEGORY_COOLDOWN](../android/health/connect/datatypes/PlannedExerciseStep.md) Cooldown exercise, typically at the end of a workout. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EXERCISE_CATEGORY_RECOVERY](../android/health/connect/datatypes/PlannedExerciseStep.md) Lower intensity, active exercise. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EXERCISE_CATEGORY_REST](../android/health/connect/datatypes/PlannedExerciseStep.md) A rest. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EXERCISE_CATEGORY_UNKNOWN](../android/health/connect/datatypes/PlannedExerciseStep.md) An unknown category of exercise. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EXERCISE_CATEGORY_WARMUP](../android/health/connect/datatypes/PlannedExerciseStep.md) A warmup. |
| --- | --- |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/health/connect/datatypes/PlannedExerciseStep.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [ExerciseCompletionGoal](../android/health/connect/datatypes/ExerciseCompletionGoal.md) | [getCompletionGoal](../android/health/connect/datatypes/PlannedExerciseStep.md))`()` Returns the exercise completion goal for this step. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getDescription](../android/health/connect/datatypes/PlannedExerciseStep.md))`()` Returns the description of this step. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getExerciseCategory](../android/health/connect/datatypes/PlannedExerciseStep.md))`()` Returns the exercise category of this step. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getExerciseType](../android/health/connect/datatypes/PlannedExerciseStep.md))`()` Returns the exercise type of this step. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ExercisePerformanceGoal](../android/health/connect/datatypes/ExercisePerformanceGoal.md)!\> | [getPerformanceGoals](../android/health/connect/datatypes/PlannedExerciseStep.md))`()` Returns the exercise performance goals for this step. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/health/connect/datatypes/PlannedExerciseStep.md))`()` <br /> |

## Constants

### EXERCISE_CATEGORY_ACTIVE

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 13](https://developer.android.com/sdkExtensions) 

```
static val EXERCISE_CATEGORY_ACTIVE: Int
```

Active exercise. 

 Value: 3

### EXERCISE_CATEGORY_COOLDOWN

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 13](https://developer.android.com/sdkExtensions) 

```
static val EXERCISE_CATEGORY_COOLDOWN: Int
```

Cooldown exercise, typically at the end of a workout. 

 Value: 4

### EXERCISE_CATEGORY_RECOVERY

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 13](https://developer.android.com/sdkExtensions) 

```
static val EXERCISE_CATEGORY_RECOVERY: Int
```

Lower intensity, active exercise. 

 Value: 5

### EXERCISE_CATEGORY_REST

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 13](https://developer.android.com/sdkExtensions) 

```
static val EXERCISE_CATEGORY_REST: Int
```

A rest. 

 Value: 2

### EXERCISE_CATEGORY_UNKNOWN

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 13](https://developer.android.com/sdkExtensions) 

```
static val EXERCISE_CATEGORY_UNKNOWN: Int
```

An unknown category of exercise. 

 Value: 0

### EXERCISE_CATEGORY_WARMUP

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 13](https://developer.android.com/sdkExtensions) 

```
static val EXERCISE_CATEGORY_WARMUP: Int
```

A warmup. 

 Value: 1

## Public methods

### equals

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The`equals`method implements an equivalence relation on non-null object references:

- It is*reflexive* : for any non-null reference value`x`,`x.equals(x)`should return`true`.
- It is*symmetric* : for any non-null reference values`x`and`y`,`x.equals(y)`should return`true`if and only if`y.equals(x)`returns`true`.
- It is*transitive* : for any non-null reference values`x`,`y`, and`z`, if`x.equals(y)`returns`true`and`y.equals(z)`returns`true`, then`x.equals(z)`should return`true`.
- It is*consistent* : for any non-null reference values`x`and`y`, multiple invocations of`x.equals(y)`consistently return`true`or consistently return`false`, provided no information used in`equals`comparisons on the objects is modified.
- For any non-null reference value`x`,`x.equals(null)`should return`false`.

An equivalence relation partitions the elements it operates on into*equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |
| `o` | This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getCompletionGoal

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 13](https://developer.android.com/sdkExtensions) 

```
fun getCompletionGoal(): ExerciseCompletionGoal
```

Returns the exercise completion goal for this step.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [ExerciseCompletionGoal](../android/health/connect/datatypes/ExerciseCompletionGoal.md) | This value cannot be`null`. |

### getDescription

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 13](https://developer.android.com/sdkExtensions) 

```
fun getDescription(): CharSequence?
```

Returns the description of this step.

| Return ||
|------------------------------------------------------------------------------------------------|--------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | This value may be`null`. |

### getExerciseCategory

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 13](https://developer.android.com/sdkExtensions) 

```
fun getExerciseCategory(): Int
```

Returns the exercise category of this step.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.health.connect.datatypes.PlannedExerciseStep#EXERCISE_CATEGORY_UNKNOWN](../android/health/connect/datatypes/PlannedExerciseStep.md), [android.health.connect.datatypes.PlannedExerciseStep#EXERCISE_CATEGORY_WARMUP](../android/health/connect/datatypes/PlannedExerciseStep.md), [android.health.connect.datatypes.PlannedExerciseStep#EXERCISE_CATEGORY_REST](../android/health/connect/datatypes/PlannedExerciseStep.md), [android.health.connect.datatypes.PlannedExerciseStep#EXERCISE_CATEGORY_ACTIVE](../android/health/connect/datatypes/PlannedExerciseStep.md), [android.health.connect.datatypes.PlannedExerciseStep#EXERCISE_CATEGORY_COOLDOWN](../android/health/connect/datatypes/PlannedExerciseStep.md), or [android.health.connect.datatypes.PlannedExerciseStep#EXERCISE_CATEGORY_RECOVERY](../android/health/connect/datatypes/PlannedExerciseStep.md) |

### getExerciseType

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 13](https://developer.android.com/sdkExtensions) 

```
fun getExerciseType(): Int
```

Returns the exercise type of this step.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_UNKNOWN](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_BARBELL_SHOULDER_PRESS](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_BENCH_SIT_UP](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_BIKING](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_BIKING_STATIONARY](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_DUMBBELL_CURL_LEFT_ARM](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_DUMBBELL_CURL_RIGHT_ARM](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_DUMBBELL_FRONT_RAISE](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_DUMBBELL_LATERAL_RAISE](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_DUMBBELL_TRICEPS_EXTENSION_LEFT_ARM](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_DUMBBELL_TRICEPS_EXTENSION_RIGHT_ARM](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_DUMBBELL_TRICEPS_EXTENSION_TWO_ARM](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_FORWARD_TWIST](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_ELLIPTICAL](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_HIGH_INTENSITY_INTERVAL_TRAINING](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_PILATES](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_ROWING_MACHINE](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_RUNNING](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_RUNNING_TREADMILL](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_STAIR_CLIMBING](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_STAIR_CLIMBING_MACHINE](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_STRETCHING](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_SWIMMING_OPEN_WATER](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_SWIMMING_POOL](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_UPPER_TWIST](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_WALKING](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_WEIGHTLIFTING](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_WHEELCHAIR](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_OTHER_WORKOUT](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_YOGA](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_ARM_CURL](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_BACK_EXTENSION](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_BALL_SLAM](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_BENCH_PRESS](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_BURPEE](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_CRUNCH](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_DEADLIFT](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_DOUBLE_ARM_TRICEPS_EXTENSION](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_DUMBBELL_ROW](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_FRONT_RAISE](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_HIP_THRUST](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_HULA_HOOP](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_JUMPING_JACK](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_JUMP_ROPE](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_KETTLEBELL_SWING](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_LATERAL_RAISE](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_LAT_PULL_DOWN](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_LEG_CURL](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_LEG_EXTENSION](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_LEG_PRESS](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_LEG_RAISE](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_LUNGE](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_MOUNTAIN_CLIMBER](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_PLANK](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_PULL_UP](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_PUNCH](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_SHOULDER_PRESS](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_SINGLE_ARM_TRICEPS_EXTENSION](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_SIT_UP](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_SQUAT](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_SWIMMING_FREESTYLE](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_SWIMMING_BACKSTROKE](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_SWIMMING_BREASTSTROKE](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_SWIMMING_BUTTERFLY](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_SWIMMING_MIXED](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_SWIMMING_OTHER](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_REST](../android/health/connect/datatypes/ExerciseSegmentType.md), or [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_PAUSE](../android/health/connect/datatypes/ExerciseSegmentType.md) |

### getPerformanceGoals

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 13](https://developer.android.com/sdkExtensions) 

```
fun getPerformanceGoals(): MutableList<ExercisePerformanceGoal!>
```

Returns the exercise performance goals for this step.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [ExercisePerformanceGoal](../android/health/connect/datatypes/ExercisePerformanceGoal.md)!> | An unmodifiable list of [ExercisePerformanceGoal](../android/health/connect/datatypes/ExercisePerformanceGoal.md). This value cannot be`null`. |

### hashCode

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |
