# PlannedExerciseStep

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 13](https://developer.android.com/sdkExtensions)

# PlannedExerciseStep

Kotlin| [Java](https://developer.android.com/reference/android/health/connect/datatypes/PlannedExerciseStep "View this page in Java") 
| --- | --- |

```
class PlannedExerciseStep
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.health.connect.datatypes.PlannedExerciseStep](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/PlannedExerciseStep#) |

A single step within an [PlannedExerciseBlock](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/PlannedExerciseBlock) e.g. 8x 60kg barbell squats.

## Summary

| Nested classes ||
|---|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/PlannedExerciseStep.Builder) Builder of [PlannedExerciseStep](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/PlannedExerciseStep#). |

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EXERCISE_CATEGORY_ACTIVE](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/PlannedExerciseStep#EXERCISE_CATEGORY_ACTIVE:kotlin.Int) Active exercise. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EXERCISE_CATEGORY_COOLDOWN](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/PlannedExerciseStep#EXERCISE_CATEGORY_COOLDOWN:kotlin.Int) Cooldown exercise, typically at the end of a workout. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EXERCISE_CATEGORY_RECOVERY](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/PlannedExerciseStep#EXERCISE_CATEGORY_RECOVERY:kotlin.Int) Lower intensity, active exercise. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EXERCISE_CATEGORY_REST](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/PlannedExerciseStep#EXERCISE_CATEGORY_REST:kotlin.Int) A rest. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EXERCISE_CATEGORY_UNKNOWN](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/PlannedExerciseStep#EXERCISE_CATEGORY_UNKNOWN:kotlin.Int) An unknown category of exercise. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EXERCISE_CATEGORY_WARMUP](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/PlannedExerciseStep#EXERCISE_CATEGORY_WARMUP:kotlin.Int) A warmup. |
| --- | --- |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/PlannedExerciseStep#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [ExerciseCompletionGoal](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseCompletionGoal) | [getCompletionGoal](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/PlannedExerciseStep#getCompletionGoal())`()` Returns the exercise completion goal for this step. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getDescription](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/PlannedExerciseStep#getDescription())`()` Returns the description of this step. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getExerciseCategory](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/PlannedExerciseStep#getExerciseCategory())`()` Returns the exercise category of this step. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getExerciseType](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/PlannedExerciseStep#getExerciseType())`()` Returns the exercise type of this step. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ExercisePerformanceGoal](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExercisePerformanceGoal)!\> | [getPerformanceGoals](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/PlannedExerciseStep#getPerformanceGoals())`()` Returns the exercise performance goals for this step. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/PlannedExerciseStep#hashCode())`()` <br /> |

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
| [ExerciseCompletionGoal](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseCompletionGoal) | This value cannot be`null`. |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.health.connect.datatypes.PlannedExerciseStep#EXERCISE_CATEGORY_UNKNOWN](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/PlannedExerciseStep#EXERCISE_CATEGORY_UNKNOWN:kotlin.Int), [android.health.connect.datatypes.PlannedExerciseStep#EXERCISE_CATEGORY_WARMUP](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/PlannedExerciseStep#EXERCISE_CATEGORY_WARMUP:kotlin.Int), [android.health.connect.datatypes.PlannedExerciseStep#EXERCISE_CATEGORY_REST](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/PlannedExerciseStep#EXERCISE_CATEGORY_REST:kotlin.Int), [android.health.connect.datatypes.PlannedExerciseStep#EXERCISE_CATEGORY_ACTIVE](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/PlannedExerciseStep#EXERCISE_CATEGORY_ACTIVE:kotlin.Int), [android.health.connect.datatypes.PlannedExerciseStep#EXERCISE_CATEGORY_COOLDOWN](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/PlannedExerciseStep#EXERCISE_CATEGORY_COOLDOWN:kotlin.Int), or [android.health.connect.datatypes.PlannedExerciseStep#EXERCISE_CATEGORY_RECOVERY](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/PlannedExerciseStep#EXERCISE_CATEGORY_RECOVERY:kotlin.Int) |

### getExerciseType

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 13](https://developer.android.com/sdkExtensions) 

```
fun getExerciseType(): Int
```

Returns the exercise type of this step.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_UNKNOWN](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_UNKNOWN:kotlin.Int), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_BARBELL_SHOULDER_PRESS](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_BARBELL_SHOULDER_PRESS:kotlin.Int), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_BENCH_SIT_UP](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_BENCH_SIT_UP:kotlin.Int), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_BIKING](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_BIKING:kotlin.Int), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_BIKING_STATIONARY](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_BIKING_STATIONARY:kotlin.Int), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_DUMBBELL_CURL_LEFT_ARM](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_DUMBBELL_CURL_LEFT_ARM:kotlin.Int), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_DUMBBELL_CURL_RIGHT_ARM](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_DUMBBELL_CURL_RIGHT_ARM:kotlin.Int), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_DUMBBELL_FRONT_RAISE](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_DUMBBELL_FRONT_RAISE:kotlin.Int), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_DUMBBELL_LATERAL_RAISE](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_DUMBBELL_LATERAL_RAISE:kotlin.Int), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_DUMBBELL_TRICEPS_EXTENSION_LEFT_ARM](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_DUMBBELL_TRICEPS_EXTENSION_LEFT_ARM:kotlin.Int), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_DUMBBELL_TRICEPS_EXTENSION_RIGHT_ARM](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_DUMBBELL_TRICEPS_EXTENSION_RIGHT_ARM:kotlin.Int), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_DUMBBELL_TRICEPS_EXTENSION_TWO_ARM](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_DUMBBELL_TRICEPS_EXTENSION_TWO_ARM:kotlin.Int), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_FORWARD_TWIST](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_FORWARD_TWIST:kotlin.Int), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_ELLIPTICAL](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_ELLIPTICAL:kotlin.Int), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_HIGH_INTENSITY_INTERVAL_TRAINING](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_HIGH_INTENSITY_INTERVAL_TRAINING:kotlin.Int), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_PILATES](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_PILATES:kotlin.Int), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_ROWING_MACHINE](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_ROWING_MACHINE:kotlin.Int), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_RUNNING](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_RUNNING:kotlin.Int), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_RUNNING_TREADMILL](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_RUNNING_TREADMILL:kotlin.Int), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_STAIR_CLIMBING](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_STAIR_CLIMBING:kotlin.Int), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_STAIR_CLIMBING_MACHINE](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_STAIR_CLIMBING_MACHINE:kotlin.Int), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_STRETCHING](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_STRETCHING:kotlin.Int), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_SWIMMING_OPEN_WATER](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_SWIMMING_OPEN_WATER:kotlin.Int), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_SWIMMING_POOL](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_SWIMMING_POOL:kotlin.Int), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_UPPER_TWIST](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_UPPER_TWIST:kotlin.Int), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_WALKING](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_WALKING:kotlin.Int), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_WEIGHTLIFTING](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_WEIGHTLIFTING:kotlin.Int), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_WHEELCHAIR](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_WHEELCHAIR:kotlin.Int), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_OTHER_WORKOUT](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_OTHER_WORKOUT:kotlin.Int), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_YOGA](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_YOGA:kotlin.Int), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_ARM_CURL](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_ARM_CURL:kotlin.Int), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_BACK_EXTENSION](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_BACK_EXTENSION:kotlin.Int), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_BALL_SLAM](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_BALL_SLAM:kotlin.Int), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_BENCH_PRESS](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_BENCH_PRESS:kotlin.Int), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_BURPEE](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_BURPEE:kotlin.Int), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_CRUNCH](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_CRUNCH:kotlin.Int), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_DEADLIFT](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_DEADLIFT:kotlin.Int), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_DOUBLE_ARM_TRICEPS_EXTENSION](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_DOUBLE_ARM_TRICEPS_EXTENSION:kotlin.Int), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_DUMBBELL_ROW](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_DUMBBELL_ROW:kotlin.Int), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_FRONT_RAISE](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_FRONT_RAISE:kotlin.Int), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_HIP_THRUST](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_HIP_THRUST:kotlin.Int), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_HULA_HOOP](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_HULA_HOOP:kotlin.Int), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_JUMPING_JACK](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_JUMPING_JACK:kotlin.Int), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_JUMP_ROPE](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_JUMP_ROPE:kotlin.Int), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_KETTLEBELL_SWING](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_KETTLEBELL_SWING:kotlin.Int), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_LATERAL_RAISE](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_LATERAL_RAISE:kotlin.Int), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_LAT_PULL_DOWN](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_LAT_PULL_DOWN:kotlin.Int), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_LEG_CURL](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_LEG_CURL:kotlin.Int), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_LEG_EXTENSION](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_LEG_EXTENSION:kotlin.Int), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_LEG_PRESS](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_LEG_PRESS:kotlin.Int), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_LEG_RAISE](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_LEG_RAISE:kotlin.Int), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_LUNGE](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_LUNGE:kotlin.Int), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_MOUNTAIN_CLIMBER](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_MOUNTAIN_CLIMBER:kotlin.Int), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_PLANK](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_PLANK:kotlin.Int), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_PULL_UP](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_PULL_UP:kotlin.Int), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_PUNCH](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_PUNCH:kotlin.Int), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_SHOULDER_PRESS](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_SHOULDER_PRESS:kotlin.Int), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_SINGLE_ARM_TRICEPS_EXTENSION](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_SINGLE_ARM_TRICEPS_EXTENSION:kotlin.Int), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_SIT_UP](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_SIT_UP:kotlin.Int), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_SQUAT](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_SQUAT:kotlin.Int), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_SWIMMING_FREESTYLE](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_SWIMMING_FREESTYLE:kotlin.Int), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_SWIMMING_BACKSTROKE](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_SWIMMING_BACKSTROKE:kotlin.Int), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_SWIMMING_BREASTSTROKE](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_SWIMMING_BREASTSTROKE:kotlin.Int), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_SWIMMING_BUTTERFLY](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_SWIMMING_BUTTERFLY:kotlin.Int), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_SWIMMING_MIXED](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_SWIMMING_MIXED:kotlin.Int), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_SWIMMING_OTHER](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_SWIMMING_OTHER:kotlin.Int), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_REST](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_REST:kotlin.Int), or [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_PAUSE](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_PAUSE:kotlin.Int) |

### getPerformanceGoals

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 13](https://developer.android.com/sdkExtensions) 

```
fun getPerformanceGoals(): MutableList<ExercisePerformanceGoal!>
```

Returns the exercise performance goals for this step.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [ExercisePerformanceGoal](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExercisePerformanceGoal)!> | An unmodifiable list of [ExercisePerformanceGoal](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExercisePerformanceGoal). This value cannot be`null`. |

### hashCode

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |
