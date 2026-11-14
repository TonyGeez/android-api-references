Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Time

```
open class Time
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.text.format.Time](https://developer.android.com/reference/kotlin/android/text/format/Time#) |

> [!CAUTION]
> **This class was deprecated in API level 22.**
>
> Use `https://developer.android.com/reference/kotlin/java/time/ZonedDateTime.html#` instead.

An alternative to the `https://developer.android.com/reference/kotlin/java/util/Calendar.html#` and `https://developer.android.com/reference/kotlin/java/util/GregorianCalendar.html#` classes. An instance of the Time class represents a moment in time, specified with second precision. It is modelled after struct tm. This class is not thread-safe and does not consider leap seconds.

This class has a number of issues and it is recommended that `https://developer.android.com/reference/kotlin/java/time/ZonedDateTime.html#` is used instead.

Known issues:

- For historical reasons when performing time calculations all arithmetic currently takes place using 32-bit integers. This limits the reliable time range representable from 1902 until 2037.See the wikipedia article on the [Year 2038 problem](http://en.wikipedia.org/wiki/Year_2038_problem) for details. Do not rely on this behavior; it may change in the future.
- Calling `https://developer.android.com/reference/kotlin/android/text/format/Time#switchTimezone(kotlin.String)` on a date that cannot exist, such as a wall time that was skipped due to a DST transition, will result in a date in 1969 (i.e. -1, or 1 second before 1st Jan 1970 UTC).
- Much of the formatting / parsing assumes ASCII text and is therefore not suitable for use with non-ASCII scripts.
- No support for pseudo-zones like "GMT-07:00".

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/format/Time#EPOCH_JULIAN_DAY:kotlin.Int` The Julian day of the epoch, that is, January 1, 1970 on the Gregorian calendar. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/format/Time#FRIDAY:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/format/Time#HOUR:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/format/Time#MINUTE:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/format/Time#MONDAY:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/format/Time#MONDAY_BEFORE_JULIAN_EPOCH:kotlin.Int` The Julian day of the Monday in the week of the epoch, December 29, 1969 on the Gregorian calendar. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/format/Time#MONTH:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/format/Time#MONTH_DAY:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/format/Time#SATURDAY:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/format/Time#SECOND:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/format/Time#SUNDAY:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/format/Time#THURSDAY:kotlin.Int` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/format/Time#TIMEZONE_UTC:kotlin.String` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/format/Time#TUESDAY:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/format/Time#WEDNESDAY:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/format/Time#WEEK_DAY:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/format/Time#WEEK_NUM:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/format/Time#YEAR:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/format/Time#YEAR_DAY:kotlin.Int` <br /> |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/text/format/Time#Time()()` Construct a Time object in the default timezone. |
| `https://developer.android.com/reference/kotlin/android/text/format/Time#Time(android.text.format.Time)(other: https://developer.android.com/reference/kotlin/android/text/format/Time#!)` A copy constructor. |
| `https://developer.android.com/reference/kotlin/android/text/format/Time#Time(kotlin.String)(timezoneId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Construct a Time object in the timezone named by the string argument "timezone". |

| Public methods ||
|---|---|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/text/format/Time#after(android.text.format.Time)(that: https://developer.android.com/reference/kotlin/android/text/format/Time#!)` Returns true if the time represented by this Time object occurs after the given time. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/text/format/Time#before(android.text.format.Time)(that: https://developer.android.com/reference/kotlin/android/text/format/Time#!)` Returns true if the time represented by this Time object occurs before the given time. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/text/format/Time#clear(kotlin.String)(timezoneId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Clears all values, setting the timezone to the given timezone. |
| open static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/format/Time#compare(android.text.format.Time,%20android.text.format.Time)(a: https://developer.android.com/reference/kotlin/android/text/format/Time#!, b: https://developer.android.com/reference/kotlin/android/text/format/Time#!)` Compare two `Time` objects and return a negative number if `a` is less than `b`, a positive number if `a` is greater than `b`, or 0 if they are equal. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/text/format/Time#format(kotlin.String)(format: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Print the current value given the format string provided. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/text/format/Time#format2445()()` Format according to RFC 2445 DATE-TIME type. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/text/format/Time#format3339(kotlin.Boolean)(allDay: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Return a string in the RFC 3339 format. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/format/Time#getActualMaximum(kotlin.Int)(field: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Return the maximum possible value for the given field given the value of the other fields. |
| open static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/text/format/Time#getCurrentTimezone()()` Returns the timezone string that is currently set for the device. |
| open static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/format/Time#getJulianDay(kotlin.Long,%20kotlin.Long)(millis: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, gmtoffSeconds: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Computes the Julian day number for a point in time in a particular timezone. |
| open static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/format/Time#getJulianMondayFromWeeksSinceEpoch(kotlin.Int)(week: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Takes a number of weeks since the epoch and calculates the Julian day of the Monday for that week. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/format/Time#getWeekNumber()()` Computes the week number according to ISO 8601. |
| open static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/format/Time#getWeeksSinceEpochFromJulianDay(kotlin.Int,%20kotlin.Int)(julianDay: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, firstDayOfWeek: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the week since `https://developer.android.com/reference/kotlin/android/text/format/Time#EPOCH_JULIAN_DAY:kotlin.Int` (Jan 1, 1970) adjusted for first day of week. |
| open static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/text/format/Time#isEpoch(android.text.format.Time)(time: https://developer.android.com/reference/kotlin/android/text/format/Time#!)` Returns true if the instant of the supplied time would be for the Gregorian calendar date January 1, 1970 *for a user observing UTC*, i. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/text/format/Time#normalize(kotlin.Boolean)(ignoreDst: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Ensures the values in each field are in range. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/text/format/Time#parse(kotlin.String)(s: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Parses a date-time string in either the RFC 2445 format or an abbreviated format that does not include the "time" field. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/text/format/Time#parse3339(kotlin.String)(s: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Parse a time in RFC 3339 format. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/text/format/Time#set(android.text.format.Time)(that: https://developer.android.com/reference/kotlin/android/text/format/Time#!)` Copy the value of that to this Time object. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/text/format/Time#set(kotlin.Int,%20kotlin.Int,%20kotlin.Int)(monthDay: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, month: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, year: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the date from the given fields. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/text/format/Time#set(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(second: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, minute: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, hour: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, monthDay: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, month: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, year: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the fields. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/text/format/Time#set(kotlin.Long)(millis: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Sets the fields in this Time object given the UTC milliseconds. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/text/format/Time#setJulianDay(kotlin.Int)(julianDay: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the time from the given Julian day number, which must be based on the same timezone that is set in this Time object. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/text/format/Time#setToNow()()` Sets the time of the given Time object to the current time. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/text/format/Time#switchTimezone(kotlin.String)(timezone: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Convert this time object so the time represented remains the same, but is instead located in a different timezone. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/text/format/Time#toMillis(kotlin.Boolean)(ignoreDst: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Converts this time to milliseconds. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/format/Time#toString()()` Return the current time in YYYYMMDDTHHMMSS\<tz\> format |

| Properties ||
|---|---|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/text/format/Time#allDay:kotlin.Boolean` True if this is an allDay event. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/text/format/Time#gmtoff:kotlin.Long` Offset in seconds from UTC including any DST offset. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/format/Time#hour:kotlin.Int` Hour of day \[0-23\] |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/format/Time#isDst:kotlin.Int` This time is in daylight savings time. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/format/Time#minute:kotlin.Int` Minute \[0-59\] |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/format/Time#month:kotlin.Int` Month \[0-11\] |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/format/Time#monthDay:kotlin.Int` Day of month \[1-31\] |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/format/Time#second:kotlin.Int` Seconds \[0-61\] (2 leap seconds allowed) |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/text/format/Time#timezone:kotlin.String` The timezone for this Time. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/format/Time#weekDay:kotlin.Int` Day of week \[0-6\] |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/format/Time#year:kotlin.Int` Year. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/format/Time#yearDay:kotlin.Int` Day of year \[0-365\] |

## Constants

### EPOCH_JULIAN_DAY

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EPOCH_JULIAN_DAY: Int
```

**Deprecated:** *Deprecated in Java.*

The Julian day of the epoch, that is, January 1, 1970 on the Gregorian calendar.

 Value: 2440588

### FRIDAY

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FRIDAY: Int
```

**Deprecated:** *Deprecated in Java.*

 Value: 5

### HOUR

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HOUR: Int
```

**Deprecated:** *Deprecated in Java.*

 Value: 3

### MINUTE

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MINUTE: Int
```

**Deprecated:** *Deprecated in Java.*

 Value: 2

### MONDAY

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MONDAY: Int
```

**Deprecated:** *Deprecated in Java.*

 Value: 1

### MONDAY_BEFORE_JULIAN_EPOCH

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MONDAY_BEFORE_JULIAN_EPOCH: Int
```

**Deprecated:** *Deprecated in Java.*

The Julian day of the Monday in the week of the epoch, December 29, 1969 on the Gregorian calendar.

 Value: 2440585

### MONTH

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MONTH: Int
```

**Deprecated:** *Deprecated in Java.*

 Value: 5

### MONTH_DAY

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MONTH_DAY: Int
```

**Deprecated:** *Deprecated in Java.*

 Value: 4

### SATURDAY

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SATURDAY: Int
```

**Deprecated:** *Deprecated in Java.*

 Value: 6

### SECOND

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SECOND: Int
```

**Deprecated:** *Deprecated in Java.*

 Value: 1

### SUNDAY

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SUNDAY: Int
```

**Deprecated:** *Deprecated in Java.*

 Value: 0

### THURSDAY

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val THURSDAY: Int
```

**Deprecated:** *Deprecated in Java.*

 Value: 4

### TIMEZONE_UTC

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TIMEZONE_UTC: String
```

**Deprecated:** *Deprecated in Java.*

 Value: "UTC"

### TUESDAY

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TUESDAY: Int
```

**Deprecated:** *Deprecated in Java.*

 Value: 2

### WEDNESDAY

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WEDNESDAY: Int
```

**Deprecated:** *Deprecated in Java.*

 Value: 3

### WEEK_DAY

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WEEK_DAY: Int
```

**Deprecated:** *Deprecated in Java.*

 Value: 7

### WEEK_NUM

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WEEK_NUM: Int
```

**Deprecated:** *Deprecated in Java.*

 Value: 9

### YEAR

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val YEAR: Int
```

**Deprecated:** *Deprecated in Java.*

 Value: 6

### YEAR_DAY

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val YEAR_DAY: Int
```

**Deprecated:** *Deprecated in Java.*

 Value: 8

## Public constructors

### Time

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Time()
```

Construct a Time object in the default timezone. The time is initialized to Jan 1, 1970.

### Time

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Time(other: Time!)
```

A copy constructor. Construct a Time object by copying the given Time object. No normalization occurs.

| Parameters ||
|---|---|
| `other` | [Time](https://developer.android.com/reference/kotlin/android/text/format/Time#)!: |

### Time

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Time(timezoneId: String!)
```

Construct a Time object in the timezone named by the string argument "timezone". The time is initialized to Jan 1, 1970.

| Parameters ||
|---|---|
| `timezoneId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: string containing the timezone to use. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/TimeZone.html#`

## Public methods

### after

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun after(that: Time!): Boolean
```

**Deprecated:** *Deprecated in Java.*

Returns true if the time represented by this Time object occurs after the given time.

Equivalent to `Time.compare(this, that) > 0`. See `https://developer.android.com/reference/kotlin/android/text/format/Time#compare(android.text.format.Time,%20android.text.format.Time)` for details.

| Parameters ||
|---|---|
| `that` | [Time](https://developer.android.com/reference/kotlin/android/text/format/Time#)!: a given Time object to compare against |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this time is greater than the given time |

### before

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun before(that: Time!): Boolean
```

**Deprecated:** *Deprecated in Java.*

Returns true if the time represented by this Time object occurs before the given time.

Equivalent to `Time.compare(this, that) < 0`. See `https://developer.android.com/reference/kotlin/android/text/format/Time#compare(android.text.format.Time,%20android.text.format.Time)` for details.

| Parameters ||
|---|---|
| `that` | [Time](https://developer.android.com/reference/kotlin/android/text/format/Time#)!: a given Time object to compare against |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this time is less than the given time |

### clear

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clear(timezoneId: String!): Unit
```

**Deprecated:** *Deprecated in Java.*

Clears all values, setting the timezone to the given timezone. Sets isDst to a negative value to mean "unknown".

| Parameters ||
|---|---|
| `timezoneId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the timezone to use. |

### compare

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun compare(
    a: Time!, 
    b: Time!
): Int
```

**Deprecated:** *Deprecated in Java.*

Compare two `Time` objects and return a negative number if `a` is less than `b`, a positive number if `a` is greater than `b`, or 0 if they are equal.

This method can return an incorrect answer when the date / time fields of either `Time` have been set to a local time that contradicts the available timezone information.

| Parameters ||
|---|---|
| `a` | [Time](https://developer.android.com/reference/kotlin/android/text/format/Time#)!: first `Time` instance to compare |
| `b` | [Time](https://developer.android.com/reference/kotlin/android/text/format/Time#)!: second `Time` instance to compare |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a negative result if `a` is earlier, a positive result if `b` is earlier, or 0 if they are equal. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `https://developer.android.com/reference/kotlin/android/text/format/Time#allDay:kotlin.Boolean` is true but `hour`, `minute`, and `second` are not 0. |
| `java.lang.NullPointerException` | if either argument is `null` |

### format

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun format(format: String!): String!
```

**Deprecated:** *Deprecated in Java.*

Print the current value given the format string provided. See strftime(3) manual page for what means what. The final string must be less than 256 characters.

| Parameters ||
|---|---|
| `format` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: a string containing the desired format. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | a String containing the current time expressed in the current locale. |

### format2445

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun format2445(): String!
```

**Deprecated:** *Deprecated in Java.*

Format according to RFC 2445 DATE-TIME type.

The same as format("%Y%m%dT%H%M%S"), or format("%Y%m%dT%H%M%SZ") for a Time with a timezone set to "UTC".

### format3339

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun format3339(allDay: Boolean): String!
```

**Deprecated:** *Deprecated in Java.*

Return a string in the RFC 3339 format.

If allDay is true, expresses the time as Y-M-D

Otherwise, if the timezone is UTC, expresses the time as Y-M-D-T-H-M-S UTC

Otherwise the time is expressed the time as Y-M-D-T-H-M-S +- GMT

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | string in the RFC 3339 format. |

### getActualMaximum

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getActualMaximum(field: Int): Int
```

**Deprecated:** *Deprecated in Java.*

Return the maximum possible value for the given field given the value of the other fields. Requires that it be normalized for MONTH_DAY and YEAR_DAY.

| Parameters ||
|---|---|
| `field` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): one of the constants for HOUR, MINUTE, SECOND, etc. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the maximum value for the field. |

### getCurrentTimezone

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getCurrentTimezone(): String!
```

**Deprecated:** *Deprecated in Java.*

Returns the timezone string that is currently set for the device.

### getJulianDay

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getJulianDay(
    millis: Long, 
    gmtoffSeconds: Long
): Int
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/java/time/temporal/JulianFields.html#JULIAN_DAY:java.time.temporal.TemporalField` instead.*

Computes the Julian day number for a point in time in a particular timezone. The Julian day for a given calendar date is the same for every timezone. For example, the Julian day for July 1, 2008 is 2454649.

Callers must pass the time in UTC millisecond (as can be returned by `https://developer.android.com/reference/kotlin/android/text/format/Time#toMillis(kotlin.Boolean)` or `https://developer.android.com/reference/kotlin/android/text/format/Time#normalize(kotlin.Boolean)`) and the offset from UTC of the timezone in seconds at that time (as might be in `https://developer.android.com/reference/kotlin/android/text/format/Time#gmtoff:kotlin.Long`).

The Julian day is useful for testing if two events occur on the same calendar date and for determining the relative time of an event from the present ("yesterday", "3 days ago", etc.).

| Parameters ||
|---|---|
| `millis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the time in UTC milliseconds |
| `gmtoffSeconds` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the offset from UTC in seconds |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the Julian day |

### getJulianMondayFromWeeksSinceEpoch

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getJulianMondayFromWeeksSinceEpoch(week: Int): Int
```

**Deprecated:** *Deprecated in Java.*

Takes a number of weeks since the epoch and calculates the Julian day of the Monday for that week. This assumes that the week containing the `https://developer.android.com/reference/kotlin/android/text/format/Time#EPOCH_JULIAN_DAY:kotlin.Int` is considered week 0. It returns the Julian day for the Monday week weeks after the Monday of the week containing the epoch.

| Parameters ||
|---|---|
| `week` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Number of weeks since the epoch |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The julian day for the Monday of the given week since the epoch |

### getWeekNumber

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getWeekNumber(): Int
```

**Deprecated:** *Deprecated in Java.*

Computes the week number according to ISO 8601. The current Time object must already be normalized because this method uses the yearDay and weekDay fields.

In IS0 8601, weeks start on Monday. The first week of the year (week 1) is defined by ISO 8601 as the first week with four or more of its days in the starting year. Or equivalently, the week containing January 4. Or equivalently, the week with the year's first Thursday in it.

The week number can be calculated by counting Thursdays. Week N contains the Nth Thursday of the year.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the ISO week number. |

### getWeeksSinceEpochFromJulianDay

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getWeeksSinceEpochFromJulianDay(
    julianDay: Int, 
    firstDayOfWeek: Int
): Int
```

**Deprecated:** *Deprecated in Java.*

Returns the week since `https://developer.android.com/reference/kotlin/android/text/format/Time#EPOCH_JULIAN_DAY:kotlin.Int` (Jan 1, 1970) adjusted for first day of week. This takes a julian day and the week start day and calculates which week since `https://developer.android.com/reference/kotlin/android/text/format/Time#EPOCH_JULIAN_DAY:kotlin.Int` that day occurs in, starting at 0. \*Do not\* use this to compute the ISO week number for the year.

| Parameters ||
|---|---|
| `julianDay` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The julian day to calculate the week number for |
| `firstDayOfWeek` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Which week day is the first day of the week, see `https://developer.android.com/reference/kotlin/android/text/format/Time#SUNDAY:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Weeks since the epoch |

### isEpoch

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun isEpoch(time: Time!): Boolean
```

**Deprecated:** *Deprecated in Java.*

Returns true if the instant of the supplied time would be for the Gregorian calendar date January 1, 1970 *for a user observing UTC*, i.e. the timezone of the time object is ignored.

See `https://developer.android.com/reference/kotlin/android/text/format/Time#getJulianDay(kotlin.Long,%20kotlin.Long)` for how to determine the Julian day for the timezone of the time object.

This method can return an incorrect answer when the date / time fields have been set to a local time that contradicts the available timezone information.

| Parameters ||
|---|---|
| `time` | [Time](https://developer.android.com/reference/kotlin/android/text/format/Time#)!: the time to test |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if epoch. |

### normalize

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun normalize(ignoreDst: Boolean): Long
```

**Deprecated:** *Deprecated in Java.*

Ensures the values in each field are in range. For example if the current value of this calendar is March 32, normalize() will convert it to April 1. It also fills in weekDay, yearDay, isDst and gmtoff.

If "ignoreDst" is true, then this method sets the "isDst" field to -1 (the "unknown" value) before normalizing. It then computes the time in milliseconds and sets the correct value for "isDst" if the fields resolve to a valid date / time.

See `https://developer.android.com/reference/kotlin/android/text/format/Time#toMillis(kotlin.Boolean)` for more information about when to use true or false for "ignoreDst" and when `-1` might be returned.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the UTC milliseconds since the epoch, or `-1` |

### parse

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun parse(s: String!): Boolean
```

**Deprecated:** *Deprecated in Java.*

Parses a date-time string in either the RFC 2445 format or an abbreviated format that does not include the "time" field. For example, all of the following strings are valid:

- "20081013T160000Z"
- "20081013T160000"
- "20081013"

Returns whether or not the time is in UTC (ends with Z). If the string ends with "Z" then the timezone is set to UTC. If the date-time string included only a date and no time field, then the `allDay` field of this Time class is set to true and the `hour`, `minute`, and `second` fields are set to zero; otherwise (a time field was included in the date-time string) `allDay` is set to false. The fields `weekDay`, `yearDay`, and `gmtoff` are always set to zero, and the field `isDst` is set to -1 (unknown). To set those fields, call `https://developer.android.com/reference/kotlin/android/text/format/Time#normalize(kotlin.Boolean)` after parsing. To parse a date-time string and convert it to UTC milliseconds, do something like this:

```kotlin
Time time = new Time();
    String date = "20081013T160000Z";
    time.parse(date);
    long millis = time.normalize(false);
  
```

<br />

| Parameters ||
|---|---|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the string to parse |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the resulting time value is in UTC time |

| Exceptions ||
|---|---|
| `android.util.TimeFormatException` | if s cannot be parsed. |

### parse3339

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun parse3339(s: String!): Boolean
```

**Deprecated:** *Deprecated in Java.*

Parse a time in RFC 3339 format. This method also parses simple dates (that is, strings that contain no time or time offset). For example, all of the following strings are valid:

- "2008-10-13T16:00:00.000Z"
- "2008-10-13T16:00:00.000+07:00"
- "2008-10-13T16:00:00.000-07:00"
- "2008-10-13"

<br />

If the string contains a time and time offset, then the time offset will be used to convert the time value to UTC.

If the given string contains just a date (with no time field), then the `https://developer.android.com/reference/kotlin/android/text/format/Time#allDay:kotlin.Boolean` field is set to true and the `https://developer.android.com/reference/kotlin/android/text/format/Time#hour:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/text/format/Time#minute:kotlin.Int`, and `https://developer.android.com/reference/kotlin/android/text/format/Time#second:kotlin.Int` fields are set to zero.

Returns true if the resulting time value is in UTC time.

| Parameters ||
|---|---|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the string to parse |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the resulting time value is in UTC time |

| Exceptions ||
|---|---|
| `android.util.TimeFormatException` | if s cannot be parsed. |

### set

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun set(that: Time!): Unit
```

**Deprecated:** *Deprecated in Java.*

Copy the value of that to this Time object. No normalization happens.

### set

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun set(
    monthDay: Int, 
    month: Int, 
    year: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the date from the given fields. Also sets allDay to true. Sets weekDay, yearDay and gmtoff to 0, and isDst to -1. Call `https://developer.android.com/reference/kotlin/android/text/format/Time#normalize(kotlin.Boolean)` if you need those.

| Parameters ||
|---|---|
| `monthDay` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the day of the month (in the range \[1,31\]) |
| `month` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the zero-based month number (in the range \[0,11\]) |
| `year` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the year |

### set

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun set(
    second: Int, 
    minute: Int, 
    hour: Int, 
    monthDay: Int, 
    month: Int, 
    year: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the fields. Sets weekDay, yearDay and gmtoff to 0, and isDst to -1. Call `https://developer.android.com/reference/kotlin/android/text/format/Time#normalize(kotlin.Boolean)` if you need those.

### set

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun set(millis: Long): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the fields in this Time object given the UTC milliseconds. After this method returns, all the fields are normalized. This also sets the "isDst" field to the correct value.

| Parameters ||
|---|---|
| `millis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the time in UTC milliseconds since the epoch. |

### setJulianDay

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setJulianDay(julianDay: Int): Long
```

**Deprecated:** *Deprecated in Java.*

Sets the time from the given Julian day number, which must be based on the same timezone that is set in this Time object. The "gmtoff" field need not be initialized because the given Julian day may have a different GMT offset than whatever is currently stored in this Time object anyway. After this method returns all the fields will be normalized and the time will be set to 12am at the beginning of the given Julian day.

The only exception to this is if 12am does not exist for that day because of daylight saving time. For example, Cairo, Eqypt moves time ahead one hour at 12am on April 25, 2008 and there are a few other places that also change daylight saving time at 12am. In those cases, the time will be set to 1am.

| Parameters ||
|---|---|
| `julianDay` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the Julian day in the timezone for this Time object |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the UTC milliseconds for the beginning of the Julian day |

### setToNow

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setToNow(): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the time of the given Time object to the current time.

### switchTimezone

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun switchTimezone(timezone: String!): Unit
```

**Deprecated:** *Deprecated in Java.*

Convert this time object so the time represented remains the same, but is instead located in a different timezone. This method automatically calls normalize() in some cases.

This method can return incorrect results if the date / time cannot be normalized.

### toMillis

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toMillis(ignoreDst: Boolean): Long
```

**Deprecated:** *Deprecated in Java.*

Converts this time to milliseconds. Suitable for interacting with the standard java libraries. The time is in UTC milliseconds since the epoch. This does an implicit normalization to compute the milliseconds but does *not* change any of the fields in this Time object. If you want to normalize the fields in this Time object and also get the milliseconds then use `https://developer.android.com/reference/kotlin/android/text/format/Time#normalize(kotlin.Boolean)`.

If "ignoreDst" is false, then this method uses the current setting of the "isDst" field and will adjust the returned time if the "isDst" field is wrong for the given time. See the sample code below for an example of this.

If "ignoreDst" is true, then this method ignores the current setting of the "isDst" field in this Time object and will instead figure out the correct value of "isDst" (as best it can) from the fields in this Time object. The only case where this method cannot figure out the correct value of the "isDst" field is when the time is inherently ambiguous because it falls in the hour that is repeated when switching from Daylight-Saving Time to Standard Time.

Here is an example where toMillis(true) adjusts the time, assuming that DST changes at 2am on Sunday, Nov 4, 2007.

```kotlin
Time time = new Time();
  time.set(4, 10, 2007);  // set the date to Nov 4, 2007, 12am
  time.normalize(false);       // this sets isDst = 1
  time.monthDay += 1;     // changes the date to Nov 5, 2007, 12am
  millis = time.toMillis(false);   // millis is Nov 4, 2007, 11pm
  millis = time.toMillis(true);    // millis is Nov 5, 2007, 12am
  
```

To avoid this problem, use toMillis(true) after adding or subtracting days or explicitly setting the "monthDay" field. On the other hand, if you are adding or subtracting hours or minutes, then you should use toMillis(false).

You should also use toMillis(false) if you want to read back the same milliseconds that you set with `https://developer.android.com/reference/kotlin/android/text/format/Time#set(kotlin.Long)` or `https://developer.android.com/reference/kotlin/android/text/format/Time#set(android.text.format.Time)` or after parsing a date string.

This method can return `-1` when the date / time fields have been set to a local time that conflicts with available timezone information. For example, when daylight savings transitions cause an hour to be skipped: times within that hour will return `-1` if isDst = `-1`.

### toString

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

**Deprecated:** *Deprecated in Java.*

Return the current time in YYYYMMDDTHHMMSS\<tz\> format

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

## Properties

### allDay

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var allDay: Boolean
```

**Deprecated:** *Deprecated in Java.*

True if this is an allDay event. The hour, minute, second fields are all zero, and the date is displayed the same in all time zones.

### gmtoff

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var gmtoff: Long
```

**Deprecated:** *Deprecated in Java.*

Offset in seconds from UTC including any DST offset.

### hour

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var hour: Int
```

**Deprecated:** *Deprecated in Java.*

Hour of day \[0-23\]

### isDst

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var isDst: Int
```

**Deprecated:** *Deprecated in Java.*

This time is in daylight savings time. One of:

- **positive** - in dst
- **0** - not in dst
- **negative** - unknown

<br />

### minute

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var minute: Int
```

**Deprecated:** *Deprecated in Java.*

Minute \[0-59\]

### month

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var month: Int
```

**Deprecated:** *Deprecated in Java.*

Month \[0-11\]

### monthDay

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var monthDay: Int
```

**Deprecated:** *Deprecated in Java.*

Day of month \[1-31\]

### second

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var second: Int
```

**Deprecated:** *Deprecated in Java.*

Seconds \[0-61\] (2 leap seconds allowed)

### timezone

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var timezone: String!
```

**Deprecated:** *Deprecated in Java.*

The timezone for this Time. Should not be null.

### weekDay

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var weekDay: Int
```

**Deprecated:** *Deprecated in Java.*

Day of week \[0-6\]

### year

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var year: Int
```

**Deprecated:** *Deprecated in Java.*

Year. For example, 1970.

### yearDay

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var yearDay: Int
```

**Deprecated:** *Deprecated in Java.*

Day of year \[0-365\]
