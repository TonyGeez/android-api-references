Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 15](https://developer.android.com/sdkExtensions)

# MindfulnessSessionRecord

```
class MindfulnessSessionRecord : IntervalRecord
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| ↳ | [android.health.connect.datatypes.Record](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record) |||
| | ↳ | [android.health.connect.datatypes.IntervalRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/IntervalRecord) ||
| | | ↳ | [android.health.connect.datatypes.MindfulnessSessionRecord](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MindfulnessSessionRecord#) |

Captures a mindfulness session.

For example: yoga, meditation, guided breathing, etc.

Each record needs a start time, end time and a mindfulness session type. In addition, each record has an optional title and notes.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MindfulnessSessionRecord.Builder` Builder class for `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MindfulnessSessionRecord#` |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MindfulnessSessionRecord#MINDFULNESS_SESSION_TYPE_BREATHING:kotlin.Int` Guided breathing mindfulness session. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MindfulnessSessionRecord#MINDFULNESS_SESSION_TYPE_MEDITATION:kotlin.Int` Meditation mindfulness session. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MindfulnessSessionRecord#MINDFULNESS_SESSION_TYPE_MOVEMENT:kotlin.Int` Stretches/movement mindfulness session. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MindfulnessSessionRecord#MINDFULNESS_SESSION_TYPE_MUSIC:kotlin.Int` Music/soundscapes mindfulness session. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MindfulnessSessionRecord#MINDFULNESS_SESSION_TYPE_OTHER:kotlin.Int` Other mindfulness session. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MindfulnessSessionRecord#MINDFULNESS_SESSION_TYPE_UNGUIDED:kotlin.Int` Unguided mindfulness session. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MindfulnessSessionRecord#MINDFULNESS_SESSION_TYPE_UNKNOWN:kotlin.Int` Use this type if the mindfulness session type is unknown. |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_INSTANT:kotlin.Int` The record represents an instantaneous event. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_INTERVAL:kotlin.Int` The record represents an event over an interval. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#RECORD_TEMPORAL_TYPE_LOCAL_DATE:kotlin.Int` The record represents an event that occurred on a specific date. <br /> | ||

| Public methods ||
|---|---|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MindfulnessSessionRecord#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MindfulnessSessionRecord#getMindfulnessSessionType()()` Returns type of the mindfulness session. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MindfulnessSessionRecord#getNotes()()` Returns notes for the mindfulness session. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MindfulnessSessionRecord#getTitle()()` Returns title of the mindfulness session. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MindfulnessSessionRecord#hashCode()()` Returns a hash code value for the object. |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/IntervalRecord` |---|---| | `https://developer.android.com/reference/kotlin/java/time/Instant.html#` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/IntervalRecord#getEndTime()()` <br /> | | `https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/IntervalRecord#getEndZoneOffset()()` <br /> | | `https://developer.android.com/reference/kotlin/java/time/Instant.html#` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/IntervalRecord#getStartTime()()` <br /> | | `https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/IntervalRecord#getStartZoneOffset()()` <br /> | ||
| From class `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record` |---|---| | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Metadata` | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/Record#getMetadata()()` <br /> | ||

| Properties ||
|---|---|
| static [AggregationType](https://developer.android.com/reference/kotlin/android/health/connect/datatypes/AggregationType)\< [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)!\> | `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MindfulnessSessionRecord#MINDFULNESS_DURATION_TOTAL:android.health.connect.datatypes.AggregationType` Metric identifier to retrieve total mindfulness session duration using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`. |

## Constants

### MINDFULNESS_SESSION_TYPE_BREATHING

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 15](https://developer.android.com/sdkExtensions)

```
static val MINDFULNESS_SESSION_TYPE_BREATHING: Int
```

Guided breathing mindfulness session.

 Value: 3

### MINDFULNESS_SESSION_TYPE_MEDITATION

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 15](https://developer.android.com/sdkExtensions)

```
static val MINDFULNESS_SESSION_TYPE_MEDITATION: Int
```

Meditation mindfulness session.

 Value: 1

### MINDFULNESS_SESSION_TYPE_MOVEMENT

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 15](https://developer.android.com/sdkExtensions)

```
static val MINDFULNESS_SESSION_TYPE_MOVEMENT: Int
```

Stretches/movement mindfulness session.

 Value: 5

### MINDFULNESS_SESSION_TYPE_MUSIC

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 15](https://developer.android.com/sdkExtensions)

```
static val MINDFULNESS_SESSION_TYPE_MUSIC: Int
```

Music/soundscapes mindfulness session.

 Value: 4

### MINDFULNESS_SESSION_TYPE_OTHER

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 15](https://developer.android.com/sdkExtensions)

```
static val MINDFULNESS_SESSION_TYPE_OTHER: Int
```

Other mindfulness session.

 Value: 2

### MINDFULNESS_SESSION_TYPE_UNGUIDED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 15](https://developer.android.com/sdkExtensions)

```
static val MINDFULNESS_SESSION_TYPE_UNGUIDED: Int
```

Unguided mindfulness session.

 Value: 6

### MINDFULNESS_SESSION_TYPE_UNKNOWN

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 15](https://developer.android.com/sdkExtensions)

```
static val MINDFULNESS_SESSION_TYPE_UNKNOWN: Int
```

Use this type if the mindfulness session type is unknown.

 Value: 0

## Public methods

### equals

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |
| `object` | the reference object with which to compare. This value may be `null`. |
| `o` | This value may be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj |

### getMindfulnessSessionType

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 15](https://developer.android.com/sdkExtensions)

```
fun getMindfulnessSessionType(): Int
```

Returns type of the mindfulness session.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MindfulnessSessionRecord#MINDFULNESS_SESSION_TYPE_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MindfulnessSessionRecord#MINDFULNESS_SESSION_TYPE_MEDITATION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MindfulnessSessionRecord#MINDFULNESS_SESSION_TYPE_OTHER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MindfulnessSessionRecord#MINDFULNESS_SESSION_TYPE_BREATHING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MindfulnessSessionRecord#MINDFULNESS_SESSION_TYPE_MUSIC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MindfulnessSessionRecord#MINDFULNESS_SESSION_TYPE_MOVEMENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/health/connect/datatypes/MindfulnessSessionRecord#MINDFULNESS_SESSION_TYPE_UNGUIDED:kotlin.Int` |

### getNotes

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 15](https://developer.android.com/sdkExtensions)

```
fun getNotes(): CharSequence?
```

Returns notes for the mindfulness session. Returns null if no notes was specified.

### getTitle

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 15](https://developer.android.com/sdkExtensions)

```
fun getTitle(): CharSequence?
```

Returns title of the mindfulness session. Returns null if no title was specified.

### hashCode

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

Returns a hash code value for the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

## Properties

### MINDFULNESS_DURATION_TOTAL

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 15](https://developer.android.com/sdkExtensions)

```
static val MINDFULNESS_DURATION_TOTAL: AggregationType<Long!>
```

Metric identifier to retrieve total mindfulness session duration using aggregate APIs in `https://developer.android.com/reference/kotlin/android/health/connect/HealthConnectManager.html#`. Calculated in milliseconds.
