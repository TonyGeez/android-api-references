Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ZoneOffsetTransition

```
class ZoneOffsetTransition : Comparable<ZoneOffsetTransition!>, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.time.zone.ZoneOffsetTransition](ZoneOffsetTransition.md) |

A transition between two offsets caused by a discontinuity in the local time-line.

A transition between two offsets is normally the result of a daylight savings cutover. The discontinuity is normally a gap in spring and an overlap in autumn. `ZoneOffsetTransition` models the transition between the two offsets.

Gaps occur where there are local date-times that simply do not exist. An example would be when the offset changes from `+03:00` to `+04:00`. This might be described as 'the clocks will move forward one hour tonight at 1am'.

Overlaps occur where there are local date-times that exist twice. An example would be when the offset changes from `+04:00` to `+03:00`. This might be described as 'the clocks will move back one hour tonight at 2am'.

## Summary

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | compareTo Compares this transition to another based on the transition instant. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | equals Checks if this object equals another. |
| [LocalDateTime](../java.time/LocalDateTime.md)! | getDateTimeAfter Gets the local transition date-time, as would be expressed with the 'after' offset. |
| --- | --- |
| [LocalDateTime](../java.time/LocalDateTime.md)! | getDateTimeBefore Gets the local transition date-time, as would be expressed with the 'before' offset. |
| [Duration](../java.time/Duration.md)! | getDuration Gets the duration of the transition. |
| [Instant](../java.time/Instant.md)! | getInstant Gets the transition instant. |
| --- | --- |
| [ZoneOffset](../java.time/ZoneOffset.md)! | getOffsetAfter Gets the offset after the transition. |
| [ZoneOffset](../java.time/ZoneOffset.md)! | getOffsetBefore Gets the offset before the transition. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | hashCode Returns a suitable hash code. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isGap Does this transition represent a gap in the local time-line. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isOverlap Does this transition represent an overlap in the local time-line. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isValidOffset Checks if the specified offset is valid during this transition. |
| --- | --- |
| static [ZoneOffsetTransition](ZoneOffsetTransition.md)! | of Obtains an instance defining a transition between two offsets. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | toEpochSecond Gets the transition instant as an epoch second. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | toString Returns a string describing this object. |
| --- | --- |

## Public methods

### compareTo

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun compareTo(other: ZoneOffsetTransition!): Int
```

Compares this transition to another based on the transition instant.

This compares the instants of each transition. The offsets are ignored, making this order inconsistent with equals.

| Parameters ||
|---|---|
| `o` | the object to be compared. |
| `otherTransition` | the transition to compare to, not null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the comparator value, that is the comparison of this transition instant with `otherTransition` instant |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the specified object's type prevents it from being compared to this object. |
| `java.lang.NullPointerException` | if the specified object is null |

### equals

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

Checks if this object equals another.

The entire state of the object is compared.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |
| `other` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?: the other object to compare to, null returns false |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if equal |

### getDateTimeAfter

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDateTimeAfter(): LocalDateTime!
```

Gets the local transition date-time, as would be expressed with the 'after' offset.

This is the first date-time after the discontinuity, when the new offset applies.

The combination of the 'before' date-time and offset represents the same instant as the 'after' date-time and offset.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalDateTime.html#!` | the transition date-time expressed with the after offset, not null |

### getDateTimeBefore

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDateTimeBefore(): LocalDateTime!
```

Gets the local transition date-time, as would be expressed with the 'before' offset.

This is the date-time where the discontinuity begins expressed with the 'before' offset. At this instant, the 'after' offset is actually used, therefore the combination of this date-time and the 'before' offset will never occur.

The combination of the 'before' date-time and offset represents the same instant as the 'after' date-time and offset.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/LocalDateTime.html#!` | the transition date-time expressed with the before offset, not null |

### getDuration

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDuration(): Duration!
```

Gets the duration of the transition.

In most cases, the transition duration is one hour, however this is not always the case. The duration will be positive for a gap and negative for an overlap. Time-zones are second-based, so the nanosecond part of the duration will be zero.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/Duration.html#!` | the duration of the transition, positive for gaps, negative for overlaps |

### getInstant

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getInstant(): Instant!
```

Gets the transition instant.

This is the instant of the discontinuity, which is defined as the first instant that the 'after' offset applies.

The methods getInstant, getDateTimeBefore and getDateTimeAfter all represent the same instant.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/Instant.html#!` | the transition instant, not null |

### getOffsetAfter

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getOffsetAfter(): ZoneOffset!
```

Gets the offset after the transition.

This is the offset in use on and after the instant of the transition.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#!` | the offset after the transition, not null |

### getOffsetBefore

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getOffsetBefore(): ZoneOffset!
```

Gets the offset before the transition.

This is the offset in use before the instant of the transition.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#!` | the offset before the transition, not null |

### hashCode

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

Returns a suitable hash code.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the hash code |

### isGap

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isGap(): Boolean
```

Does this transition represent a gap in the local time-line.

Gaps occur where there are local date-times that simply do not exist. An example would be when the offset changes from `+01:00` to `+02:00`. This might be described as 'the clocks will move forward one hour tonight at 1am'.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this transition is a gap, false if it is an overlap |

### isOverlap

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isOverlap(): Boolean
```

Does this transition represent an overlap in the local time-line.

Overlaps occur where there are local date-times that exist twice. An example would be when the offset changes from `+02:00` to `+01:00`. This might be described as 'the clocks will move back one hour tonight at 2am'.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this transition is an overlap, false if it is a gap |

### isValidOffset

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isValidOffset(offset: ZoneOffset!): Boolean
```

Checks if the specified offset is valid during this transition.

This checks to see if the given offset will be valid at some point in the transition. A gap will always return false. An overlap will return true if the offset is either the before or after offset.

| Parameters ||
|---|---|
| `offset` | [ZoneOffset](../java.time/ZoneOffset.md)!: the offset to check, null returns false |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the offset is valid during the transition |

### of

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun of(
    transition: LocalDateTime!, 
    offsetBefore: ZoneOffset!, 
    offsetAfter: ZoneOffset!
): ZoneOffsetTransition!
```

Obtains an instance defining a transition between two offsets.

Applications should normally obtain an instance from ZoneRules. This factory is only intended for use when creating ZoneRules.

| Parameters ||
|---|---|
| `transition` | [LocalDateTime](../java.time/LocalDateTime.md)!: the transition date-time at the transition, which never actually occurs, expressed local to the before offset, not null |
| `offsetBefore` | [ZoneOffset](../java.time/ZoneOffset.md)!: the offset before the transition, not null |
| `offsetAfter` | [ZoneOffset](../java.time/ZoneOffset.md)!: the offset at and after the transition, not null |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/zone/ZoneOffsetTransition#!` | the transition, not null |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `offsetBefore` and `offsetAfter` are equal, or `transition.getNano()` returns non-zero value |

### toEpochSecond

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toEpochSecond(): Long
```

Gets the transition instant as an epoch second.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the transition epoch second |

### toString

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string describing this object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string for debugging, not null |
