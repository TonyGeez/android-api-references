# PlannedExerciseStep

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 13](https://developer.android.com/sdkExtensions)

# PlannedExerciseStep

Kotlin| [Java](PlannedExerciseStep.md) 
| --- | --- |

```
class PlannedExerciseStep
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.health.connect.datatypes.PlannedExerciseStep](PlannedExerciseStep.md) |

A single step within an [PlannedExerciseBlock](PlannedExerciseBlock.md) e.g. 8x 60kg barbell squats.

## Summary

| Nested classes ||
|---|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/health/connect/datatypes/PlannedExerciseStep.Builder.md) Builder of [PlannedExerciseStep](PlannedExerciseStep.md). |

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EXERCISE_CATEGORY_ACTIVE](PlannedExerciseStep.md) Active exercise. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EXERCISE_CATEGORY_COOLDOWN](PlannedExerciseStep.md) Cooldown exercise, typically at the end of a workout. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EXERCISE_CATEGORY_RECOVERY](PlannedExerciseStep.md) Lower intensity, active exercise. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EXERCISE_CATEGORY_REST](PlannedExerciseStep.md) A rest. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EXERCISE_CATEGORY_UNKNOWN](PlannedExerciseStep.md) An unknown category of exercise. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EXERCISE_CATEGORY_WARMUP](PlannedExerciseStep.md) A warmup. |
| --- | --- |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](PlannedExerciseStep.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [ExerciseCompletionGoal](ExerciseCompletionGoal.md) | [getCompletionGoal](PlannedExerciseStep.md))`()` Returns the exercise completion goal for this step. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getDescription](PlannedExerciseStep.md))`()` Returns the description of this step. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getExerciseCategory](PlannedExerciseStep.md))`()` Returns the exercise category of this step. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getExerciseType](PlannedExerciseStep.md))`()` Returns the exercise type of this step. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ExercisePerformanceGoal](ExercisePerformanceGoal.md)!\> | [getPerformanceGoals](PlannedExerciseStep.md))`()` Returns the exercise performance goals for this step. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](PlannedExerciseStep.md))`()` <br /> |

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
| [ExerciseCompletionGoal](ExerciseCompletionGoal.md) | This value cannot be`null`. |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.health.connect.datatypes.PlannedExerciseStep#EXERCISE_CATEGORY_UNKNOWN](PlannedExerciseStep.md), [android.health.connect.datatypes.PlannedExerciseStep#EXERCISE_CATEGORY_WARMUP](PlannedExerciseStep.md), [android.health.connect.datatypes.PlannedExerciseStep#EXERCISE_CATEGORY_REST](PlannedExerciseStep.md), [android.health.connect.datatypes.PlannedExerciseStep#EXERCISE_CATEGORY_ACTIVE](PlannedExerciseStep.md), [android.health.connect.datatypes.PlannedExerciseStep#EXERCISE_CATEGORY_COOLDOWN](PlannedExerciseStep.md), or [android.health.connect.datatypes.PlannedExerciseStep#EXERCISE_CATEGORY_RECOVERY](PlannedExerciseStep.md) |

### getExerciseType

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 13](https://developer.android.com/sdkExtensions) 

```
fun getExerciseType(): Int
```

Returns the exercise type of this step.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_UNKNOWN](ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_BARBELL_SHOULDER_PRESS](ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_BENCH_SIT_UP](ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_BIKING](ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_BIKING_STATIONARY](ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_DUMBBELL_CURL_LEFT_ARM](ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_DUMBBELL_CURL_RIGHT_ARM](ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_DUMBBELL_FRONT_RAISE](ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_DUMBBELL_LATERAL_RAISE](ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_DUMBBELL_TRICEPS_EXTENSION_LEFT_ARM](ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_DUMBBELL_TRICEPS_EXTENSION_RIGHT_ARM](ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_DUMBBELL_TRICEPS_EXTENSION_TWO_ARM](ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_FORWARD_TWIST](ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_ELLIPTICAL](ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_HIGH_INTENSITY_INTERVAL_TRAINING](ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_PILATES](ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_ROWING_MACHINE](ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_RUNNING](ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_RUNNING_TREADMILL](ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_STAIR_CLIMBING](ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_STAIR_CLIMBING_MACHINE](ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_STRETCHING](ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_SWIMMING_OPEN_WATER](ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_SWIMMING_POOL](ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_UPPER_TWIST](ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_WALKING](ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_WEIGHTLIFTING](ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_WHEELCHAIR](ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_OTHER_WORKOUT](ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_YOGA](ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_ARM_CURL](ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_BACK_EXTENSION](ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_BALL_SLAM](ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_BENCH_PRESS](ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_BURPEE](ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_CRUNCH](ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_DEADLIFT](ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_DOUBLE_ARM_TRICEPS_EXTENSION](ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_DUMBBELL_ROW](ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_FRONT_RAISE](ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_HIP_THRUST](ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_HULA_HOOP](ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_JUMPING_JACK](ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_JUMP_ROPE](ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_KETTLEBELL_SWING](ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_LATERAL_RAISE](ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_LAT_PULL_DOWN](ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_LEG_CURL](ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_LEG_EXTENSION](ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_LEG_PRESS](ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_LEG_RAISE](ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_LUNGE](ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_MOUNTAIN_CLIMBER](ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_PLANK](ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_PULL_UP](ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_PUNCH](ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_SHOULDER_PRESS](ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_SINGLE_ARM_TRICEPS_EXTENSION](ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_SIT_UP](ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_SQUAT](ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_SWIMMING_FREESTYLE](ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_SWIMMING_BACKSTROKE](ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_SWIMMING_BREASTSTROKE](ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_SWIMMING_BUTTERFLY](ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_SWIMMING_MIXED](ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_SWIMMING_OTHER](ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_REST](ExerciseSegmentType.md), or [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_PAUSE](ExerciseSegmentType.md) |

### getPerformanceGoals

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 13](https://developer.android.com/sdkExtensions) 

```
fun getPerformanceGoals(): MutableList<ExercisePerformanceGoal!>
```

Returns the exercise performance goals for this step.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [ExercisePerformanceGoal](ExercisePerformanceGoal.md)!> | An unmodifiable list of [ExercisePerformanceGoal](ExercisePerformanceGoal.md). This value cannot be`null`. |

### hashCode

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |
