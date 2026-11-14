# SimpleTimeZone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SimpleTimeZone

```
open class SimpleTimeZone : TimeZone
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.util.TimeZone](https://developer.android.com/reference/kotlin/java/util/TimeZone) ||
| | ↳ | [java.util.SimpleTimeZone](https://developer.android.com/reference/kotlin/java/util/SimpleTimeZone#) |

`SimpleTimeZone`is a concrete subclass of`TimeZone`that represents a time zone for use with a Gregorian calendar. The class holds an offset from GMT, called*raw offset* , and start and end rules for a daylight saving time schedule. Since it only holds single values for each, it cannot handle historical changes in the offset from GMT and the daylight saving schedule, except that the [setStartYear](https://developer.android.com/reference/kotlin/java/util/SimpleTimeZone#setStartYear(kotlin.Int))method can specify the year when the daylight saving time schedule starts in effect.

To construct a`SimpleTimeZone`with a daylight saving time schedule, the schedule can be described with a set of rules,*start-rule* and*end-rule* . A day when daylight saving time starts or ends is specified by a combination of*month* ,*day-of-month* , and*day-of-week* values. The*month* value is represented by a Calendar [MONTH](https://developer.android.com/reference/kotlin/java/util/Calendar#MONTH:kotlin.Int) field value, such as [Calendar.MARCH](https://developer.android.com/reference/kotlin/java/util/Calendar#MARCH:kotlin.Int). The*day-of-week* value is represented by a Calendar [DAY_OF_WEEK](https://developer.android.com/reference/kotlin/java/util/Calendar#DAY_OF_WEEK:kotlin.Int) value, such as [SUNDAY](https://developer.android.com/reference/kotlin/java/util/Calendar#SUNDAY:kotlin.Int). The meanings of value combinations are as follows.

- **Exact day of month** 
 To specify an exact day of month, set the*month* and*day-of-month* to an exact value, and*day-of-week* to zero. For example, to specify March 1, set the*month* to [MARCH](https://developer.android.com/reference/kotlin/java/util/Calendar#MARCH:kotlin.Int),*day-of-month* to 1, and*day-of-week*to 0.
- **Day of week on or after day of month** 
 To specify a day of week on or after an exact day of month, set the*month* to an exact month value,*day-of-month* to the day on or after which the rule is applied, and*day-of-week* to a negative [DAY_OF_WEEK](https://developer.android.com/reference/kotlin/java/util/Calendar#DAY_OF_WEEK:kotlin.Int) field value. For example, to specify the second Sunday of April, set*month* to [APRIL](https://developer.android.com/reference/kotlin/java/util/Calendar#APRIL:kotlin.Int),*day-of-month* to 8, and*day-of-week* to`-` [SUNDAY](https://developer.android.com/reference/kotlin/java/util/Calendar#SUNDAY:kotlin.Int).
- **Day of week on or before day of month** 
 To specify a day of the week on or before an exact day of the month, set*day-of-month* and*day-of-week* to a negative value. For example, to specify the last Wednesday on or before the 21st of March, set*month* to [MARCH](https://developer.android.com/reference/kotlin/java/util/Calendar#MARCH:kotlin.Int),*day-of-month* is -21 and*day-of-week* is`-` [WEDNESDAY](https://developer.android.com/reference/kotlin/java/util/Calendar#WEDNESDAY:kotlin.Int).
- **Last day-of-week of month** 
 To specify, the last day-of-week of the month, set*day-of-week* to a [DAY_OF_WEEK](https://developer.android.com/reference/kotlin/java/util/Calendar#DAY_OF_WEEK:kotlin.Int) value and*day-of-month* to -1. For example, to specify the last Sunday of October, set*month* to [OCTOBER](https://developer.android.com/reference/kotlin/java/util/Calendar#OCTOBER:kotlin.Int),*day-of-week* to [SUNDAY](https://developer.android.com/reference/kotlin/java/util/Calendar#SUNDAY:kotlin.Int) and*day-of-month*to -1.

The time of the day at which daylight saving time starts or ends is specified by a millisecond value within the day. There are three kinds of*mode* s to specify the time: [WALL_TIME](https://developer.android.com/reference/kotlin/java/util/SimpleTimeZone#WALL_TIME:kotlin.Int), [STANDARD_TIME](https://developer.android.com/reference/kotlin/java/util/SimpleTimeZone#STANDARD_TIME:kotlin.Int) and [UTC_TIME](https://developer.android.com/reference/kotlin/java/util/SimpleTimeZone#UTC_TIME:kotlin.Int). For example, if daylight saving time ends at 2:00 am in the wall clock time, it can be specified by 7200000 milliseconds in the [WALL_TIME](https://developer.android.com/reference/kotlin/java/util/SimpleTimeZone#WALL_TIME:kotlin.Int) mode. In this case, the wall clock time for an*end-rule* means the same thing as the daylight time.

The following are examples of parameters for constructing time zone objects. 

```kotlin
<code>
       // Base GMT offset: -8:00
       // DST starts:      at 2:00am in standard time
       //                  on the first Sunday in April
       // DST ends:        at 2:00am in daylight time
       //                  on the last Sunday in October
       // Save:            1 hour
       SimpleTimeZone(-28800000,
                      "America/Los_Angeles",
                      Calendar.APRIL, 1, -Calendar.SUNDAY,
                      7200000,
                      Calendar.OCTOBER, -1, Calendar.SUNDAY,
                      7200000,
                      3600000)
 
       // Base GMT offset: +1:00
       // DST starts:      at 1:00am in UTC time
       //                  on the last Sunday in March
       // DST ends:        at 1:00am in UTC time
       //                  on the last Sunday in October
       // Save:            1 hour
       SimpleTimeZone(3600000,
                      "Europe/Paris",
                      Calendar.MARCH, -1, Calendar.SUNDAY,
                      3600000, SimpleTimeZone.UTC_TIME,
                      Calendar.OCTOBER, -1, Calendar.SUNDAY,
                      3600000, SimpleTimeZone.UTC_TIME,
                      3600000)
  </code>
```
These parameter rules are also applicable to the set rule methods, such as`setStartRule`.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STANDARD_TIME](https://developer.android.com/reference/kotlin/java/util/SimpleTimeZone#STANDARD_TIME:kotlin.Int) Constant for a mode of start or end time specified as standard time. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UTC_TIME](https://developer.android.com/reference/kotlin/java/util/SimpleTimeZone#UTC_TIME:kotlin.Int) Constant for a mode of start or end time specified as UTC. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WALL_TIME](https://developer.android.com/reference/kotlin/java/util/SimpleTimeZone#WALL_TIME:kotlin.Int) Constant for a mode of start or end time specified as wall clock time. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class [TimeZone](https://developer.android.com/reference/kotlin/java/util/TimeZone) |----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LONG](https://developer.android.com/reference/kotlin/java/util/TimeZone#LONG:kotlin.Int) <br /> A style specifier for`getDisplayName()`indicating a long name, such as "Pacific Standard Time." <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SHORT](https://developer.android.com/reference/kotlin/java/util/TimeZone#SHORT:kotlin.Int) <br /> A style specifier for`getDisplayName()`indicating a short name, such as "PST." <br /> | ||

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SimpleTimeZone](https://developer.android.com/reference/kotlin/java/util/SimpleTimeZone#SimpleTimeZone(kotlin.Int,%20kotlin.String))`(`rawOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `ID:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a SimpleTimeZone with the given base time zone offset from GMT and time zone ID with no daylight saving time schedule. |
| [SimpleTimeZone](https://developer.android.com/reference/kotlin/java/util/SimpleTimeZone#SimpleTimeZone(kotlin.Int,%20kotlin.String,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`rawOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `ID:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `startMonth:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `startDay:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `startDayOfWeek:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `startTime:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `endMonth:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `endDay:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `endDayOfWeek:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `endTime:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs a SimpleTimeZone with the given base time zone offset from GMT, time zone ID, and rules for starting and ending the daylight time. |
| [SimpleTimeZone](https://developer.android.com/reference/kotlin/java/util/SimpleTimeZone#SimpleTimeZone(kotlin.Int,%20kotlin.String,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`rawOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `ID:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `startMonth:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `startDay:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `startDayOfWeek:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `startTime:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `endMonth:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `endDay:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `endDayOfWeek:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `endTime:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dstSavings:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs a SimpleTimeZone with the given base time zone offset from GMT, time zone ID, and rules for starting and ending the daylight time. |
| [SimpleTimeZone](https://developer.android.com/reference/kotlin/java/util/SimpleTimeZone#SimpleTimeZone(kotlin.Int,%20kotlin.String,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`rawOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `ID:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `startMonth:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `startDay:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `startDayOfWeek:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `startTime:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `startTimeMode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `endMonth:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `endDay:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `endDayOfWeek:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `endTime:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `endTimeMode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dstSavings:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs a SimpleTimeZone with the given base time zone offset from GMT, time zone ID, and rules for starting and ending the daylight time. |

| Public methods ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [clone](https://developer.android.com/reference/kotlin/java/util/SimpleTimeZone#clone())`()` Returns a clone of this`SimpleTimeZone`instance. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/java/util/SimpleTimeZone#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Compares the equality of two`SimpleTimeZone`objects. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDSTSavings](https://developer.android.com/reference/kotlin/java/util/SimpleTimeZone#getDSTSavings())`()` Returns the amount of time in milliseconds that the clock is advanced during daylight saving time. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOffset](https://developer.android.com/reference/kotlin/java/util/SimpleTimeZone#getOffset(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`era:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `year:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `month:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `day:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dayOfWeek:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `millis:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the difference in milliseconds between local time and UTC, taking into account both the raw offset and the effect of daylight saving, for the specified date and time. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOffset](https://developer.android.com/reference/kotlin/java/util/SimpleTimeZone#getOffset(kotlin.Long))`(`date:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns the offset of this time zone from UTC at the given time. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRawOffset](https://developer.android.com/reference/kotlin/java/util/SimpleTimeZone#getRawOffset())`()` Gets the GMT offset for this time zone. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasSameRules](https://developer.android.com/reference/kotlin/java/util/SimpleTimeZone#hasSameRules(java.util.TimeZone))`(`other:` ` [TimeZone](https://developer.android.com/reference/kotlin/java/util/TimeZone)!`)` Returns`true`if this zone has the same rules and offset as another zone. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/java/util/SimpleTimeZone#hashCode())`()` Generates the hash code for the SimpleDateFormat object. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [inDaylightTime](https://developer.android.com/reference/kotlin/java/util/SimpleTimeZone#inDaylightTime(java.util.Date))`(`date:` ` [Date](https://developer.android.com/reference/kotlin/java/util/Date)!`)` Queries if the given date is in daylight saving time. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [observesDaylightTime](https://developer.android.com/reference/kotlin/java/util/SimpleTimeZone#observesDaylightTime())`()` Returns`true`if this`SimpleTimeZone`observes Daylight Saving Time. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDSTSavings](https://developer.android.com/reference/kotlin/java/util/SimpleTimeZone#setDSTSavings(kotlin.Int))`(`millisSavedDuringDST:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the amount of time in milliseconds that the clock is advanced during daylight saving time. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEndRule](https://developer.android.com/reference/kotlin/java/util/SimpleTimeZone#setEndRule(kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`endMonth:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `endDay:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `endTime:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the daylight saving time end rule to a fixed date within a month. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEndRule](https://developer.android.com/reference/kotlin/java/util/SimpleTimeZone#setEndRule(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`endMonth:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `endDay:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `endDayOfWeek:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `endTime:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the daylight saving time end rule. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEndRule](https://developer.android.com/reference/kotlin/java/util/SimpleTimeZone#setEndRule(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Boolean))`(`endMonth:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `endDay:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `endDayOfWeek:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `endTime:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `after:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets the daylight saving time end rule to a weekday before or after the given date within a month, e. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRawOffset](https://developer.android.com/reference/kotlin/java/util/SimpleTimeZone#setRawOffset(kotlin.Int))`(`offsetMillis:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the base time zone offset to GMT. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStartRule](https://developer.android.com/reference/kotlin/java/util/SimpleTimeZone#setStartRule(kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`startMonth:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `startDay:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `startTime:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the daylight saving time start rule to a fixed date within a month. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStartRule](https://developer.android.com/reference/kotlin/java/util/SimpleTimeZone#setStartRule(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`startMonth:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `startDay:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `startDayOfWeek:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `startTime:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the daylight saving time start rule. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStartRule](https://developer.android.com/reference/kotlin/java/util/SimpleTimeZone#setStartRule(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Boolean))`(`startMonth:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `startDay:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `startDayOfWeek:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `startTime:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `after:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets the daylight saving time start rule to a weekday before or after the given date within a month, e. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStartYear](https://developer.android.com/reference/kotlin/java/util/SimpleTimeZone#setStartYear(kotlin.Int))`(`year:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the daylight saving time starting year. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/util/SimpleTimeZone#toString())`()` Returns a string representation of this time zone. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [useDaylightTime](https://developer.android.com/reference/kotlin/java/util/SimpleTimeZone#useDaylightTime())`()` Queries if this time zone uses daylight saving time. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [TimeZone](https://developer.android.com/reference/kotlin/java/util/TimeZone) |--------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | [getAvailableIDs](https://developer.android.com/reference/kotlin/java/util/TimeZone#getAvailableIDs())`()` <br /> Gets all the available IDs supported. <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | [getAvailableIDs](https://developer.android.com/reference/kotlin/java/util/TimeZone#getAvailableIDs(kotlin.Int))`(`rawOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Gets the available IDs according to the given time zone offset in milliseconds. <br /> | | [TimeZone](https://developer.android.com/reference/kotlin/java/util/TimeZone)! | [getDefault](https://developer.android.com/reference/kotlin/java/util/TimeZone#getDefault())`()` <br /> Gets the default`TimeZone`for this host. The source of the default`TimeZone`may vary with implementation. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDisplayName](https://developer.android.com/reference/kotlin/java/util/TimeZone#getDisplayName())`()` <br /> Returns a long standard time name of this`TimeZone`suitable for presentation to the user in the default locale. This method is equivalent to: {@snippet lang=java : \* // @link substring="LONG" target="#LONG" : \* getDisplayName(false, LONG, \* // @link substring="Locale.Category.DISPLAY" target="Locale.Category#DISPLAY" : \* Locale.getDefault(Locale.Category.DISPLAY)); \* } <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDisplayName](https://developer.android.com/reference/kotlin/java/util/TimeZone#getDisplayName(kotlin.Boolean,%20kotlin.Int))`(`daylight:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `style:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Returns a name in the specified`style`of this`TimeZone`suitable for presentation to the user in the default locale. If the specified`daylight`is`true`, a Daylight Saving Time name is returned (even if this`TimeZone`doesn't observe Daylight Saving Time). Otherwise, a Standard Time name is returned. This method is equivalent to: {@snippet lang=java : \* getDisplayName(daylight, style, \* // @link substring="Locale.Category.DISPLAY" target="Locale.Category#DISPLAY" : \* Locale.getDefault(Locale.Category.DISPLAY)); \* } <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDisplayName](https://developer.android.com/reference/kotlin/java/util/TimeZone#getDisplayName(kotlin.Boolean,%20kotlin.Int,%20java.util.Locale))`(`daylightTime:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `style:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `locale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale)!`)` <br /> Returns the [short](https://developer.android.com/reference/kotlin/java/util/TimeZone#SHORT:kotlin.Int) or [long](https://developer.android.com/reference/kotlin/java/util/TimeZone#LONG:kotlin.Int) name of this time zone with either standard or daylight time, as written in`locale`. If the name is not available, the result is in the format`GMT[+-]hh:mm`. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDisplayName](https://developer.android.com/reference/kotlin/java/util/TimeZone#getDisplayName(java.util.Locale))`(`locale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale)!`)` <br /> Returns a long standard time name of this`TimeZone`suitable for presentation to the user in the specified`locale`. This method is equivalent to: {@snippet lang=java : \* // @link substring="LONG" target="#LONG" : \* getDisplayName(false, LONG, locale); \* } <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getID](https://developer.android.com/reference/kotlin/java/util/TimeZone#getID())`()` <br /> Gets the ID of this time zone. <br /> | | [TimeZone](https://developer.android.com/reference/kotlin/java/util/TimeZone)! | [getTimeZone](https://developer.android.com/reference/kotlin/java/util/TimeZone#getTimeZone(kotlin.String))`(`id:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Gets the`TimeZone`for the given ID. <br /> | | [TimeZone](https://developer.android.com/reference/kotlin/java/util/TimeZone)! | [getTimeZone](https://developer.android.com/reference/kotlin/java/util/TimeZone#getTimeZone(java.time.ZoneId))`(`zoneId:` ` [ZoneId](https://developer.android.com/reference/kotlin/java/time/ZoneId.html#)!`)` <br /> Gets the`TimeZone`for the given`zoneId`. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDefault](https://developer.android.com/reference/kotlin/java/util/TimeZone#setDefault(java.util.TimeZone))`(`timeZone:` ` [TimeZone](https://developer.android.com/reference/kotlin/java/util/TimeZone)!`)` <br /> Sets the`TimeZone`that is returned by the`getDefault`method.`zone`is cached. If`zone`is null, the cached default`TimeZone`is cleared. This method doesn't change the value of the`user.timezone`property. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setID](https://developer.android.com/reference/kotlin/java/util/TimeZone#setID(kotlin.String))`(`ID:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Sets the time zone ID. This does not change any other data in the time zone object. <br /> | | [ZoneId](https://developer.android.com/reference/kotlin/java/time/ZoneId.html#)! | [toZoneId](https://developer.android.com/reference/kotlin/java/util/TimeZone#toZoneId())`()` <br /> Converts this`TimeZone`object to a`ZoneId`. <br /> | ||

## Constants

### STANDARD_TIME

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STANDARD_TIME: Int
```

Constant for a mode of start or end time specified as standard time. 

 Value: 1

### UTC_TIME

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UTC_TIME: Int
```

Constant for a mode of start or end time specified as UTC. European Union rules are specified as UTC time, for example. 

 Value: 2

### WALL_TIME

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WALL_TIME: Int
```

Constant for a mode of start or end time specified as wall clock time. Wall clock time is standard time for the onset rule, and daylight time for the end rule. 

 Value: 0

## Public constructors

### SimpleTimeZone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SimpleTimeZone(
    rawOffset: Int, 
    ID: String!)
```

Constructs a SimpleTimeZone with the given base time zone offset from GMT and time zone ID with no daylight saving time schedule.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------|
| `rawOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The base time zone offset in milliseconds to GMT. |
| `ID` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The time zone name that is given to this instance. |

### SimpleTimeZone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SimpleTimeZone(
    rawOffset: Int, 
    ID: String!, 
    startMonth: Int, 
    startDay: Int, 
    startDayOfWeek: Int, 
    startTime: Int, 
    endMonth: Int, 
    endDay: Int, 
    endDayOfWeek: Int, 
    endTime: Int)
```

Constructs a SimpleTimeZone with the given base time zone offset from GMT, time zone ID, and rules for starting and ending the daylight time. Both`startTime`and`endTime`are specified to be represented in the wall clock time. The amount of daylight saving is assumed to be 3600000 milliseconds (i.e., one hour). This constructor is equivalent to: 

```kotlin
<code>
      SimpleTimeZone(rawOffset,
                     ID,
                     startMonth,
                     startDay,
                     startDayOfWeek,
                     startTime,
                     SimpleTimeZone.<code><a docref="java.util.SimpleTimeZone$WALL_TIME">#WALL_TIME</a></code>,
                     endMonth,
                     endDay,
                     endDayOfWeek,
                     endTime,
                     SimpleTimeZone.<code><a docref="java.util.SimpleTimeZone$WALL_TIME">#WALL_TIME</a></code>,
                     3600000)
  </code>
```

<br />

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `rawOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The given base time zone offset from GMT. |
| `ID` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The time zone ID which is given to this object. |
| `startMonth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The daylight saving time starting month. Month is a [MONTH](https://developer.android.com/reference/kotlin/java/util/Calendar#MONTH:kotlin.Int) field value (0-based. e.g., 0 for January). |
| --- | --- |
| `startDay` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The day of the month on which the daylight saving time starts. See the class description for the special cases of this parameter. |
| `startDayOfWeek` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The daylight saving time starting day-of-week. See the class description for the special cases of this parameter. |
| `startTime` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The daylight saving time starting time in local wall clock time (in milliseconds within the day), which is local standard time in this case. |
| --- | --- |
| `endMonth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The daylight saving time ending month. Month is a [MONTH](https://developer.android.com/reference/kotlin/java/util/Calendar#MONTH:kotlin.Int) field value (0-based. e.g., 9 for October). |
| `endDay` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The day of the month on which the daylight saving time ends. See the class description for the special cases of this parameter. |
| `endDayOfWeek` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The daylight saving time ending day-of-week. See the class description for the special cases of this parameter. |
| --- | --- |
| `endTime` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The daylight saving ending time in local wall clock time, (in milliseconds within the day) which is local daylight time in this case. |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the month, day, dayOfWeek, or time parameters are out of range for the start or end rule |

### SimpleTimeZone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SimpleTimeZone(
    rawOffset: Int, 
    ID: String!, 
    startMonth: Int, 
    startDay: Int, 
    startDayOfWeek: Int, 
    startTime: Int, 
    endMonth: Int, 
    endDay: Int, 
    endDayOfWeek: Int, 
    endTime: Int, 
    dstSavings: Int)
```

Constructs a SimpleTimeZone with the given base time zone offset from GMT, time zone ID, and rules for starting and ending the daylight time. Both`startTime`and`endTime`are assumed to be represented in the wall clock time. This constructor is equivalent to: 

```kotlin
<code>
      SimpleTimeZone(rawOffset,
                     ID,
                     startMonth,
                     startDay,
                     startDayOfWeek,
                     startTime,
                     SimpleTimeZone.<code><a docref="java.util.SimpleTimeZone$WALL_TIME">#WALL_TIME</a></code>,
                     endMonth,
                     endDay,
                     endDayOfWeek,
                     endTime,
                     SimpleTimeZone.<code><a docref="java.util.SimpleTimeZone$WALL_TIME">#WALL_TIME</a></code>,
                     dstSavings)
  </code>
```

<br />

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `rawOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The given base time zone offset from GMT. |
| `ID` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The time zone ID which is given to this object. |
| `startMonth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The daylight saving time starting month. Month is a [MONTH](https://developer.android.com/reference/kotlin/java/util/Calendar#MONTH:kotlin.Int) field value (0-based. e.g., 0 for January). |
| --- | --- |
| `startDay` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The day of the month on which the daylight saving time starts. See the class description for the special cases of this parameter. |
| `startDayOfWeek` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The daylight saving time starting day-of-week. See the class description for the special cases of this parameter. |
| `startTime` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The daylight saving time starting time in local wall clock time, which is local standard time in this case. |
| --- | --- |
| `endMonth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The daylight saving time ending month. Month is a [MONTH](https://developer.android.com/reference/kotlin/java/util/Calendar#MONTH:kotlin.Int) field value (0-based. e.g., 9 for October). |
| `endDay` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The day of the month on which the daylight saving time ends. See the class description for the special cases of this parameter. |
| `endDayOfWeek` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The daylight saving time ending day-of-week. See the class description for the special cases of this parameter. |
| --- | --- |
| `endTime` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The daylight saving ending time in local wall clock time, which is local daylight time in this case. |
| `dstSavings` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The amount of time in milliseconds saved during daylight saving time. |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the month, day, dayOfWeek, or time parameters are out of range for the start or end rule |

### SimpleTimeZone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SimpleTimeZone(
    rawOffset: Int, 
    ID: String!, 
    startMonth: Int, 
    startDay: Int, 
    startDayOfWeek: Int, 
    startTime: Int, 
    startTimeMode: Int, 
    endMonth: Int, 
    endDay: Int, 
    endDayOfWeek: Int, 
    endTime: Int, 
    endTimeMode: Int, 
    dstSavings: Int)
```

Constructs a SimpleTimeZone with the given base time zone offset from GMT, time zone ID, and rules for starting and ending the daylight time. This constructor takes the full set of the start and end rules parameters, including modes of`startTime`and`endTime`. The mode specifies either [wall](https://developer.android.com/reference/kotlin/java/util/SimpleTimeZone#WALL_TIME:kotlin.Int) or [standard time](https://developer.android.com/reference/kotlin/java/util/SimpleTimeZone#STANDARD_TIME:kotlin.Int) or [UTC](https://developer.android.com/reference/kotlin/java/util/SimpleTimeZone#UTC_TIME:kotlin.Int).

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `rawOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The given base time zone offset from GMT. |
| `ID` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The time zone ID which is given to this object. |
| `startMonth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The daylight saving time starting month. Month is a [MONTH](https://developer.android.com/reference/kotlin/java/util/Calendar#MONTH:kotlin.Int) field value (0-based. e.g., 0 for January). |
| --- | --- |
| `startDay` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The day of the month on which the daylight saving time starts. See the class description for the special cases of this parameter. |
| `startDayOfWeek` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The daylight saving time starting day-of-week. See the class description for the special cases of this parameter. |
| `startTime` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The daylight saving time starting time in the time mode specified by`startTimeMode`. |
| --- | --- |
| `startTimeMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The mode of the start time specified by startTime. |
| `endMonth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The daylight saving time ending month. Month is a [MONTH](https://developer.android.com/reference/kotlin/java/util/Calendar#MONTH:kotlin.Int) field value (0-based. e.g., 9 for October). |
| `endDay` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The day of the month on which the daylight saving time ends. See the class description for the special cases of this parameter. |
| --- | --- |
| `endDayOfWeek` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The daylight saving time ending day-of-week. See the class description for the special cases of this parameter. |
| `endTime` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The daylight saving ending time in time mode specified by`endTimeMode`. |
| `endTimeMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The mode of the end time specified by endTime |
| --- | --- |
| `dstSavings` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The amount of time in milliseconds saved during daylight saving time. |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the month, day, dayOfWeek, time more, or time parameters are out of range for the start or end rule, or if a time mode value is invalid. |

**See Also**

- [#WALL_TIME](https://developer.android.com/reference/kotlin/java/util/SimpleTimeZone#WALL_TIME:kotlin.Int)
- [#STANDARD_TIME](https://developer.android.com/reference/kotlin/java/util/SimpleTimeZone#STANDARD_TIME:kotlin.Int)
- [#UTC_TIME](https://developer.android.com/reference/kotlin/java/util/SimpleTimeZone#UTC_TIME:kotlin.Int)

## Public methods

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clone(): Any
```

Returns a clone of this`SimpleTimeZone`instance.

| Return ||
|----------------------------------------------------------------------------|---------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | a clone of this instance. |

| Exceptions ||
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the`Cloneable`interface. Subclasses that override the`clone`method can also throw this exception to indicate that an instance cannot be cloned. |

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

Compares the equality of two`SimpleTimeZone`objects.

| Parameters ||
|-------|------------------------------------------------|
| `obj` | The`SimpleTimeZone`object to be compared with. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the given`obj`is the same as this`SimpleTimeZone`object; false otherwise. |

### getDSTSavings

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDSTSavings(): Int
```

Returns the amount of time in milliseconds that the clock is advanced during daylight saving time.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of milliseconds the time is advanced with respect to standard time when the daylight saving rules are in effect, or 0 (zero) if this time zone doesn't observe daylight saving time. |

**See Also**

- [#setDSTSavings](https://developer.android.com/reference/kotlin/java/util/SimpleTimeZone#setDSTSavings(kotlin.Int)) 

### getOffset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getOffset(
    era: Int, 
    year: Int, 
    month: Int, 
    day: Int, 
    dayOfWeek: Int, 
    millis: Int
): Int
```

Returns the difference in milliseconds between local time and UTC, taking into account both the raw offset and the effect of daylight saving, for the specified date and time. This method assumes that the start and end month are distinct. It also uses a default [GregorianCalendar](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar) object as its underlying calendar, such as for determining leap years. Do not use the result of this method with a calendar other than a default`GregorianCalendar`.

*Note: In general, clients should use`Calendar.get(ZONE_OFFSET) + Calendar.get(DST_OFFSET)`instead of calling this method.*

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `era` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The era of the given date. |
| `year` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The year in the given date. |
| `month` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The month in the given date. Month is 0-based. e.g., 0 for January. |
| --- | --- |
| `day` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The day-in-month of the given date. |
| `dayOfWeek` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The day-of-week of the given date. |
| `milliseconds` | the milliseconds in day in*standard*local time. |
| --- | --- |
| `millis` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The milliseconds in day in*standard*local time. |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The milliseconds to add to UTC to get local time. |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | the`era`,`month`,`day`,`dayOfWeek`, or`millis`parameters are out of range |

### getOffset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getOffset(date: Long): Int
```

Returns the offset of this time zone from UTC at the given time. If daylight saving time is in effect at the given time, the offset value is adjusted with the amount of daylight saving.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------|
| `date` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the time at which the time zone offset is found |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the amount of time in milliseconds to add to UTC to get local time. |

### getRawOffset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRawOffset(): Int
```

Gets the GMT offset for this time zone.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the GMT offset value in milliseconds |

**See Also**

- [#setRawOffset](https://developer.android.com/reference/kotlin/java/util/SimpleTimeZone#setRawOffset(kotlin.Int)) 

### hasSameRules

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasSameRules(other: TimeZone!): Boolean
```

Returns`true`if this zone has the same rules and offset as another zone.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------|
| `other` | [TimeZone](https://developer.android.com/reference/kotlin/java/util/TimeZone)!:the TimeZone object to be compared with |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the given zone is a SimpleTimeZone and has the same rules and offset as this one |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

Generates the hash code for the SimpleDateFormat object.

| Return ||
|----------------------------------------------------------------------------|-------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the hash code for this object |

### inDaylightTime

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun inDaylightTime(date: Date!): Boolean
```

Queries if the given date is in daylight saving time.

| Parameters ||
|--------|----------------------------------------------------------------------------------------|
| `date` | [Date](https://developer.android.com/reference/kotlin/java/util/Date)!:the given Date. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if daylight saving time is in effective at the given date; false otherwise. |

| Exceptions ||
|----------------------------------|---------------------------------------------------------------|
| `java.lang.NullPointerException` | This method may throw a`NullPointerException`if`date`is`null` |

### observesDaylightTime

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun observesDaylightTime(): Boolean
```

Returns`true`if this`SimpleTimeZone`observes Daylight Saving Time. This method is equivalent to [useDaylightTime()](https://developer.android.com/reference/kotlin/java/util/SimpleTimeZone#useDaylightTime()).

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this`SimpleTimeZone`observes Daylight Saving Time;`false`otherwise. |

### setDSTSavings

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDSTSavings(millisSavedDuringDST: Int): Unit
```

Sets the amount of time in milliseconds that the clock is advanced during daylight saving time.

| Parameters ||
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `millisSavedDuringDST` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of milliseconds the time is advanced with respect to standard time when the daylight saving time rules are in effect. A positive number, typically one hour (3600000). |

**See Also**

- [#getDSTSavings](https://developer.android.com/reference/kotlin/java/util/SimpleTimeZone#getDSTSavings()) 

### setEndRule

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setEndRule(
    endMonth: Int, 
    endDay: Int, 
    endTime: Int
): Unit
```

Sets the daylight saving time end rule to a fixed date within a month. This method is equivalent to: 

```kotlin
<code>setEndRule(endMonth, endDay, 0, endTime)</code>
```

<br />

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `endMonth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The daylight saving time ending month. Month is a [MONTH](https://developer.android.com/reference/kotlin/java/util/Calendar#MONTH:kotlin.Int) field value (0-based. e.g., 9 for October). |
| `endDay` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The day of the month on which the daylight saving time ends. |
| `endTime` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The daylight saving ending time in local wall clock time, (in milliseconds within the day) which is local daylight time in this case. |
| --- | --- |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | the`endMonth`,`endDay`, or`endTime`parameters are out of range |

### setEndRule

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setEndRule(
    endMonth: Int, 
    endDay: Int, 
    endDayOfWeek: Int, 
    endTime: Int
): Unit
```

Sets the daylight saving time end rule. For example, if daylight saving time ends on the last Sunday in October at 2 am in wall clock time, you can set the end rule by calling:`setEndRule(Calendar.OCTOBER, -1, Calendar.SUNDAY, 2*60*60*1000);`

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `endMonth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The daylight saving time ending month. Month is a [MONTH](https://developer.android.com/reference/kotlin/java/util/Calendar#MONTH:kotlin.Int) field value (0-based. e.g., 9 for October). |
| `endDay` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The day of the month on which the daylight saving time ends. See the class description for the special cases of this parameter. |
| `endDayOfWeek` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The daylight saving time ending day-of-week. See the class description for the special cases of this parameter. |
| --- | --- |
| `endTime` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The daylight saving ending time in local wall clock time, (in milliseconds within the day) which is local daylight time in this case. |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the`endMonth`,`endDay`,`endDayOfWeek`, or`endTime`parameters are out of range |

### setEndRule

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setEndRule(
    endMonth: Int, 
    endDay: Int, 
    endDayOfWeek: Int, 
    endTime: Int, 
    after: Boolean
): Unit
```

Sets the daylight saving time end rule to a weekday before or after the given date within a month, e.g., the first Monday on or after the 8th.

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `endMonth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The daylight saving time ending month. Month is a [MONTH](https://developer.android.com/reference/kotlin/java/util/Calendar#MONTH:kotlin.Int) field value (0-based. e.g., 9 for October). |
| `endDay` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The day of the month on which the daylight saving time ends. |
| `endDayOfWeek` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The daylight saving time ending day-of-week. |
| --- | --- |
| `endTime` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The daylight saving ending time in local wall clock time, (in milliseconds within the day) which is local daylight time in this case. |
| `after` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):If true, this rule selects the first`endDayOfWeek`on or*after* `endDay`. If false, this rule selects the last`endDayOfWeek`on or before`endDay`of the month. |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | the`endMonth`,`endDay`,`endDayOfWeek`, or`endTime`parameters are out of range |

### setRawOffset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setRawOffset(offsetMillis: Int): Unit
```

Sets the base time zone offset to GMT. This is the offset to add to UTC to get local time.

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------|
| `offsetMillis` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the given base time zone offset to GMT. |

**See Also**

- [#getRawOffset](https://developer.android.com/reference/kotlin/java/util/SimpleTimeZone#getRawOffset()) 

### setStartRule

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setStartRule(
    startMonth: Int, 
    startDay: Int, 
    startTime: Int
): Unit
```

Sets the daylight saving time start rule to a fixed date within a month. This method is equivalent to: 

```kotlin
<code>setStartRule(startMonth, startDay, 0, startTime)</code>
```

<br />

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `startMonth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The daylight saving time starting month. Month is a [MONTH](https://developer.android.com/reference/kotlin/java/util/Calendar#MONTH:kotlin.Int) field value (0-based. e.g., 0 for January). |
| `startDay` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The day of the month on which the daylight saving time starts. |
| `startTime` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The daylight saving time starting time in local wall clock time, which is local standard time in this case. See the class description for the special cases of this parameter. |
| --- | --- |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the`startMonth`,`startDayOfMonth`, or`startTime`parameters are out of range |

### setStartRule

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setStartRule(
    startMonth: Int, 
    startDay: Int, 
    startDayOfWeek: Int, 
    startTime: Int
): Unit
```

Sets the daylight saving time start rule. For example, if daylight saving time starts on the first Sunday in April at 2 am in local wall clock time, you can set the start rule by calling: 

```kotlin
<code>setStartRule(Calendar.APRIL, 1, Calendar.SUNDAY, 2*60*60*1000);</code>
```

<br />

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `startMonth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The daylight saving time starting month. Month is a [MONTH](https://developer.android.com/reference/kotlin/java/util/Calendar#MONTH:kotlin.Int) field value (0-based. e.g., 0 for January). |
| `startDay` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The day of the month on which the daylight saving time starts. See the class description for the special cases of this parameter. |
| `startDayOfWeek` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The daylight saving time starting day-of-week. See the class description for the special cases of this parameter. |
| --- | --- |
| `startTime` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The daylight saving time starting time in local wall clock time, which is local standard time in this case. |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the`startMonth`,`startDay`,`startDayOfWeek`, or`startTime`parameters are out of range |

### setStartRule

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setStartRule(
    startMonth: Int, 
    startDay: Int, 
    startDayOfWeek: Int, 
    startTime: Int, 
    after: Boolean
): Unit
```

Sets the daylight saving time start rule to a weekday before or after the given date within a month, e.g., the first Monday on or after the 8th.

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `startMonth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The daylight saving time starting month. Month is a [MONTH](https://developer.android.com/reference/kotlin/java/util/Calendar#MONTH:kotlin.Int) field value (0-based. e.g., 0 for January). |
| `startDay` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The day of the month on which the daylight saving time starts. |
| `startDayOfWeek` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The daylight saving time starting day-of-week. |
| --- | --- |
| `startTime` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The daylight saving time starting time in local wall clock time, which is local standard time in this case. |
| `after` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):If true, this rule selects the first`dayOfWeek`on or*after* `dayOfMonth`. If false, this rule selects the last`dayOfWeek`on or*before* `dayOfMonth`. |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the`startMonth`,`startDay`,`startDayOfWeek`, or`startTime`parameters are out of range |

### setStartYear

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setStartYear(year: Int): Unit
```

Sets the daylight saving time starting year.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------|
| `year` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The daylight saving starting year. |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Returns a string representation of this time zone.

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of this time zone. |

### useDaylightTime

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun useDaylightTime(): Boolean
```

Queries if this time zone uses daylight saving time.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this time zone uses daylight saving time; false otherwise. |
