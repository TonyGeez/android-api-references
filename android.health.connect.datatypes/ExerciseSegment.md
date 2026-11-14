# ExerciseSegment

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ExerciseSegment

Kotlin| [Java](../android/health/connect/datatypes/ExerciseSegment.md) 
| --- | --- |

```
class ExerciseSegment
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.health.connect.datatypes.ExerciseSegment](../android/health/connect/datatypes/ExerciseSegment.md) |

Represents particular exercise within exercise session (see [ExerciseSessionRecord](../android/health/connect/datatypes/ExerciseSessionRecord.md)).

Each record contains start and end time of the exercise, exercise type and optional number of repetitions, weight, set index and rate of perceived exertion.

## Summary

| Nested classes ||
|---|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/health/connect/datatypes/ExerciseSegment.Builder.md) Builder class for [ExerciseSegment](../android/health/connect/datatypes/ExerciseSegment.md) |

| Public methods ||
|-----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/health/connect/datatypes/ExerciseSegment.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [Instant](../java/time/Instant.md) | [getEndTime](../android/health/connect/datatypes/ExerciseSegment.md))`()` <br /> |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getRateOfPerceivedExertion](../android/health/connect/datatypes/ExerciseSegment.md))`()` Gets the rate of perceived exertion (RPE) for this exercise segment. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRepetitionsCount](../android/health/connect/datatypes/ExerciseSegment.md))`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSegmentType](../android/health/connect/datatypes/ExerciseSegment.md))`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSetIndex](../android/health/connect/datatypes/ExerciseSegment.md))`()` Gets the set index for this exercise segment. |
| --- | --- |
| [Instant](../java/time/Instant.md) | [getStartTime](../android/health/connect/datatypes/ExerciseSegment.md))`()` <br /> |
| [Mass](../android/health/connect/datatypes/units/Mass.md)? | [getWeight](../android/health/connect/datatypes/ExerciseSegment.md))`()` Gets the weight associated with this exercise segment. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasRateOfPerceivedExertion](../android/health/connect/datatypes/ExerciseSegment.md))`()` Returns true if this segment has an associated rate of perceived exertion. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasSetIndex](../android/health/connect/datatypes/ExerciseSegment.md))`()` Returns true if this segment has an associated set index. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/health/connect/datatypes/ExerciseSegment.md))`()` <br /> |

## Public methods

### equals

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getEndTime

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getEndTime(): Instant
```

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------|
| [Instant](../java/time/Instant.md) | This value cannot be`null`. |

### getRateOfPerceivedExertion

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRateOfPerceivedExertion(): Float
```

Gets the rate of perceived exertion (RPE) for this exercise segment.

Values correspond to the Borg CR10 RPE scale and must be in the range 0 to 10 inclusive. 0: No exertion (at rest) 1: Very light 2-3: Light 4-5: Moderate 6-7: Hard 8-9: Very hard 10: Maximum effort

Use [hasRateOfPerceivedExertion](../android/health/connect/datatypes/ExerciseSegment.md))to check whether RPE exists for this segment.

| Return ||
|--------------------------------------------------------------------------------|-------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | Value is between 0.0f and 10.0f inclusive |

| Exceptions ||
|-----------------------------------|-------------------------------------------|
| `java.lang.IllegalStateException` | if rate of perceived exertion is not set. |

### getRepetitionsCount

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRepetitionsCount(): Int
```

| Return ||
|----------------------------------------------------------------------------|-----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is 0 or greater |

### getSegmentType

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSegmentType(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_UNKNOWN](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_BARBELL_SHOULDER_PRESS](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_BENCH_SIT_UP](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_BIKING](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_BIKING_STATIONARY](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_DUMBBELL_CURL_LEFT_ARM](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_DUMBBELL_CURL_RIGHT_ARM](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_DUMBBELL_FRONT_RAISE](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_DUMBBELL_LATERAL_RAISE](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_DUMBBELL_TRICEPS_EXTENSION_LEFT_ARM](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_DUMBBELL_TRICEPS_EXTENSION_RIGHT_ARM](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_DUMBBELL_TRICEPS_EXTENSION_TWO_ARM](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_FORWARD_TWIST](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_ELLIPTICAL](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_HIGH_INTENSITY_INTERVAL_TRAINING](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_PILATES](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_ROWING_MACHINE](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_RUNNING](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_RUNNING_TREADMILL](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_STAIR_CLIMBING](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_STAIR_CLIMBING_MACHINE](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_STRETCHING](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_SWIMMING_OPEN_WATER](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_SWIMMING_POOL](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_UPPER_TWIST](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_WALKING](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_WEIGHTLIFTING](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_WHEELCHAIR](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_OTHER_WORKOUT](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_YOGA](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_ARM_CURL](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_BACK_EXTENSION](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_BALL_SLAM](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_BENCH_PRESS](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_BURPEE](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_CRUNCH](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_DEADLIFT](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_DOUBLE_ARM_TRICEPS_EXTENSION](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_DUMBBELL_ROW](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_FRONT_RAISE](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_HIP_THRUST](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_HULA_HOOP](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_JUMPING_JACK](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_JUMP_ROPE](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_KETTLEBELL_SWING](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_LATERAL_RAISE](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_LAT_PULL_DOWN](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_LEG_CURL](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_LEG_EXTENSION](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_LEG_PRESS](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_LEG_RAISE](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_LUNGE](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_MOUNTAIN_CLIMBER](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_PLANK](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_PULL_UP](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_PUNCH](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_SHOULDER_PRESS](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_SINGLE_ARM_TRICEPS_EXTENSION](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_SIT_UP](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_SQUAT](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_SWIMMING_FREESTYLE](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_SWIMMING_BACKSTROKE](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_SWIMMING_BREASTSTROKE](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_SWIMMING_BUTTERFLY](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_SWIMMING_MIXED](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_SWIMMING_OTHER](../android/health/connect/datatypes/ExerciseSegmentType.md), [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_REST](../android/health/connect/datatypes/ExerciseSegmentType.md), or [android.health.connect.datatypes.ExerciseSegmentType#EXERCISE_SEGMENT_TYPE_PAUSE](../android/health/connect/datatypes/ExerciseSegmentType.md) |

### getSetIndex

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSetIndex(): Int
```

Gets the set index for this exercise segment.

The set index is a non-negative integer starting at zero.

A set is a group of consecutive repetitions (reps) of a specific exercise performed without a break, e.g. 10 push-ups in a row without stopping.

A set index represents the position of this set relative to other sets in the session. For instance, if an exercise has three sets, they will have setIndex values of 0, 1, and 2 respectively.

Multiple segments may be part of a single set, for example if a collection of activities are considered to be a single set, in which case those segments would have the same set index.

The set index is may also go back to zero in a single`ExerciseSession`. For example, if three sets of one activity are completed followed by three sets of another, setIndex values of 0, 1, 2, 0, 1, 2 would be expected for those segments.

Use [hasSetIndex](../android/health/connect/datatypes/ExerciseSegment.md))to check whether a set index exists for this segment. Multiple segments can share the same set index.

| Return ||
|----------------------------------------------------------------------------|-----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is 0 or greater |

| Exceptions ||
|-----------------------------------|--------------------------|
| `java.lang.IllegalStateException` | if set index is not set. |

### getStartTime

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getStartTime(): Instant
```

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------|
| [Instant](../java/time/Instant.md) | This value cannot be`null`. |

### getWeight

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getWeight(): Mass?
```

Gets the weight associated with this exercise segment.

Returns`null`if weight is not set. 

### hasRateOfPerceivedExertion

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasRateOfPerceivedExertion(): Boolean
```

Returns true if this segment has an associated rate of perceived exertion. 

### hasSetIndex

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasSetIndex(): Boolean
```

Returns true if this segment has an associated set index. 

### hashCode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |
