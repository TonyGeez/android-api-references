Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

# ExerciseSessionRecord

```
class ExerciseSessionRecord : IntervalRecord
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [android.health.connect.datatypes.Record](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record) |||
| | ↳ | [android.health.connect.datatypes.IntervalRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/IntervalRecord) ||
| | | ↳ | [android.health.connect.datatypes.ExerciseSessionRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionRecord#) |
| --- | --- | --- | --- |

Captures exercise or a sequence of exercises. This can be a playing game like football or a sequence of fitness exercises.

Each record needs a start time, end time and session type. In addition, each record has two optional independent lists of time intervals: `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegment` represents particular exercise within session, `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseLap` represents a lap time within session.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionRecord.Builder` Builder class for `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionRecord#` |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_INSTANT:kotlin.Int` The record represents an instantaneous event. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_INTERVAL:kotlin.Int` The record represents an event over an interval. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_LOCAL_DATE:kotlin.Int` The record represents an event that occurred on a specific date. <br /> | ||

| Public methods ||
|---|---|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionRecord#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionRecord#getExerciseType()()` Returns exerciseType of this session. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ExerciseLap](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseLap)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionRecord#getLaps()()` Returns laps of this session. |
| --- | --- |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionRecord#getNotes()()` Returns notes for this activity. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionRecord#getPlannedExerciseSessionId()()` Returns the ID of the `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/PlannedExerciseSessionRecord` that this session was based upon. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionRecord#getRateOfPerceivedExertion()()` Gets the rate of perceived exertion (RPE) for this exercise session. |
| --- | --- |
| [ExerciseRoute](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseRoute)? | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionRecord#getRoute()()` Returns route of this session. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ExerciseSegment](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegment)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionRecord#getSegments()()` Returns segments of this session. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionRecord#getTitle()()` Returns title of this session. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionRecord#hasRateOfPerceivedExertion()()` Returns true if this session has an associated rate of perceived exertion. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionRecord#hasRoute()()` Returns if this session has recorded route. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionRecord#hashCode()()` Returns a hash code value for the object. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/IntervalRecord` |---|---| | `https://developer.android.com/reference/kotlin/java/time/Instant.html#` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/IntervalRecord#getEndTime()()` <br /> | | `https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/IntervalRecord#getEndZoneOffset()()` <br /> | | `https://developer.android.com/reference/kotlin/java/time/Instant.html#` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/IntervalRecord#getStartTime()()` <br /> | | `https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/IntervalRecord#getStartZoneOffset()()` <br /> | ||
| From class `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record` |---|---| | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Metadata` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#getMetadata()()` <br /> | ||

| Properties ||
|---|---|
| static [AggregationType](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType)\< [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionRecord#EXERCISE_DURATION_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to retrieve total exercise session duration using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`. |

## Public methods

### equals

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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

### getExerciseType

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getExerciseType(): Int
```

Returns exerciseType of this session.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_BADMINTON:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_BASEBALL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_BASKETBALL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_BIKING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_BIKING_STATIONARY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_BOOT_CAMP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_BOXING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_CALISTHENICS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_CRICKET:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_DANCING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_ELLIPTICAL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_EXERCISE_CLASS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_FENCING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_FOOTBALL_AMERICAN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_FOOTBALL_AUSTRALIAN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_FRISBEE_DISC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_GOLF:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_GUIDED_BREATHING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_GYMNASTICS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_HANDBALL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_HIGH_INTENSITY_INTERVAL_TRAINING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_HIKING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_ICE_HOCKEY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_ICE_SKATING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_MARTIAL_ARTS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_PADDLING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_PARAGLIDING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_PILATES:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_RACQUETBALL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_ROCK_CLIMBING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_ROLLER_HOCKEY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_ROWING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_ROWING_MACHINE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_RUGBY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_RUNNING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_RUNNING_TREADMILL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_SAILING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_SCUBA_DIVING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_SKATING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_SKIING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_SNOWBOARDING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_SNOWSHOEING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_SOCCER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_SOFTBALL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_SQUASH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_STAIR_CLIMBING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_STAIR_CLIMBING_MACHINE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_STRENGTH_TRAINING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_STRETCHING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_SURFING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_SWIMMING_OPEN_WATER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_SWIMMING_POOL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_TABLE_TENNIS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_TENNIS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_VOLLEYBALL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_WALKING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_WATER_POLO:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_WEIGHTLIFTING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_WHEELCHAIR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_OTHER_WORKOUT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionType#EXERCISE_SESSION_TYPE_YOGA:kotlin.Int` |

### getLaps

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getLaps(): MutableList<ExerciseLap!>
```

Returns laps of this session. Returns empty list if the session doesn't have exercise laps.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseLap!>` | This value cannot be `null`. |

### getNotes

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getNotes(): CharSequence?
```

Returns notes for this activity. Returns null if the session doesn't have notes.

### getPlannedExerciseSessionId

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 13](https://developer.android.com/sdkExtensions)

```
fun getPlannedExerciseSessionId(): String?
```

Returns the ID of the `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/PlannedExerciseSessionRecord` that this session was based upon. If not set, returns null.

### getRateOfPerceivedExertion

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 19](https://developer.android.com/sdkExtensions)

```
fun getRateOfPerceivedExertion(): Float
```

Gets the rate of perceived exertion (RPE) for this exercise session.

Values correspond to the Borg CR10 RPE scale and must be in the range 0 to 10 inclusive. 0: No exertion (at rest) 1: Very light 2-3: Light 4-5: Moderate 6-7: Hard 8-9: Very hard 10: Maximum effort

Use `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSessionRecord#hasRateOfPerceivedExertion()` to check whether RPE exists for this session.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | Value is between 0.0f and 10.0f inclusive |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if rate of perceived exertion is not set. |

### getRoute

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getRoute(): ExerciseRoute?
```

Returns route of this session. Returns null if the session doesn't have route.

### getSegments

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getSegments(): MutableList<ExerciseSegment!>
```

Returns segments of this session. Returns empty list if the session doesn't have exercise segments.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/health/connect/datatypes/ExerciseSegment!>` | This value cannot be `null`. |

### getTitle

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getTitle(): CharSequence?
```

Returns title of this session. Returns null if the session doesn't have title.

### hasRateOfPerceivedExertion

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 19](https://developer.android.com/sdkExtensions)

```
fun hasRateOfPerceivedExertion(): Boolean
```

Returns true if this session has an associated rate of perceived exertion.

### hasRoute

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
fun hasRoute(): Boolean
```

Returns if this session has recorded route.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | This value cannot be `null`. |

### hashCode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

Returns a hash code value for the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

## Properties

### EXERCISE_DURATION_TOTAL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 7](https://developer.android.com/sdkExtensions)

```
static val EXERCISE_DURATION_TOTAL: AggregationType<Long!>
```

Metric identifier to retrieve total exercise session duration using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`. Calculated in milliseconds.
