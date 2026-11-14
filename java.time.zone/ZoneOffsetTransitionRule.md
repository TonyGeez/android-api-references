# ZoneOffsetTransitionRule

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ZoneOffsetTransitionRule

```
class ZoneOffsetTransitionRule : Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.time.zone.ZoneOffsetTransitionRule](https://developer.android.com/reference/kotlin/java/time/zone/ZoneOffsetTransitionRule#) |

A rule expressing how to create a transition.

This class allows rules for identifying future transitions to be expressed. A rule might be written in many forms:

- the 16th March
- the Sunday on or after the 16th March
- the Sunday on or before the 16th March
- the last Sunday in February

These different rule types can be expressed and queried.

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [TimeDefinition](https://developer.android.com/reference/kotlin/java/time/zone/ZoneOffsetTransitionRule.TimeDefinition) A definition of the way a local time can be converted to the actual transition date-time. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ZoneOffsetTransition](https://developer.android.com/reference/kotlin/java/time/zone/ZoneOffsetTransition)! | [createTransition](https://developer.android.com/reference/kotlin/java/time/zone/ZoneOffsetTransitionRule#createTransition(kotlin.Int))`(`year:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a transition instance for the specified year. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/java/time/zone/ZoneOffsetTransitionRule#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Checks if this object equals another. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDayOfMonthIndicator](https://developer.android.com/reference/kotlin/java/time/zone/ZoneOffsetTransitionRule#getDayOfMonthIndicator())`()` Gets the indicator of the day-of-month of the transition. |
| --- | --- |
| [DayOfWeek](https://developer.android.com/reference/kotlin/java/time/DayOfWeek.html#)! | [getDayOfWeek](https://developer.android.com/reference/kotlin/java/time/zone/ZoneOffsetTransitionRule#getDayOfWeek())`()` Gets the day-of-week of the transition. |
| [LocalTime](https://developer.android.com/reference/kotlin/java/time/LocalTime.html#)! | [getLocalTime](https://developer.android.com/reference/kotlin/java/time/zone/ZoneOffsetTransitionRule#getLocalTime())`()` Gets the local time of day of the transition which must be checked with [isMidnightEndOfDay()](https://developer.android.com/reference/kotlin/java/time/zone/ZoneOffsetTransitionRule#isMidnightEndOfDay()). |
| [Month](https://developer.android.com/reference/kotlin/java/time/Month.html#)! | [getMonth](https://developer.android.com/reference/kotlin/java/time/zone/ZoneOffsetTransitionRule#getMonth())`()` Gets the month of the transition. |
| --- | --- |
| [ZoneOffset](https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#)! | [getOffsetAfter](https://developer.android.com/reference/kotlin/java/time/zone/ZoneOffsetTransitionRule#getOffsetAfter())`()` Gets the offset after the transition. |
| [ZoneOffset](https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#)! | [getOffsetBefore](https://developer.android.com/reference/kotlin/java/time/zone/ZoneOffsetTransitionRule#getOffsetBefore())`()` Gets the offset before the transition. |
| [ZoneOffset](https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#)! | [getStandardOffset](https://developer.android.com/reference/kotlin/java/time/zone/ZoneOffsetTransitionRule#getStandardOffset())`()` Gets the standard offset in force at the transition. |
| --- | --- |
| [ZoneOffsetTransitionRule.TimeDefinition](https://developer.android.com/reference/kotlin/java/time/zone/ZoneOffsetTransitionRule.TimeDefinition)! | [getTimeDefinition](https://developer.android.com/reference/kotlin/java/time/zone/ZoneOffsetTransitionRule#getTimeDefinition())`()` Gets the time definition, specifying how to convert the time to an instant. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/java/time/zone/ZoneOffsetTransitionRule#hashCode())`()` Returns a suitable hash code. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isMidnightEndOfDay](https://developer.android.com/reference/kotlin/java/time/zone/ZoneOffsetTransitionRule#isMidnightEndOfDay())`()` Is the transition local time midnight at the end of day. |
| --- | --- |
| static [ZoneOffsetTransitionRule](https://developer.android.com/reference/kotlin/java/time/zone/ZoneOffsetTransitionRule#)! | [of](https://developer.android.com/reference/kotlin/java/time/zone/ZoneOffsetTransitionRule#of(java.time.Month,%20kotlin.Int,%20java.time.DayOfWeek,%20java.time.LocalTime,%20kotlin.Boolean,%20java.time.zone.ZoneOffsetTransitionRule.TimeDefinition,%20java.time.ZoneOffset,%20java.time.ZoneOffset,%20java.time.ZoneOffset))`(`month:` ` [Month](https://developer.android.com/reference/kotlin/java/time/Month.html#)!`, `dayOfMonthIndicator:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dayOfWeek:` ` [DayOfWeek](https://developer.android.com/reference/kotlin/java/time/DayOfWeek.html#)!`, `time:` ` [LocalTime](https://developer.android.com/reference/kotlin/java/time/LocalTime.html#)!`, `timeEndOfDay:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `timeDefinition:` ` [ZoneOffsetTransitionRule.TimeDefinition](https://developer.android.com/reference/kotlin/java/time/zone/ZoneOffsetTransitionRule.TimeDefinition)!`, `standardOffset:` ` [ZoneOffset](https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#)!`, `offsetBefore:` ` [ZoneOffset](https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#)!`, `offsetAfter:` ` [ZoneOffset](https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#)!`)` Obtains an instance defining the yearly rule to create transitions between two offsets. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/time/zone/ZoneOffsetTransitionRule#toString())`()` Returns a string describing this object. |

## Public methods

### createTransition

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun createTransition(year: Int): ZoneOffsetTransition!
```

Creates a transition instance for the specified year.

Calculations are performed using the ISO-8601 chronology.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------|
| `year` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the year to create a transition for, not null |

| Return ||
|-------------------------------------------------------------------------------------------------------------|-----------------------------------|
| [ZoneOffsetTransition](https://developer.android.com/reference/kotlin/java/time/zone/ZoneOffsetTransition)! | the transition instance, not null |

### equals

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Checks if this object equals another.

The entire state of the object is compared.

| Parameters ||
|-------------|----------------------------------------------------|
| `obj` | the reference object with which to compare. |
| `otherRule` | the other object to compare to, null returns false |

| Return ||
|------------------------------------------------------------------------------------|---------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if equal |

### getDayOfMonthIndicator

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDayOfMonthIndicator(): Int
```

Gets the indicator of the day-of-month of the transition.

If the rule defines an exact date then the day is the month of that date.

If the rule defines a week where the transition might occur, then the day defines either the start of the end of the transition week.

If the value is positive, then it represents a normal day-of-month, and is the earliest possible date that the transition can be. The date may refer to 29th February which should be treated as 1st March in non-leap years.

If the value is negative, then it represents the number of days back from the end of the month where`-1`is the last day of the month. In this case, the day identified is the latest possible date that the transition can be.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the day-of-month indicator, from -28 to 31 excluding 0 |

### getDayOfWeek

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDayOfWeek(): DayOfWeek!
```

Gets the day-of-week of the transition.

If the rule defines an exact date then this returns null.

If the rule defines a week where the cutover might occur, then this method returns the day-of-week that the month-day will be adjusted to. If the day is positive then the adjustment is later. If the day is negative then the adjustment is earlier.

| Return ||
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [DayOfWeek](https://developer.android.com/reference/kotlin/java/time/DayOfWeek.html#)! | the day-of-week that the transition occurs, null if the rule defines an exact date |

### getLocalTime

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLocalTime(): LocalTime!
```

Gets the local time of day of the transition which must be checked with [isMidnightEndOfDay()](https://developer.android.com/reference/kotlin/java/time/zone/ZoneOffsetTransitionRule#isMidnightEndOfDay()).

The time is converted into an instant using the time definition.

| Return ||
|----------------------------------------------------------------------------------------|---------------------------------------------------|
| [LocalTime](https://developer.android.com/reference/kotlin/java/time/LocalTime.html#)! | the local time of day of the transition, not null |

### getMonth

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMonth(): Month!
```

Gets the month of the transition.

If the rule defines an exact date then the month is the month of that date.

If the rule defines a week where the transition might occur, then the month if the month of either the earliest or latest possible date of the cutover.

| Return ||
|--------------------------------------------------------------------------------|---------------------------------------|
| [Month](https://developer.android.com/reference/kotlin/java/time/Month.html#)! | the month of the transition, not null |

### getOffsetAfter

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getOffsetAfter(): ZoneOffset!
```

Gets the offset after the transition.

| Return ||
|------------------------------------------------------------------------------------------|----------------------------|
| [ZoneOffset](https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#)! | the offset after, not null |

### getOffsetBefore

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getOffsetBefore(): ZoneOffset!
```

Gets the offset before the transition.

| Return ||
|------------------------------------------------------------------------------------------|-----------------------------|
| [ZoneOffset](https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#)! | the offset before, not null |

### getStandardOffset

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getStandardOffset(): ZoneOffset!
```

Gets the standard offset in force at the transition.

| Return ||
|------------------------------------------------------------------------------------------|-------------------------------|
| [ZoneOffset](https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#)! | the standard offset, not null |

### getTimeDefinition

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTimeDefinition(): ZoneOffsetTransitionRule.TimeDefinition!
```

Gets the time definition, specifying how to convert the time to an instant.

The local time can be converted to an instant using the standard offset, the wall offset or UTC.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| [ZoneOffsetTransitionRule.TimeDefinition](https://developer.android.com/reference/kotlin/java/time/zone/ZoneOffsetTransitionRule.TimeDefinition)! | the time definition, not null |

### hashCode

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

Returns a suitable hash code.

| Return ||
|----------------------------------------------------------------------------|---------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the hash code |

### isMidnightEndOfDay

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isMidnightEndOfDay(): Boolean
```

Is the transition local time midnight at the end of day.

The transition may be represented as occurring at 24:00.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether a local time of midnight is at the start or end of the day |

### of

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun of(
    month: Month!, 
    dayOfMonthIndicator: Int, 
    dayOfWeek: DayOfWeek!, 
    time: LocalTime!, 
    timeEndOfDay: Boolean, 
    timeDefinition: ZoneOffsetTransitionRule.TimeDefinition!, 
    standardOffset: ZoneOffset!, 
    offsetBefore: ZoneOffset!, 
    offsetAfter: ZoneOffset!
): ZoneOffsetTransitionRule!
```

Obtains an instance defining the yearly rule to create transitions between two offsets.

Applications should normally obtain an instance from [ZoneRules](https://developer.android.com/reference/kotlin/java/time/zone/ZoneRules). This factory is only intended for use when creating [ZoneRules](https://developer.android.com/reference/kotlin/java/time/zone/ZoneRules).

| Parameters ||
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `month` | [Month](https://developer.android.com/reference/kotlin/java/time/Month.html#)!:the month of the month-day of the first day of the cutover week, not null |
| `dayOfMonthIndicator` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the day of the month-day of the cutover week, positive if the week is that day or later, negative if the week is that day or earlier, counting from the last day of the month, from -28 to 31 excluding 0 |
| `dayOfWeek` | [DayOfWeek](https://developer.android.com/reference/kotlin/java/time/DayOfWeek.html#)!:the required day-of-week, null if the month-day should not be changed |
| --- | --- |
| `time` | [LocalTime](https://developer.android.com/reference/kotlin/java/time/LocalTime.html#)!:the cutover time in the 'before' offset, not null |
| `timeEndOfDay` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):whether the time is midnight at the end of day |
| `timeDefinition` | [ZoneOffsetTransitionRule.TimeDefinition](https://developer.android.com/reference/kotlin/java/time/zone/ZoneOffsetTransitionRule.TimeDefinition)!:how to interpret the cutover |
| --- | --- |
| `standardOffset` | [ZoneOffset](https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#)!:the standard offset in force at the cutover, not null |
| `offsetBefore` | [ZoneOffset](https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#)!:the offset before the cutover, not null |
| `offsetAfter` | [ZoneOffset](https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#)!:the offset after the cutover, not null |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------------------------------------------------|--------------------|
| [ZoneOffsetTransitionRule](https://developer.android.com/reference/kotlin/java/time/zone/ZoneOffsetTransitionRule#)! | the rule, not null |

| Exceptions ||
|--------------------------------------|------------------------------------------|
| `java.lang.IllegalArgumentException` | if`time.getNano()`returns non-zero value |

### toString

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Returns a string describing this object.

| Return ||
|----------------------------------------------------------------------------------|----------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string for debugging, not null |
