Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 13](https://developer.android.com/sdkExtensions)

# PlannedExerciseSessionRecord

```
class PlannedExerciseSessionRecord : IntervalRecord
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [android.health.connect.datatypes.Record](../android/health/connect/datatypes/Record.md) |||
| | ↳ | [android.health.connect.datatypes.IntervalRecord](../android/health/connect/datatypes/IntervalRecord.md) ||
| | | ↳ | [android.health.connect.datatypes.PlannedExerciseSessionRecord](../android/health/connect/datatypes/PlannedExerciseSessionRecord.md) |
| --- | --- | --- | --- |

Captures a planned exercise session, also commonly referred to as a training plan.

Each record contains a start time, end time, an exercise type and a list of `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/PlannedExerciseBlock` which describe the details of the planned session. The start and end times may be in the future.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/PlannedExerciseSessionRecord.Builder` Builder class for `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/PlannedExerciseSessionRecord#`. |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_INSTANT:kotlin.Int` The record represents an instantaneous event. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_INTERVAL:kotlin.Int` The record represents an event over an interval. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_LOCAL_DATE:kotlin.Int` The record represents an event that occurred on a specific date. <br /> | ||

| Public methods ||
|---|---|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/PlannedExerciseSessionRecord#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [PlannedExerciseBlock](../android/health/connect/datatypes/PlannedExerciseBlock.md)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/PlannedExerciseSessionRecord#getBlocks()()` Returns the exercise blocks for this step. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/PlannedExerciseSessionRecord#getCompletedExerciseSessionId()()` Returns the id of exercise session that completed this planned session. |
| --- | --- |
| [Duration](../java/time/Duration.md) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/PlannedExerciseSessionRecord#getDuration()()` Returns the expected duration of the planned session. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/PlannedExerciseSessionRecord#getExerciseType()()` Returns the exercise type of this planned session. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/PlannedExerciseSessionRecord#getNotes()()` Returns notes for this planned session. |
| --- | --- |
| [LocalDate](../java/time/LocalDate.md) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/PlannedExerciseSessionRecord#getStartDate()()` Returns the start date of the planned session. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/PlannedExerciseSessionRecord#getTitle()()` Returns title of this planned session. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/PlannedExerciseSessionRecord#hasExplicitTime()()` Returns whether this planned session has an explicit time. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/PlannedExerciseSessionRecord#hashCode()()` Returns a hash code value for the object. |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/IntervalRecord` |---|---| | `https://developer.android.com/reference/kotlin/java/time/Instant.html#` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/IntervalRecord#getEndTime()()` <br /> | | `https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/IntervalRecord#getEndZoneOffset()()` <br /> | | `https://developer.android.com/reference/kotlin/java/time/Instant.html#` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/IntervalRecord#getStartTime()()` <br /> | | `https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/IntervalRecord#getStartZoneOffset()()` <br /> | ||
| From class `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record` |---|---| | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Metadata` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#getMetadata()()` <br /> | ||

## Public methods

### equals

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |
| `object` | the reference object with which to compare. This value may be `null`. |
| `o` | This value may be `null`. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj |

### getBlocks

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 13](https://developer.android.com/sdkExtensions)

```
fun getBlocks(): MutableList<PlannedExerciseBlock!>
```

Returns the exercise blocks for this step.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/health/connect/datatypes/PlannedExerciseBlock!>` | An unmodifiable list of `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/PlannedExerciseBlock`. This value cannot be `null`. |

### getCompletedExerciseSessionId

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 13](https://developer.android.com/sdkExtensions)

```
fun getCompletedExerciseSessionId(): String?
```

Returns the id of exercise session that completed this planned session. Returns null if none exists.

### getDuration

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 13](https://developer.android.com/sdkExtensions)

```
fun getDuration(): Duration
```

Returns the expected duration of the planned session.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/Duration.html#` | This value cannot be `null`. |

### getExerciseType

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 13](https://developer.android.com/sdkExtensions)

```
fun getExerciseType(): Int
```

Returns the exercise type of this planned session.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_BADMINTON:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_BASEBALL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_BASKETBALL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_BIKING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_BIKING_STATIONARY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_BOOT_CAMP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_BOXING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_CALISTHENICS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_CRICKET:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_DANCING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_ELLIPTICAL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_EXERCISE_CLASS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_FENCING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_FOOTBALL_AMERICAN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_FOOTBALL_AUSTRALIAN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_FRISBEE_DISC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_GOLF:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_GUIDED_BREATHING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_GYMNASTICS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_HANDBALL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_HIGH_INTENSITY_INTERVAL_TRAINING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_HIKING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_ICE_HOCKEY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_ICE_SKATING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_MARTIAL_ARTS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_PADDLING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_PARAGLIDING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_PILATES:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_RACQUETBALL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_ROCK_CLIMBING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_ROLLER_HOCKEY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_ROWING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_ROWING_MACHINE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_RUGBY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_RUNNING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_RUNNING_TREADMILL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_SAILING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_SCUBA_DIVING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_SKATING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_SKIING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_SNOWBOARDING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_SNOWSHOEING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_SOCCER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_SOFTBALL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_SQUASH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_STAIR_CLIMBING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_STAIR_CLIMBING_MACHINE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_STRENGTH_TRAINING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_STRETCHING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_SURFING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_SWIMMING_OPEN_WATER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_SWIMMING_POOL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_TABLE_TENNIS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_TENNIS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_VOLLEYBALL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_WALKING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_WATER_POLO:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_WEIGHTLIFTING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_WHEELCHAIR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_OTHER_WORKOUT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_YOGA:kotlin.Int` |

### getNotes

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 13](https://developer.android.com/sdkExtensions)

```
fun getNotes(): CharSequence?
```

Returns notes for this planned session. Returns null if it doesn't have notes.

### getStartDate

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 13](https://developer.android.com/sdkExtensions)

```
fun getStartDate(): LocalDate
```

Returns the start date of the planned session.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalDate.html#` | This value cannot be `null`. |

### getTitle

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 13](https://developer.android.com/sdkExtensions)

```
fun getTitle(): CharSequence?
```

Returns title of this planned session. Returns null if it doesn't have a title.

### hasExplicitTime

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 13](https://developer.android.com/sdkExtensions)

```
fun hasExplicitTime(): Boolean
```

Returns whether this planned session has an explicit time. If only a date was provided this will be false.

### hashCode

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

Returns a hash code value for the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |
