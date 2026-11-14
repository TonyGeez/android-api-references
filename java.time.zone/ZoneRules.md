Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ZoneRules

```
class ZoneRules : Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.time.zone.ZoneRules](https://developer.android.com/reference/kotlin/java/time/zone/ZoneRules#) |

The rules defining how the zone offset varies for a single time-zone.

The rules model all the historic and future transitions for a time-zone. `https://developer.android.com/reference/kotlin/java/time/zone/ZoneOffsetTransition` is used for known transitions, typically historic. `https://developer.android.com/reference/kotlin/java/time/zone/ZoneOffsetTransitionRule` is used for future transitions that are based on the result of an algorithm.

The same rules may be shared internally between multiple zone IDs.

Serializing an instance of `ZoneRules` will store the entire set of rules. It does not store the zone ID as it is not part of the state of this object.

A rule implementation may or may not store full information about historic and future transitions, and the information stored is only as accurate as that supplied to the implementation by the rules provider. Applications should treat the data provided as representing the best information available to the implementation of this rule.

## Summary

| Public methods ||
|---|---|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/time/zone/ZoneRules#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Checks if this set of rules equals another. |
| [Duration](https://developer.android.com/reference/kotlin/java/time/Duration.html#)! | `https://developer.android.com/reference/kotlin/java/time/zone/ZoneRules#getDaylightSavings(java.time.Instant)(instant: https://developer.android.com/reference/kotlin/java/time/Instant.html#!)` Gets the amount of daylight savings in use for the specified instant in this zone. |
| [ZoneOffset](https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#)! | `https://developer.android.com/reference/kotlin/java/time/zone/ZoneRules#getOffset(java.time.Instant)(instant: https://developer.android.com/reference/kotlin/java/time/Instant.html#!)` Gets the offset applicable at the specified instant in these rules. |
| [ZoneOffset](https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#)! | `https://developer.android.com/reference/kotlin/java/time/zone/ZoneRules#getOffset(java.time.LocalDateTime)(localDateTime: https://developer.android.com/reference/kotlin/java/time/LocalDateTime.html#!)` Gets a suitable offset for the specified local date-time in these rules. |
| [ZoneOffset](https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#)! | `https://developer.android.com/reference/kotlin/java/time/zone/ZoneRules#getStandardOffset(java.time.Instant)(instant: https://developer.android.com/reference/kotlin/java/time/Instant.html#!)` Gets the standard offset for the specified instant in this zone. |
| [ZoneOffsetTransition](https://developer.android.com/reference/kotlin/java/time/zone/ZoneOffsetTransition)! | `https://developer.android.com/reference/kotlin/java/time/zone/ZoneRules#getTransition(java.time.LocalDateTime)(localDateTime: https://developer.android.com/reference/kotlin/java/time/LocalDateTime.html#!)` Gets the offset transition applicable at the specified local date-time in these rules. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ZoneOffsetTransitionRule](https://developer.android.com/reference/kotlin/java/time/zone/ZoneOffsetTransitionRule)!\>! | `https://developer.android.com/reference/kotlin/java/time/zone/ZoneRules#getTransitionRules()()` Gets the list of transition rules for years beyond those defined in the transition list. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ZoneOffsetTransition](https://developer.android.com/reference/kotlin/java/time/zone/ZoneOffsetTransition)!\>! | `https://developer.android.com/reference/kotlin/java/time/zone/ZoneRules#getTransitions()()` Gets the complete list of fully defined transitions. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ZoneOffset](https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#)!\>! | `https://developer.android.com/reference/kotlin/java/time/zone/ZoneRules#getValidOffsets(java.time.LocalDateTime)(localDateTime: https://developer.android.com/reference/kotlin/java/time/LocalDateTime.html#!)` Gets the offset applicable at the specified local date-time in these rules. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/time/zone/ZoneRules#hashCode()()` Returns a suitable hash code given the definition of `equals`. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/time/zone/ZoneRules#isDaylightSavings(java.time.Instant)(instant: https://developer.android.com/reference/kotlin/java/time/Instant.html#!)` Checks if the specified instant is in daylight savings. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/time/zone/ZoneRules#isFixedOffset()()` Checks of the zone rules are fixed, such that the offset never varies. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/time/zone/ZoneRules#isValidOffset(java.time.LocalDateTime,%20java.time.ZoneOffset)(localDateTime: https://developer.android.com/reference/kotlin/java/time/LocalDateTime.html#!, offset: https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#!)` Checks if the offset date-time is valid for these rules. |
| [ZoneOffsetTransition](https://developer.android.com/reference/kotlin/java/time/zone/ZoneOffsetTransition)! | `https://developer.android.com/reference/kotlin/java/time/zone/ZoneRules#nextTransition(java.time.Instant)(instant: https://developer.android.com/reference/kotlin/java/time/Instant.html#!)` Gets the next transition after the specified instant. |
| static [ZoneRules](https://developer.android.com/reference/kotlin/java/time/zone/ZoneRules#)! | `https://developer.android.com/reference/kotlin/java/time/zone/ZoneRules#of(java.time.ZoneOffset)(offset: https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#!)` Obtains an instance of ZoneRules that has fixed zone rules. |
| static [ZoneRules](https://developer.android.com/reference/kotlin/java/time/zone/ZoneRules#)! | `https://developer.android.com/reference/kotlin/java/time/zone/ZoneRules#of(java.time.ZoneOffset,%20java.time.ZoneOffset,%20kotlin.collections.MutableList,%20kotlin.collections.MutableList,%20kotlin.collections.MutableList)(baseStandardOffset: https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#!, baseWallOffset: https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#!, standardOffsetTransitionList: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/java/time/zone/ZoneOffsetTransition!>!, transitionList: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/java/time/zone/ZoneOffsetTransition!>!, lastRules: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/java/time/zone/ZoneOffsetTransitionRule!>!)` Obtains an instance of a ZoneRules. |
| [ZoneOffsetTransition](https://developer.android.com/reference/kotlin/java/time/zone/ZoneOffsetTransition)! | `https://developer.android.com/reference/kotlin/java/time/zone/ZoneRules#previousTransition(java.time.Instant)(instant: https://developer.android.com/reference/kotlin/java/time/Instant.html#!)` Gets the previous transition before the specified instant. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/time/zone/ZoneRules#toString()()` Returns a string describing this object. |

## Public methods

### equals

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

Checks if this set of rules equals another.

Two rule sets are equal if they will always result in the same output for any given input instant or local date-time. Rules from two different groups may return false even if they are in fact the same.

This definition should result in implementations comparing their entire state.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |
| `otherRules` | the other rules, null returns false |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this rules is the same as that specified |

### getDaylightSavings

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDaylightSavings(instant: Instant!): Duration!
```

Gets the amount of daylight savings in use for the specified instant in this zone.

This provides access to historic information on how the amount of daylight savings has changed over time. This is the difference between the standard offset and the actual offset. Typically the amount is zero during winter and one hour during summer. Time-zones are second-based, so the nanosecond part of the duration will be zero.

This default implementation calculates the duration from the `https://developer.android.com/reference/kotlin/java/time/zone/ZoneRules#getOffset(java.time.Instant)` and `https://developer.android.com/reference/kotlin/java/time/zone/ZoneRules#getStandardOffset(java.time.Instant)` offsets.

| Parameters ||
|---|---|
| `instant` | [Instant](https://developer.android.com/reference/kotlin/java/time/Instant.html#)!: the instant to find the daylight savings for, not null, but null may be ignored if the rules have a single offset for all instants |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/Duration.html#!` | the difference between the standard and actual offset, not null |

### getOffset

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getOffset(instant: Instant!): ZoneOffset!
```

Gets the offset applicable at the specified instant in these rules.

The mapping from an instant to an offset is simple, there is only one valid offset for each instant. This method returns that offset.

| Parameters ||
|---|---|
| `instant` | [Instant](https://developer.android.com/reference/kotlin/java/time/Instant.html#)!: the instant to find the offset for, not null, but null may be ignored if the rules have a single offset for all instants |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#!` | the offset, not null |

### getOffset

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getOffset(localDateTime: LocalDateTime!): ZoneOffset!
```

Gets a suitable offset for the specified local date-time in these rules.

The mapping from a local date-time to an offset is not straightforward. There are three cases:

- Normal, with one valid offset. For the vast majority of the year, the normal case applies, where there is a single valid offset for the local date-time.
- Gap, with zero valid offsets. This is when clocks jump forward typically due to the spring daylight savings change from "winter" to "summer". In a gap there are local date-time values with no valid offset.
- Overlap, with two valid offsets. This is when clocks are set back typically due to the autumn daylight savings change from "summer" to "winter". In an overlap there are local date-time values with two valid offsets.

Thus, for any given local date-time there can be zero, one or two valid offsets. This method returns the single offset in the Normal case, and in the Gap or Overlap case it returns the offset before the transition.

Since, in the case of Gap and Overlap, the offset returned is a "best" value, rather than the "correct" value, it should be treated with care. Applications that care about the correct offset should use a combination of this method, `https://developer.android.com/reference/kotlin/java/time/zone/ZoneRules#getValidOffsets(java.time.LocalDateTime)` and `https://developer.android.com/reference/kotlin/java/time/zone/ZoneRules#getTransition(java.time.LocalDateTime)`.

| Parameters ||
|---|---|
| `localDateTime` | [LocalDateTime](https://developer.android.com/reference/kotlin/java/time/LocalDateTime.html#)!: the local date-time to query, not null, but null may be ignored if the rules have a single offset for all instants |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#!` | the best available offset for the local date-time, not null |

### getStandardOffset

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getStandardOffset(instant: Instant!): ZoneOffset!
```

Gets the standard offset for the specified instant in this zone.

This provides access to historic information on how the standard offset has changed over time. The standard offset is the offset before any daylight saving time is applied. This is typically the offset applicable during winter.

| Parameters ||
|---|---|
| `instant` | [Instant](https://developer.android.com/reference/kotlin/java/time/Instant.html#)!: the instant to find the offset information for, not null, but null may be ignored if the rules have a single offset for all instants |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#!` | the standard offset, not null |

### getTransition

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTransition(localDateTime: LocalDateTime!): ZoneOffsetTransition!
```

Gets the offset transition applicable at the specified local date-time in these rules.

The mapping from a local date-time to an offset is not straightforward. There are three cases:

- Normal, with one valid offset. For the vast majority of the year, the normal case applies, where there is a single valid offset for the local date-time.
- Gap, with zero valid offsets. This is when clocks jump forward typically due to the spring daylight savings change from "winter" to "summer". In a gap there are local date-time values with no valid offset.
- Overlap, with two valid offsets. This is when clocks are set back typically due to the autumn daylight savings change from "summer" to "winter". In an overlap there are local date-time values with two valid offsets.

A transition is used to model the cases of a Gap or Overlap. The Normal case will return null.

There are various ways to handle the conversion from a `LocalDateTime`. One technique, using this method, would be:

```kotlin
ZoneOffsetTransition trans = rules.getTransition(localDT);
   if (trans != null) {
     // Gap or Overlap: determine what to do from transition
   } else {
     // Normal case: only one valid offset
     zoneOffset = rule.getOffset(localDT);
   }
  
```

| Parameters ||
|---|---|
| `localDateTime` | [LocalDateTime](https://developer.android.com/reference/kotlin/java/time/LocalDateTime.html#)!: the local date-time to query for offset transition, not null, but null may be ignored if the rules have a single offset for all instants |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/zone/ZoneOffsetTransition!` | the offset transition, null if the local date-time is not in transition |

### getTransitionRules

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTransitionRules(): MutableList<ZoneOffsetTransitionRule!>!
```

Gets the list of transition rules for years beyond those defined in the transition list.

The complete set of transitions for this rules instance is defined by this method and `https://developer.android.com/reference/kotlin/java/time/zone/ZoneRules#getTransitions()`. This method returns instances of `https://developer.android.com/reference/kotlin/java/time/zone/ZoneOffsetTransitionRule` that define an algorithm for when transitions will occur.

For any given `ZoneRules`, this list contains the transition rules for years beyond those years that have been fully defined. These rules typically refer to future daylight saving time rule changes.

If the zone defines daylight savings into the future, then the list will normally be of size two and hold information about entering and exiting daylight savings. If the zone does not have daylight savings, or information about future changes is uncertain, then the list will be empty.

The list will be empty for fixed offset rules and for any time-zone where there is no daylight saving time. The list will also be empty if the transition rules are unknown.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/java/time/zone/ZoneOffsetTransitionRule!>!` | an immutable list of transition rules, not null |

### getTransitions

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTransitions(): MutableList<ZoneOffsetTransition!>!
```

Gets the complete list of fully defined transitions.

The complete set of transitions for this rules instance is defined by this method and `https://developer.android.com/reference/kotlin/java/time/zone/ZoneRules#getTransitionRules()`. This method returns those transitions that have been fully defined. These are typically historical, but may be in the future.

The list will be empty for fixed offset rules and for any time-zone where there has only ever been a single offset. The list will also be empty if the transition rules are unknown.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/java/time/zone/ZoneOffsetTransition!>!` | an immutable list of fully defined transitions, not null |

### getValidOffsets

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getValidOffsets(localDateTime: LocalDateTime!): MutableList<ZoneOffset!>!
```

Gets the offset applicable at the specified local date-time in these rules.

The mapping from a local date-time to an offset is not straightforward. There are three cases:

- Normal, with one valid offset. For the vast majority of the year, the normal case applies, where there is a single valid offset for the local date-time.
- Gap, with zero valid offsets. This is when clocks jump forward typically due to the spring daylight savings change from "winter" to "summer". In a gap there are local date-time values with no valid offset.
- Overlap, with two valid offsets. This is when clocks are set back typically due to the autumn daylight savings change from "summer" to "winter". In an overlap there are local date-time values with two valid offsets.

Thus, for any given local date-time there can be zero, one or two valid offsets. This method returns that list of valid offsets, which is a list of size 0, 1 or 2. In the case where there are two offsets, the earlier offset is returned at index 0 and the later offset at index 1.

There are various ways to handle the conversion from a `LocalDateTime`. One technique, using this method, would be:

```kotlin
List<ZoneOffset> validOffsets = rules.getValidOffsets(localDT);
   if (validOffsets.size() == 1) {
     // Normal case: only one valid offset
     zoneOffset = validOffsets.get(0);
   } else {
     // Gap or Overlap: determine what to do from transition (which will be non-null)
     ZoneOffsetTransition trans = rules.getTransition(localDT);
   }
  
```

In theory, it is possible for there to be more than two valid offsets. This would happen if clocks to be put back more than once in quick succession. This has never happened in the history of time-zones and thus has no special handling. However, if it were to happen, then the list would return more than 2 entries.

| Parameters ||
|---|---|
| `localDateTime` | [LocalDateTime](https://developer.android.com/reference/kotlin/java/time/LocalDateTime.html#)!: the local date-time to query for valid offsets, not null, but null may be ignored if the rules have a single offset for all instants |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#!>!` | the list of valid offsets, may be immutable, not null |

### hashCode

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

Returns a suitable hash code given the definition of `equals`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the hash code |

### isDaylightSavings

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isDaylightSavings(instant: Instant!): Boolean
```

Checks if the specified instant is in daylight savings.

This checks if the standard offset and the actual offset are the same for the specified instant. If they are not, it is assumed that daylight savings is in operation.

This default implementation compares the `https://developer.android.com/reference/kotlin/java/time/zone/ZoneRules#getOffset(java.time.Instant)` and `https://developer.android.com/reference/kotlin/java/time/zone/ZoneRules#getStandardOffset(java.time.Instant)` offsets.

| Parameters ||
|---|---|
| `instant` | [Instant](https://developer.android.com/reference/kotlin/java/time/Instant.html#)!: the instant to check the daylight savings for, not null, but null may be ignored if the rules have a single offset for all instants |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the specified instant is in daylight savings, false otherwise. |

### isFixedOffset

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isFixedOffset(): Boolean
```

Checks of the zone rules are fixed, such that the offset never varies.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the time-zone is fixed and the offset never changes |

### isValidOffset

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isValidOffset(
    localDateTime: LocalDateTime!, 
    offset: ZoneOffset!
): Boolean
```

Checks if the offset date-time is valid for these rules.

To be valid, the local date-time must not be in a gap and the offset must match one of the valid offsets.

This default implementation checks if `https://developer.android.com/reference/kotlin/java/time/zone/ZoneRules#getValidOffsets(java.time.LocalDateTime)` contains the specified offset.

| Parameters ||
|---|---|
| `localDateTime` | [LocalDateTime](https://developer.android.com/reference/kotlin/java/time/LocalDateTime.html#)!: the date-time to check, not null, but null may be ignored if the rules have a single offset for all instants |
| `offset` | [ZoneOffset](https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#)!: the offset to check, null returns false |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the offset date-time is valid for these rules |

### nextTransition

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun nextTransition(instant: Instant!): ZoneOffsetTransition!
```

Gets the next transition after the specified instant.

This returns details of the next transition after the specified instant. For example, if the instant represents a point where "Summer" daylight savings time applies, then the method will return the transition to the next "Winter" time.

| Parameters ||
|---|---|
| `instant` | [Instant](https://developer.android.com/reference/kotlin/java/time/Instant.html#)!: the instant to get the next transition after, not null, but null may be ignored if the rules have a single offset for all instants |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/zone/ZoneOffsetTransition!` | the next transition after the specified instant, null if this is after the last transition |

### of

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun of(offset: ZoneOffset!): ZoneRules!
```

Obtains an instance of ZoneRules that has fixed zone rules.

| Parameters ||
|---|---|
| `offset` | [ZoneOffset](https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#)!: the offset this fixed zone rules is based on, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/zone/ZoneRules#!` | the zone rules, not null |

**See Also**

- `https://developer.android.com/reference/kotlin/java/time/zone/ZoneRules#isFixedOffset()`

### of

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun of(
    baseStandardOffset: ZoneOffset!, 
    baseWallOffset: ZoneOffset!, 
    standardOffsetTransitionList: MutableList<ZoneOffsetTransition!>!, 
    transitionList: MutableList<ZoneOffsetTransition!>!, 
    lastRules: MutableList<ZoneOffsetTransitionRule!>!
): ZoneRules!
```

Obtains an instance of a ZoneRules.

| Parameters ||
|---|---|
| `baseStandardOffset` | [ZoneOffset](https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#)!: the standard offset to use before legal rules were set, not null |
| `baseWallOffset` | [ZoneOffset](https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#)!: the wall offset to use before legal rules were set, not null |
| `standardOffsetTransitionList` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ZoneOffsetTransition](https://developer.android.com/reference/kotlin/java/time/zone/ZoneOffsetTransition)!\>!: the list of changes to the standard offset, not null |
| `transitionList` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ZoneOffsetTransition](https://developer.android.com/reference/kotlin/java/time/zone/ZoneOffsetTransition)!\>!: the list of transitions, not null |
| `lastRules` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ZoneOffsetTransitionRule](https://developer.android.com/reference/kotlin/java/time/zone/ZoneOffsetTransitionRule)!\>!: the recurring last rules, size 16 or less, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/zone/ZoneRules#!` | the zone rules, not null |

### previousTransition

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun previousTransition(instant: Instant!): ZoneOffsetTransition!
```

Gets the previous transition before the specified instant.

This returns details of the previous transition before the specified instant. For example, if the instant represents a point where "summer" daylight saving time applies, then the method will return the transition from the previous "winter" time.

| Parameters ||
|---|---|
| `instant` | [Instant](https://developer.android.com/reference/kotlin/java/time/Instant.html#)!: the instant to get the previous transition after, not null, but null may be ignored if the rules have a single offset for all instants |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/zone/ZoneOffsetTransition!` | the previous transition before the specified instant, null if this is before the first transition |

### toString

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string describing this object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string for debugging, not null |
