Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Calendar

```
abstract class Calendar : Cloneable, Comparable<Calendar!>, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.Calendar](Calendar.md) |

| Known Direct Subclasses [GregorianCalendar](GregorianCalendar.md) |---|---| | [GregorianCalendar](GregorianCalendar.md) | `GregorianCalendar` is a concrete subclass of `Calendar` and provides the standard calendar system used by most of the world. | |
| --- | --- | --- | --- | --- | --- | --- |

The class is an abstract class that provides methods for converting between a specific instant in time and a set of `https://developer.android.com/reference/kotlin/java/util/Calendar#fields:kotlin.IntArray` such as `YEAR``MONTH``DAY_OF_MONTH``HOUR`, and so on, and for manipulating the calendar fields, such as getting the date of the next week. An instant in time can be represented by a millisecond value that is an offset from the *Epoch*, January 1, 1970 00:00:00.000 GMT (Gregorian).

The class also provides additional fields and methods for implementing a concrete calendar system outside the package. Those fields and methods are defined as `protected`.

Like other locale-sensitive classes, `Calendar` provides a class method, `getInstance`, for getting a generally useful object of this type. `Calendar`'s `getInstance` method returns a `Calendar` object whose calendar fields have been initialized with the current date and time:

```kotlin
Calendar rightNow = Calendar.getInstance();
  
```

A `Calendar` object can produce all the calendar field values needed to implement the date-time formatting for a particular language and calendar style (for example, Japanese-Gregorian, Japanese-Traditional). `Calendar` defines the range of values returned by certain calendar fields, as well as their meaning. For example, the first month of the calendar system has value `MONTH == JANUARY` for all calendars. Other values are defined by the concrete subclass, such as `ERA`. See individual field documentation and subclass documentation for details.

## Getting and Setting Calendar Field Values

The calendar field values can be set by calling the `set` methods. Any field values set in a `Calendar` will not be interpreted until it needs to calculate its time value (milliseconds from the Epoch) or values of the calendar fields. Calling the `get`, `getTimeInMillis`, `getTime`, `add` and `roll` involves such calculation.

### Leniency

`Calendar` has two modes for interpreting the calendar fields, *lenient* and *non-lenient* . When a `Calendar` is in lenient mode, it accepts a wider range of calendar field values than it produces. When a `Calendar` recomputes calendar field values for return by `get()`, all of the calendar fields are normalized. For example, a lenient `GregorianCalendar` interprets `MONTH == JANUARY`, `DAY_OF_MONTH == 32` as February 1.

When a `Calendar` is in non-lenient mode, it throws an exception if there is any inconsistency in its calendar fields. For example, a `GregorianCalendar` always produces `DAY_OF_MONTH` values between 1 and the length of the month. A non-lenient `GregorianCalendar` throws an exception upon calculating its time or calendar field values if any out-of-range field value has been set.

### First Week

`Calendar` defines a locale-specific seven day week using two parameters: the first day of the week and the minimal days in first week (from 1 to 7). These numbers are taken from the locale resource data or the locale itself when a `Calendar` is constructed. If the designated locale contains "fw" [Unicode extensions](Locale.md), the first day of the week will be obtained according to those extensions. They may also be specified explicitly through the methods for setting their values.

When setting or getting the `WEEK_OF_MONTH` or `WEEK_OF_YEAR` fields, `Calendar` must determine the first week of the month or year as a reference point. The first week of a month or year is defined as the earliest seven day period beginning on `getFirstDayOfWeek()` and containing at least `getMinimalDaysInFirstWeek()` days of that month or year. Weeks numbered ..., -1, 0 precede the first week; weeks numbered 2, 3,... follow it. Note that the normalized numbering returned by `get()` may be different. For example, a specific `Calendar` subclass may designate the week before week 1 of a year as week `n` of the previous year.

### Calendar Fields Resolution

When computing a date and time from the calendar fields, there may be insufficient information for the computation (such as only year and month with no day of month), or there may be inconsistent information (such as Tuesday, July 15, 1996 (Gregorian) -- July 15, 1996 is actually a Monday). `Calendar` will resolve calendar field values to determine the date and time in the following way.

If there is any conflict in calendar field values, `Calendar` gives priorities to calendar fields that have been set more recently. The following are the default combinations of the calendar fields. The most recent combination, as determined by the most recently set single field, will be used.

For the date fields:

```kotlin
YEAR + MONTH + DAY_OF_MONTH
  YEAR + MONTH + WEEK_OF_MONTH + DAY_OF_WEEK
  YEAR + MONTH + DAY_OF_WEEK_IN_MONTH + DAY_OF_WEEK
  YEAR + DAY_OF_YEAR
  YEAR + DAY_OF_WEEK + WEEK_OF_YEAR
  
```
For the time of day fields:

```kotlin
HOUR_OF_DAY
  AM_PM + HOUR
  
```

If there are any calendar fields whose values haven't been set in the selected field combination, `Calendar` uses their default values. The default value of each field may vary by concrete calendar systems. For example, in `GregorianCalendar`, the default of a field is the same as that of the start of the Epoch: i.e., `YEAR = 1970`, `MONTH = JANUARY`, `DAY_OF_MONTH = 1`, etc.

**Note:** There are certain possible ambiguities in interpretation of certain singular times, which are resolved in the following ways:

1. 23:59 is the last minute of the day and 00:00 is the first minute of the next day. Thus, 23:59 on Dec 31, 1999 \< 00:00 on Jan 1, 2000 \< 00:01 on Jan 1, 2000.
2. Although historically not precise, midnight also belongs to "am", and noon belongs to "pm", so on the same day, 12:00 am (midnight) \< 12:01 am, and 12:00 pm (noon) \< 12:01 pm

The date or time format strings are not part of the definition of a calendar, as those must be modifiable or overridable by the user at runtime. Use `https://developer.android.com/reference/kotlin/java/text/DateFormat.html#` to format dates.

### Field Manipulation

The calendar fields can be changed using three methods: `set()`, `add()`, and `roll()`.

**`set(f, value)`** changes calendar field `f` to `value`. In addition, it sets an internal member variable to indicate that calendar field `f` has been changed. Although calendar field `f` is changed immediately, the calendar's time value in milliseconds is not recomputed until the next call to `get()`, `getTime()`, `getTimeInMillis()`, `add()`, or `roll()` is made. Thus, multiple calls to `set()` do not trigger multiple, unnecessary computations. As a result of changing a calendar field using `set()`, other calendar fields may also change, depending on the calendar field, the calendar field value, and the calendar system. In addition, `get(f)` will not necessarily return `value` set by the call to the `set` method after the calendar fields have been recomputed. The specifics are determined by the concrete calendar class.

*Example* : Consider a `GregorianCalendar` originally set to August 31, 1999. Calling `set(Calendar.MONTH, Calendar.SEPTEMBER)` sets the date to September 31, 1999. This is a temporary internal representation that resolves to October 1, 1999 if `getTime()` is then called. However, a call to `set(Calendar.DAY_OF_MONTH, 30)` before the call to `getTime()` sets the date to September 30, 1999, since no recomputation occurs after `set()` itself.

**`add(f, delta)`** adds `delta` to field `f`. This is equivalent to calling `set(f, get(f) + delta)` with two adjustments:

**Add rule 1** . The value of field `f` after the call minus the value of field `f` before the call is `delta`, modulo any overflow that has occurred in field `f`. Overflow occurs when a field value exceeds its range and, as a result, the next larger field is incremented or decremented and the field value is adjusted back into its range.

**Add rule 2** . If a smaller field is expected to be invariant, but it is impossible for it to be equal to its prior value because of changes in its minimum or maximum after field `f` is changed or other constraints, such as time zone offset changes, then its value is adjusted to be as close as possible to its expected value. A smaller field represents a smaller unit of time. `HOUR` is a smaller field than `DAY_OF_MONTH`. No adjustment is made to smaller fields that are not expected to be invariant. The calendar system determines what fields are expected to be invariant.

In addition, unlike `set()`, `add()` forces an immediate recomputation of the calendar's milliseconds and all fields.

*Example* : Consider a `GregorianCalendar` originally set to August 31, 1999. Calling `add(Calendar.MONTH, 13)` sets the calendar to September 30, 2000. **Add rule 1** sets the `MONTH` field to September, since adding 13 months to August gives September of the next year. Since `DAY_OF_MONTH` cannot be 31 in September in a `GregorianCalendar`, **add rule 2** sets the `DAY_OF_MONTH` to 30, the closest possible value. Although it is a smaller field, `DAY_OF_WEEK` is not adjusted by rule 2, since it is expected to change when the month changes in a `GregorianCalendar`.

**`roll(f, delta)`** adds `delta` to field `f` without changing larger fields. This is equivalent to calling `add(f, delta)` with the following adjustment:

**Roll rule** . Larger fields are unchanged after the call. A larger field represents a larger unit of time. `DAY_OF_MONTH` is a larger field than `HOUR`.

*Example* : See roll.

**Usage model** . To motivate the behavior of `add()` and `roll()`, consider a user interface component with increment and decrement buttons for the month, day, and year, and an underlying `GregorianCalendar`. If the interface reads January 31, 1999 and the user presses the month increment button, what should it read? If the underlying implementation uses `set()`, it might read March 3, 1999. A better result would be February 28, 1999. Furthermore, if the user presses the month increment button again, it should read March 31, 1999, not March 28, 1999. By saving the original date and using either `add()` or `roll()`, depending on whether larger fields should be affected, the user interface can behave as most users will intuitively expect.

## Summary

| Nested classes ||
|---|---|
| open | `https://developer.android.com/reference/kotlin/java/util/Calendar.Builder` `Calendar.Builder` is used for creating a `Calendar` from various date-time parameters. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/Calendar#ALL_STYLES:kotlin.Int` A style specifier for getDisplayNames indicating names in all styles, such as "January" and "Jan". |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/Calendar#AM:kotlin.Int` Value of the `https://developer.android.com/reference/kotlin/java/util/Calendar#AM_PM:kotlin.Int` field indicating the period of the day from midnight to just before noon. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/Calendar#AM_PM:kotlin.Int` Field number for `get` and `set` indicating whether the `HOUR` is before or after noon. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/Calendar#APRIL:kotlin.Int` Value of the `https://developer.android.com/reference/kotlin/java/util/Calendar#MONTH:kotlin.Int` field indicating the fourth month of the year in the Gregorian and Julian calendars. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/Calendar#AUGUST:kotlin.Int` Value of the `https://developer.android.com/reference/kotlin/java/util/Calendar#MONTH:kotlin.Int` field indicating the eighth month of the year in the Gregorian and Julian calendars. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/Calendar#DATE:kotlin.Int` Field number for `get` and `set` indicating the day of the month. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/Calendar#DAY_OF_MONTH:kotlin.Int` Field number for `get` and `set` indicating the day of the month. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/Calendar#DAY_OF_WEEK:kotlin.Int` Field number for `get` and `set` indicating the day of the week. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/Calendar#DAY_OF_WEEK_IN_MONTH:kotlin.Int` Field number for `get` and `set` indicating the ordinal number of the day of the week within the current month. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/Calendar#DAY_OF_YEAR:kotlin.Int` Field number for `get` and `set` indicating the day number within the current year. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/Calendar#DECEMBER:kotlin.Int` Value of the `https://developer.android.com/reference/kotlin/java/util/Calendar#MONTH:kotlin.Int` field indicating the twelfth month of the year in the Gregorian and Julian calendars. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/Calendar#DST_OFFSET:kotlin.Int` Field number for `get` and `set` indicating the daylight saving offset in milliseconds. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/Calendar#ERA:kotlin.Int` Field number for `get` and `set` indicating the era, e. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/Calendar#FEBRUARY:kotlin.Int` Value of the `https://developer.android.com/reference/kotlin/java/util/Calendar#MONTH:kotlin.Int` field indicating the second month of the year in the Gregorian and Julian calendars. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/Calendar#FIELD_COUNT:kotlin.Int` The number of distinct fields recognized by `get` and `set`. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/Calendar#FRIDAY:kotlin.Int` Value of the `https://developer.android.com/reference/kotlin/java/util/Calendar#DAY_OF_WEEK:kotlin.Int` field indicating Friday. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/Calendar#HOUR:kotlin.Int` Field number for `get` and `set` indicating the hour of the morning or afternoon. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/Calendar#HOUR_OF_DAY:kotlin.Int` Field number for `get` and `set` indicating the hour of the day. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/Calendar#JANUARY:kotlin.Int` Value of the `https://developer.android.com/reference/kotlin/java/util/Calendar#MONTH:kotlin.Int` field indicating the first month of the year in the Gregorian and Julian calendars. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/Calendar#JULY:kotlin.Int` Value of the `https://developer.android.com/reference/kotlin/java/util/Calendar#MONTH:kotlin.Int` field indicating the seventh month of the year in the Gregorian and Julian calendars. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/Calendar#JUNE:kotlin.Int` Value of the `https://developer.android.com/reference/kotlin/java/util/Calendar#MONTH:kotlin.Int` field indicating the sixth month of the year in the Gregorian and Julian calendars. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/Calendar#LONG:kotlin.Int` A style specifier for getDisplayName and getDisplayNames equivalent to `https://developer.android.com/reference/kotlin/java/util/Calendar#LONG_FORMAT:kotlin.Int`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/Calendar#LONG_FORMAT:kotlin.Int` A style specifier for getDisplayName and getDisplayNames indicating a long name used for format. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/Calendar#LONG_STANDALONE:kotlin.Int` A style specifier for getDisplayName and getDisplayNames indicating a long name used independently, such as a month name as calendar headers. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/Calendar#MARCH:kotlin.Int` Value of the `https://developer.android.com/reference/kotlin/java/util/Calendar#MONTH:kotlin.Int` field indicating the third month of the year in the Gregorian and Julian calendars. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/Calendar#MAY:kotlin.Int` Value of the `https://developer.android.com/reference/kotlin/java/util/Calendar#MONTH:kotlin.Int` field indicating the fifth month of the year in the Gregorian and Julian calendars. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/Calendar#MILLISECOND:kotlin.Int` Field number for `get` and `set` indicating the millisecond within the second. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/Calendar#MINUTE:kotlin.Int` Field number for `get` and `set` indicating the minute within the hour. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/Calendar#MONDAY:kotlin.Int` Value of the `https://developer.android.com/reference/kotlin/java/util/Calendar#DAY_OF_WEEK:kotlin.Int` field indicating Monday. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/Calendar#MONTH:kotlin.Int` Field number for `get` and `set` indicating the month. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/Calendar#NARROW_FORMAT:kotlin.Int` A style specifier for getDisplayName and getDisplayNames indicating a narrow name used for format. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/Calendar#NARROW_STANDALONE:kotlin.Int` A style specifier for getDisplayName and getDisplayNames indicating a narrow name independently. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/Calendar#NOVEMBER:kotlin.Int` Value of the `https://developer.android.com/reference/kotlin/java/util/Calendar#MONTH:kotlin.Int` field indicating the eleventh month of the year in the Gregorian and Julian calendars. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/Calendar#OCTOBER:kotlin.Int` Value of the `https://developer.android.com/reference/kotlin/java/util/Calendar#MONTH:kotlin.Int` field indicating the tenth month of the year in the Gregorian and Julian calendars. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/Calendar#PM:kotlin.Int` Value of the `https://developer.android.com/reference/kotlin/java/util/Calendar#AM_PM:kotlin.Int` field indicating the period of the day from noon to just before midnight. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/Calendar#SATURDAY:kotlin.Int` Value of the `https://developer.android.com/reference/kotlin/java/util/Calendar#DAY_OF_WEEK:kotlin.Int` field indicating Saturday. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/Calendar#SECOND:kotlin.Int` Field number for `get` and `set` indicating the second within the minute. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/Calendar#SEPTEMBER:kotlin.Int` Value of the `https://developer.android.com/reference/kotlin/java/util/Calendar#MONTH:kotlin.Int` field indicating the ninth month of the year in the Gregorian and Julian calendars. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/Calendar#SHORT:kotlin.Int` A style specifier for getDisplayName and getDisplayNames equivalent to `https://developer.android.com/reference/kotlin/java/util/Calendar#SHORT_FORMAT:kotlin.Int`. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/Calendar#SHORT_FORMAT:kotlin.Int` A style specifier for getDisplayName and getDisplayNames indicating a short name used for format. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/Calendar#SHORT_STANDALONE:kotlin.Int` A style specifier for getDisplayName and getDisplayNames indicating a short name used independently, such as a month abbreviation as calendar headers. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/Calendar#SUNDAY:kotlin.Int` Value of the `https://developer.android.com/reference/kotlin/java/util/Calendar#DAY_OF_WEEK:kotlin.Int` field indicating Sunday. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/Calendar#THURSDAY:kotlin.Int` Value of the `https://developer.android.com/reference/kotlin/java/util/Calendar#DAY_OF_WEEK:kotlin.Int` field indicating Thursday. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/Calendar#TUESDAY:kotlin.Int` Value of the `https://developer.android.com/reference/kotlin/java/util/Calendar#DAY_OF_WEEK:kotlin.Int` field indicating Tuesday. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/Calendar#UNDECIMBER:kotlin.Int` Value of the `https://developer.android.com/reference/kotlin/java/util/Calendar#MONTH:kotlin.Int` field indicating the thirteenth month of the year. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/Calendar#WEDNESDAY:kotlin.Int` Value of the `https://developer.android.com/reference/kotlin/java/util/Calendar#DAY_OF_WEEK:kotlin.Int` field indicating Wednesday. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/Calendar#WEEK_OF_MONTH:kotlin.Int` Field number for `get` and `set` indicating the week number within the current month. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/Calendar#WEEK_OF_YEAR:kotlin.Int` Field number for `get` and `set` indicating the week number within the current year. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/Calendar#YEAR:kotlin.Int` Field number for `get` and `set` indicating the year. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/Calendar#ZONE_OFFSET:kotlin.Int` Field number for `get` and `set` indicating the raw offset from GMT in milliseconds. |

| Protected constructors ||
|---|---|
| Calendar Constructs a Calendar with the default time zone and the default `https://developer.android.com/reference/kotlin/java/util/Locale.Category` locale. |
| Calendar Constructs a calendar with the specified time zone and locale. |

| Public methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | add Adds or subtracts the specified amount of time to the given calendar field, based on the calendar's rules. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | after Returns whether this `Calendar` represents a time after the time represented by the specified `Object`. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | before Returns whether this `Calendar` represents a time before the time represented by the specified `Object`. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | clear Sets all the calendar field values and the time value (millisecond offset from the [Epoch](Calendar.md)) of this `Calendar` undefined. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | clear Sets the given calendar field value and the time value (millisecond offset from the [Epoch](Calendar.md)) of this `Calendar` undefined. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | clone Creates and returns a copy of this object. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | compareTo Compares the time values (millisecond offsets from the [Epoch](Calendar.md)) represented by two `Calendar` objects. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | equals Compares this `Calendar` to the specified `Object`. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | get Returns the value of the given calendar field. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getActualMaximum Returns the maximum value that the specified calendar field could have, given the time value of this `Calendar`. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getActualMinimum Returns the minimum value that the specified calendar field could have, given the time value of this `Calendar`. |
| open static [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | getAvailableCalendarTypes Returns an unmodifiable `Set` containing all calendar types supported by `Calendar` in the runtime environment. |
| --- | --- |
| open static [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Locale](Locale.md)!\> | getAvailableLocales Returns an array of all locales for which the `getInstance` methods of this class can return localized instances. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | getCalendarType Returns the calendar type of this `Calendar`. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | getDisplayName Returns the string representation of the calendar `field` value in the given `style` and `locale`. |
| --- | --- |
| open [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\>? | getDisplayNames Returns a `Map` containing all names of the calendar `field` in the given `style` and `locale` and their corresponding field values. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getFirstDayOfWeek Gets what the first day of the week is; e. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getGreatestMinimum Returns the highest minimum value for the given calendar field of this `Calendar` instance. |
| --- | --- |
| open static [Calendar](Calendar.md) | getInstance Gets a calendar using the default time zone and locale. |
| open static [Calendar](Calendar.md) | getInstance Gets a calendar using the default time zone and specified locale. |
| open static [Calendar](Calendar.md) | getInstance Gets a calendar using the specified time zone and default locale. |
| --- | --- |
| open static [Calendar](Calendar.md) | getInstance Gets a calendar with the specified time zone and locale. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getLeastMaximum Returns the lowest maximum value for the given calendar field of this `Calendar` instance. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getMaximum Returns the maximum value for the given calendar field of this `Calendar` instance. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getMinimalDaysInFirstWeek Gets what the minimal days required in the first week of the year are; e. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getMinimum Returns the minimum value for the given calendar field of this `Calendar` instance. |
| [Date](Date.md) | getTime Returns a `Date` object representing this `Calendar`'s time value (millisecond offset from the [Epoch](Calendar.md)"). |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | getTimeInMillis Returns this Calendar's time value in milliseconds. |
| open [TimeZone](TimeZone.md) | getTimeZone Gets the time zone. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getWeekYear Returns the week year represented by this `Calendar`. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getWeeksInWeekYear Returns the number of weeks in the week year represented by this `Calendar`. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | hashCode Returns a hash code for this calendar. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isLenient Tells whether date/time interpretation is to be lenient. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isSet Determines if the given calendar field has a value set, including cases that the value has been set by internal fields calculations triggered by a `get` method call. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isWeekDateSupported Returns whether this `Calendar` supports week dates. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | roll Adds or subtracts (up/down) a single unit of time on the given time field without changing larger fields. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | roll Adds the specified (signed) amount to the specified calendar field without changing larger fields. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | set Sets the given calendar field to the given value. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | set Sets the values for the calendar fields `YEAR`, `MONTH`, and `DAY_OF_MONTH`. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | set Sets the values for the calendar fields `YEAR`, `MONTH`, `DAY_OF_MONTH`, `HOUR_OF_DAY`, and `MINUTE`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | set Sets the values for the fields `YEAR`, `MONTH`, `DAY_OF_MONTH`, `HOUR_OF_DAY`, `MINUTE`, and `SECOND`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setFirstDayOfWeek Sets what the first day of the week is; e. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setLenient Specifies whether or not date/time interpretation is to be lenient. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setMinimalDaysInFirstWeek Sets what the minimal days required in the first week of the year are; For example, if the first week is defined as one that contains the first day of the first month of a year, call this method with value 1. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setTime Sets this Calendar's time with the given `Date`. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setTimeInMillis Sets this Calendar's current time from the given long value. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setTimeZone Sets the time zone with the given time zone value. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setWeekDate Sets the date of this `Calendar` with the given date specifiers - week year, week of year, and day of week. |
| --- | --- |
| [Instant](../java.time/Instant.md) | toInstant Converts this object to an `https://developer.android.com/reference/kotlin/java/time/Instant.html#`. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | toString Return a string representation of this calendar. |

| Protected methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | complete Fills in any unset fields in the calendar fields. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | computeFields Converts the current millisecond time value `https://developer.android.com/reference/kotlin/java/util/Calendar#time:kotlin.Long` to calendar field values in `https://developer.android.com/reference/kotlin/java/util/Calendar#fields:kotlin.IntArray`. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | computeTime Converts the current calendar field values in `https://developer.android.com/reference/kotlin/java/util/Calendar#fields:kotlin.IntArray` to the millisecond time value `https://developer.android.com/reference/kotlin/java/util/Calendar#time:kotlin.Long`. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | internalGet Returns the value of the given calendar field. |

| Properties ||
|---|---|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/Calendar#areFieldsSet:kotlin.Boolean` True if `fields[]` are in sync with the currently set time. |
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | `https://developer.android.com/reference/kotlin/java/util/Calendar#fields:kotlin.IntArray` The calendar field values for the currently set time for this calendar. |
| [BooleanArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html) | `https://developer.android.com/reference/kotlin/java/util/Calendar#isSet:kotlin.BooleanArray` The flags which tell if a specified calendar field for the calendar is set. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/Calendar#isTimeSet:kotlin.Boolean` True if then the value of `time` is valid. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/util/Calendar#time:kotlin.Long` The currently set time for this calendar, expressed in milliseconds after January 1, 1970, 0:00:00 GMT. |

## Constants

### ALL_STYLES

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ALL_STYLES: Int
```

A style specifier for getDisplayNames indicating names in all styles, such as "January" and "Jan".

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/Calendar#SHORT_FORMAT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/java/util/Calendar#LONG_FORMAT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/java/util/Calendar#SHORT_STANDALONE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/java/util/Calendar#LONG_STANDALONE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/java/util/Calendar#SHORT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/java/util/Calendar#LONG:kotlin.Int`

### AM

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AM: Int
```

Value of the `https://developer.android.com/reference/kotlin/java/util/Calendar#AM_PM:kotlin.Int` field indicating the period of the day from midnight to just before noon.

 Value: 0

### AM_PM

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AM_PM: Int
```

Field number for `get` and `set` indicating whether the `HOUR` is before or after noon. E.g., at 10:04:15.250 PM the `AM_PM` is `PM`.

 Value: 9

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/Calendar#AM:kotlin.Int`
- `https://developer.android.com/reference/kotlin/java/util/Calendar#PM:kotlin.Int`
- `https://developer.android.com/reference/kotlin/java/util/Calendar#HOUR:kotlin.Int`

### APRIL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val APRIL: Int
```

Value of the `https://developer.android.com/reference/kotlin/java/util/Calendar#MONTH:kotlin.Int` field indicating the fourth month of the year in the Gregorian and Julian calendars.

 Value: 3

### AUGUST

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUGUST: Int
```

Value of the `https://developer.android.com/reference/kotlin/java/util/Calendar#MONTH:kotlin.Int` field indicating the eighth month of the year in the Gregorian and Julian calendars.

 Value: 7

### DATE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATE: Int
```

Field number for `get` and `set` indicating the day of the month. This is a synonym for `DAY_OF_MONTH`. The first day of the month has value 1.

 Value: 5

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/Calendar#DAY_OF_MONTH:kotlin.Int`

### DAY_OF_MONTH

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DAY_OF_MONTH: Int
```

Field number for `get` and `set` indicating the day of the month. This is a synonym for `DATE`. The first day of the month has value 1.

 Value: 5

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/Calendar#DATE:kotlin.Int`

### DAY_OF_WEEK

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DAY_OF_WEEK: Int
```

Field number for `get` and `set` indicating the day of the week. This field takes values `SUNDAY`, `MONDAY`, `TUESDAY`, `WEDNESDAY`, `THURSDAY`, `FRIDAY`, and `SATURDAY`.

 Value: 7

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/Calendar#SUNDAY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/java/util/Calendar#MONDAY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/java/util/Calendar#TUESDAY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/java/util/Calendar#WEDNESDAY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/java/util/Calendar#THURSDAY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/java/util/Calendar#FRIDAY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/java/util/Calendar#SATURDAY:kotlin.Int`

### DAY_OF_WEEK_IN_MONTH

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DAY_OF_WEEK_IN_MONTH: Int
```

Field number for `get` and `set` indicating the ordinal number of the day of the week within the current month. Together with the `DAY_OF_WEEK` field, this uniquely specifies a day within a month. Unlike `WEEK_OF_MONTH` and `WEEK_OF_YEAR`, this field's value does *not* depend on `getFirstDayOfWeek()` or `getMinimalDaysInFirstWeek()`. `DAY_OF_MONTH 1` through `7` always correspond to `DAY_OF_WEEK_IN_MONTH 1`; `8` through `14` correspond to `DAY_OF_WEEK_IN_MONTH 2`, and so on. `DAY_OF_WEEK_IN_MONTH 0` indicates the week before `DAY_OF_WEEK_IN_MONTH 1`. Negative values count back from the end of the month, so the last Sunday of a month is specified as `DAY_OF_WEEK = SUNDAY, DAY_OF_WEEK_IN_MONTH = -1`. Because negative values count backward they will usually be aligned differently within the month than positive values. For example, if a month has 31 days, `DAY_OF_WEEK_IN_MONTH -1` will overlap `DAY_OF_WEEK_IN_MONTH 5` and the end of `4`.

 Value: 8

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/Calendar#DAY_OF_WEEK:kotlin.Int`
- `https://developer.android.com/reference/kotlin/java/util/Calendar#WEEK_OF_MONTH:kotlin.Int`

### DAY_OF_YEAR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DAY_OF_YEAR: Int
```

Field number for `get` and `set` indicating the day number within the current year. The first day of the year has value 1.

 Value: 6

### DECEMBER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DECEMBER: Int
```

Value of the `https://developer.android.com/reference/kotlin/java/util/Calendar#MONTH:kotlin.Int` field indicating the twelfth month of the year in the Gregorian and Julian calendars.

 Value: 11

### DST_OFFSET

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DST_OFFSET: Int
```

Field number for `get` and `set` indicating the daylight saving offset in milliseconds.

This field reflects the correct daylight saving offset value of the time zone of this `Calendar` if the `TimeZone` implementation subclass supports historical Daylight Saving Time schedule changes.

 Value: 16

### ERA

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERA: Int
```

Field number for `get` and `set` indicating the era, e.g., AD or BC in the Julian calendar. This is a calendar-specific value; see subclass documentation.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#AD:kotlin.Int`
- `https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#BC:kotlin.Int`

### FEBRUARY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEBRUARY: Int
```

Value of the `https://developer.android.com/reference/kotlin/java/util/Calendar#MONTH:kotlin.Int` field indicating the second month of the year in the Gregorian and Julian calendars.

 Value: 1

### FIELD_COUNT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FIELD_COUNT: Int
```

The number of distinct fields recognized by `get` and `set`. Field numbers range from `0..FIELD_COUNT-1`.

 Value: 17

### FRIDAY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FRIDAY: Int
```

Value of the `https://developer.android.com/reference/kotlin/java/util/Calendar#DAY_OF_WEEK:kotlin.Int` field indicating Friday.

 Value: 6

### HOUR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HOUR: Int
```

Field number for `get` and `set` indicating the hour of the morning or afternoon. `HOUR` is used for the 12-hour clock (0 - 11). Noon and midnight are represented by 0, not by 12. E.g., at 10:04:15.250 PM the `HOUR` is 10.

 Value: 10

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/Calendar#AM_PM:kotlin.Int`
- `https://developer.android.com/reference/kotlin/java/util/Calendar#HOUR_OF_DAY:kotlin.Int`

### HOUR_OF_DAY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HOUR_OF_DAY: Int
```

Field number for `get` and `set` indicating the hour of the day. `HOUR_OF_DAY` is used for the 24-hour clock. E.g., at 10:04:15.250 PM the `HOUR_OF_DAY` is 22.

 Value: 11

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/Calendar#HOUR:kotlin.Int`

### JANUARY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val JANUARY: Int
```

Value of the `https://developer.android.com/reference/kotlin/java/util/Calendar#MONTH:kotlin.Int` field indicating the first month of the year in the Gregorian and Julian calendars.

 Value: 0

### JULY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val JULY: Int
```

Value of the `https://developer.android.com/reference/kotlin/java/util/Calendar#MONTH:kotlin.Int` field indicating the seventh month of the year in the Gregorian and Julian calendars.

 Value: 6

### JUNE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val JUNE: Int
```

Value of the `https://developer.android.com/reference/kotlin/java/util/Calendar#MONTH:kotlin.Int` field indicating the sixth month of the year in the Gregorian and Julian calendars.

 Value: 5

### LONG

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LONG: Int
```

A style specifier for getDisplayName and getDisplayNames equivalent to `https://developer.android.com/reference/kotlin/java/util/Calendar#LONG_FORMAT:kotlin.Int`.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/Calendar#LONG_STANDALONE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/java/util/Calendar#SHORT:kotlin.Int`

### LONG_FORMAT

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LONG_FORMAT: Int
```

A style specifier for getDisplayName and getDisplayNames indicating a long name used for format.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/Calendar#LONG_STANDALONE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/java/util/Calendar#SHORT_FORMAT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/java/util/Calendar#SHORT_STANDALONE:kotlin.Int`

### LONG_STANDALONE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LONG_STANDALONE: Int
```

A style specifier for getDisplayName and getDisplayNames indicating a long name used independently, such as a month name as calendar headers.

 Value: 32770

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/Calendar#LONG_FORMAT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/java/util/Calendar#SHORT_FORMAT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/java/util/Calendar#SHORT_STANDALONE:kotlin.Int`

### MARCH

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MARCH: Int
```

Value of the `https://developer.android.com/reference/kotlin/java/util/Calendar#MONTH:kotlin.Int` field indicating the third month of the year in the Gregorian and Julian calendars.

 Value: 2

### MAY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MAY: Int
```

Value of the `https://developer.android.com/reference/kotlin/java/util/Calendar#MONTH:kotlin.Int` field indicating the fifth month of the year in the Gregorian and Julian calendars.

 Value: 4

### MILLISECOND

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MILLISECOND: Int
```

Field number for `get` and `set` indicating the millisecond within the second. E.g., at 10:04:15.250 PM the `MILLISECOND` is 250.

 Value: 14

### MINUTE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MINUTE: Int
```

Field number for `get` and `set` indicating the minute within the hour. E.g., at 10:04:15.250 PM the `MINUTE` is 4.

 Value: 12

### MONDAY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MONDAY: Int
```

Value of the `https://developer.android.com/reference/kotlin/java/util/Calendar#DAY_OF_WEEK:kotlin.Int` field indicating Monday.

 Value: 2

### MONTH

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MONTH: Int
```

Field number for `get` and `set` indicating the month. This is a calendar-specific value. The first month of the year in the Gregorian and Julian calendars is `JANUARY` which is 0; the last depends on the number of months in a year.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/Calendar#JANUARY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/java/util/Calendar#FEBRUARY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/java/util/Calendar#MARCH:kotlin.Int`
- `https://developer.android.com/reference/kotlin/java/util/Calendar#APRIL:kotlin.Int`
- `https://developer.android.com/reference/kotlin/java/util/Calendar#MAY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/java/util/Calendar#JUNE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/java/util/Calendar#JULY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/java/util/Calendar#AUGUST:kotlin.Int`
- `https://developer.android.com/reference/kotlin/java/util/Calendar#SEPTEMBER:kotlin.Int`
- `https://developer.android.com/reference/kotlin/java/util/Calendar#OCTOBER:kotlin.Int`
- `https://developer.android.com/reference/kotlin/java/util/Calendar#NOVEMBER:kotlin.Int`
- `https://developer.android.com/reference/kotlin/java/util/Calendar#DECEMBER:kotlin.Int`
- `https://developer.android.com/reference/kotlin/java/util/Calendar#UNDECIMBER:kotlin.Int`

### NARROW_FORMAT

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NARROW_FORMAT: Int
```

A style specifier for getDisplayName and getDisplayNames indicating a narrow name used for format. Narrow names are typically single character strings, such as "M" for Monday.

 Value: 4

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/Calendar#NARROW_STANDALONE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/java/util/Calendar#SHORT_FORMAT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/java/util/Calendar#LONG_FORMAT:kotlin.Int`

### NARROW_STANDALONE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NARROW_STANDALONE: Int
```

A style specifier for getDisplayName and getDisplayNames indicating a narrow name independently. Narrow names are typically single character strings, such as "M" for Monday.

 Value: 32772

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/Calendar#NARROW_FORMAT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/java/util/Calendar#SHORT_STANDALONE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/java/util/Calendar#LONG_STANDALONE:kotlin.Int`

### NOVEMBER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NOVEMBER: Int
```

Value of the `https://developer.android.com/reference/kotlin/java/util/Calendar#MONTH:kotlin.Int` field indicating the eleventh month of the year in the Gregorian and Julian calendars.

 Value: 10

### OCTOBER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OCTOBER: Int
```

Value of the `https://developer.android.com/reference/kotlin/java/util/Calendar#MONTH:kotlin.Int` field indicating the tenth month of the year in the Gregorian and Julian calendars.

 Value: 9

### PM

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PM: Int
```

Value of the `https://developer.android.com/reference/kotlin/java/util/Calendar#AM_PM:kotlin.Int` field indicating the period of the day from noon to just before midnight.

 Value: 1

### SATURDAY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SATURDAY: Int
```

Value of the `https://developer.android.com/reference/kotlin/java/util/Calendar#DAY_OF_WEEK:kotlin.Int` field indicating Saturday.

 Value: 7

### SECOND

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SECOND: Int
```

Field number for `get` and `set` indicating the second within the minute. E.g., at 10:04:15.250 PM the `SECOND` is 15.

 Value: 13

### SEPTEMBER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SEPTEMBER: Int
```

Value of the `https://developer.android.com/reference/kotlin/java/util/Calendar#MONTH:kotlin.Int` field indicating the ninth month of the year in the Gregorian and Julian calendars.

 Value: 8

### SHORT

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SHORT: Int
```

A style specifier for getDisplayName and getDisplayNames equivalent to `https://developer.android.com/reference/kotlin/java/util/Calendar#SHORT_FORMAT:kotlin.Int`.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/Calendar#SHORT_STANDALONE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/java/util/Calendar#LONG:kotlin.Int`

### SHORT_FORMAT

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SHORT_FORMAT: Int
```

A style specifier for getDisplayName and getDisplayNames indicating a short name used for format.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/Calendar#SHORT_STANDALONE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/java/util/Calendar#LONG_FORMAT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/java/util/Calendar#LONG_STANDALONE:kotlin.Int`

### SHORT_STANDALONE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SHORT_STANDALONE: Int
```

A style specifier for getDisplayName and getDisplayNames indicating a short name used independently, such as a month abbreviation as calendar headers.

 Value: 32769

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/Calendar#SHORT_FORMAT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/java/util/Calendar#LONG_FORMAT:kotlin.Int`
- `https://developer.android.com/reference/kotlin/java/util/Calendar#LONG_STANDALONE:kotlin.Int`

### SUNDAY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SUNDAY: Int
```

Value of the `https://developer.android.com/reference/kotlin/java/util/Calendar#DAY_OF_WEEK:kotlin.Int` field indicating Sunday.

 Value: 1

### THURSDAY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val THURSDAY: Int
```

Value of the `https://developer.android.com/reference/kotlin/java/util/Calendar#DAY_OF_WEEK:kotlin.Int` field indicating Thursday.

 Value: 5

### TUESDAY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TUESDAY: Int
```

Value of the `https://developer.android.com/reference/kotlin/java/util/Calendar#DAY_OF_WEEK:kotlin.Int` field indicating Tuesday.

 Value: 3

### UNDECIMBER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UNDECIMBER: Int
```

Value of the `https://developer.android.com/reference/kotlin/java/util/Calendar#MONTH:kotlin.Int` field indicating the thirteenth month of the year. Although `GregorianCalendar` does not use this value, lunar calendars do.

 Value: 12

### WEDNESDAY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WEDNESDAY: Int
```

Value of the `https://developer.android.com/reference/kotlin/java/util/Calendar#DAY_OF_WEEK:kotlin.Int` field indicating Wednesday.

 Value: 4

### WEEK_OF_MONTH

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WEEK_OF_MONTH: Int
```

Field number for `get` and `set` indicating the week number within the current month. The first week of the month, as defined by `getFirstDayOfWeek()` and `getMinimalDaysInFirstWeek()`, has value 1. Subclasses define the value of `WEEK_OF_MONTH` for days before the first week of the month.

 Value: 4

**See Also**

- getFirstDayOfWeek
- getMinimalDaysInFirstWeek

### WEEK_OF_YEAR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WEEK_OF_YEAR: Int
```

Field number for `get` and `set` indicating the week number within the current year. The first week of the year, as defined by `getFirstDayOfWeek()` and `getMinimalDaysInFirstWeek()`, has value 1. Subclasses define the value of `WEEK_OF_YEAR` for days before the first week of the year.

 Value: 3

**See Also**

- getFirstDayOfWeek
- getMinimalDaysInFirstWeek

### YEAR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val YEAR: Int
```

Field number for `get` and `set` indicating the year. This is a calendar-specific value; see subclass documentation.

 Value: 1

### ZONE_OFFSET

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ZONE_OFFSET: Int
```

Field number for `get` and `set` indicating the raw offset from GMT in milliseconds.

This field reflects the correct GMT offset value of the time zone of this `Calendar` if the `TimeZone` implementation subclass supports historical GMT offset changes.

 Value: 15

## Protected constructors

### Calendar

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected Calendar()
```

Constructs a Calendar with the default time zone and the default `https://developer.android.com/reference/kotlin/java/util/Locale.Category` locale.
**See Also**

- getDefault

### Calendar

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected Calendar(
    zone: TimeZone, 
    aLocale: Locale)
```

Constructs a calendar with the specified time zone and locale.

| Parameters ||
|---|---|
| `zone` | [TimeZone](TimeZone.md): the time zone to use |
| `aLocale` | [Locale](Locale.md): the locale for the week data |

## Public methods

### add

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun add(
    field: Int, 
    amount: Int
): Unit
```

Adds or subtracts the specified amount of time to the given calendar field, based on the calendar's rules. For example, to subtract 5 days from the current time of the calendar, you can achieve it by calling:

`add(Calendar.DAY_OF_MONTH, -5)`.

| Parameters ||
|---|---|
| `field` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the calendar field. |
| `amount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the amount of date or time to be added to the field. |

**See Also**

- roll
- set

### after

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun after(when: Any?): Boolean
```

Returns whether this `Calendar` represents a time after the time represented by the specified `Object`. This method is equivalent to:

```kotlin
<code>compareTo(when) &gt; 0
  </code>
```
if and only if `when` is a `Calendar` instance. Otherwise, the method returns `false`.

<br />

| Parameters ||
|---|---|
| `when` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?: the `Object` to be compared |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the time of this `Calendar` is after the time represented by `when`; `false` otherwise. |

**See Also**

- compareTo

### before

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun before(when: Any?): Boolean
```

Returns whether this `Calendar` represents a time before the time represented by the specified `Object`. This method is equivalent to:

```kotlin
<code>compareTo(when) &lt; 0
  </code>
```
if and only if `when` is a `Calendar` instance. Otherwise, the method returns `false`.

<br />

| Parameters ||
|---|---|
| `when` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?: the `Object` to be compared |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the time of this `Calendar` is before the time represented by `when`; `false` otherwise. |

**See Also**

- compareTo

### clear

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun clear(): Unit
```

Sets all the calendar field values and the time value (millisecond offset from the [Epoch](Calendar.md)) of this `Calendar` undefined. This means that isSet will return `false` for all the calendar fields, and the date and time calculations will treat the fields as if they had never been set. A `Calendar` implementation class may use its specific default field values for date/time calculations. For example, `GregorianCalendar` uses 1970 if the `YEAR` field value is undefined.
**See Also**

- clear

### clear

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun clear(field: Int): Unit
```

Sets the given calendar field value and the time value (millisecond offset from the [Epoch](Calendar.md)) of this `Calendar` undefined. This means that isSet will return `false`, and the date and time calculations will treat the field as if it had never been set. A `Calendar` implementation class may use the field's specific default value for date and time calculations.

The `https://developer.android.com/reference/kotlin/java/util/Calendar#HOUR_OF_DAY:kotlin.Int`, `https://developer.android.com/reference/kotlin/java/util/Calendar#HOUR:kotlin.Int` and `https://developer.android.com/reference/kotlin/java/util/Calendar#AM_PM:kotlin.Int` fields are handled independently and the [the resolution rule for the time of day](Calendar.md) is applied. Clearing one of the fields doesn't reset the hour of day value of this `Calendar`. Use set to reset the hour value.

| Parameters ||
|---|---|
| `field` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the calendar field to be cleared. |

**See Also**

- clear

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clone(): Any
```

Creates and returns a copy of this object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html` | a copy of this object. |

| Exceptions ||
|---|---|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the `Cloneable` interface. Subclasses that override the `clone` method can also throw this exception to indicate that an instance cannot be cloned. |

### compareTo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun compareTo(other: Calendar): Int
```

Compares the time values (millisecond offsets from the [Epoch](Calendar.md)) represented by two `Calendar` objects.

| Parameters ||
|---|---|
| `o` | the object to be compared. |
| `anotherCalendar` | the `Calendar` to be compared. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the value `0` if the time represented by the argument is equal to the time represented by this `Calendar`; a value less than `0` if the time of this `Calendar` is before the time represented by the argument; and a value greater than `0` if the time of this `Calendar` is after the time represented by the argument. |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the specified object's type prevents it from being compared to this object. |
| `java.lang.NullPointerException` | if the specified `Calendar` is `null`. |
| `java.lang.IllegalArgumentException` | if the time value of the specified `Calendar` object can't be obtained due to any invalid calendar values. |
| --- | --- |

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun equals(other: Any?): Boolean
```

Compares this `Calendar` to the specified `Object`. The result is `true` if and only if the argument is a `Calendar` object of the same calendar system that represents the same time value (millisecond offset from the [Epoch](Calendar.md)) under the same `Calendar` parameters as this object.

The `Calendar` parameters are the values represented by the `isLenient`, `getFirstDayOfWeek`, `getMinimalDaysInFirstWeek` and `getTimeZone` methods. If there is any difference in those parameters between the two `Calendar`s, this method returns `false`.

Use the compareTo method to compare only the time values.

| Parameters ||
|---|---|
| `obj` | the object to compare with. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is equal to `obj`; `false` otherwise. |

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun get(field: Int): Int
```

Returns the value of the given calendar field. In lenient mode, all calendar fields are normalized. In non-lenient mode, all calendar fields are validated and this method throws an exception if any calendar fields have out-of-range values. The normalization and validation are handled by the complete method, which process is calendar system dependent.

| Parameters ||
|---|---|
| `field` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the given calendar field. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the value for the given calendar field. |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if the specified field is out of range (`field < 0 || field >= FIELD_COUNT`). |

**See Also**

- set
- complete

### getActualMaximum

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getActualMaximum(field: Int): Int
```

Returns the maximum value that the specified calendar field could have, given the time value of this `Calendar`. For example, the actual maximum value of the `MONTH` field is 12 in some years, and 13 in other years in the Hebrew calendar system.

The default implementation of this method uses an iterative algorithm to determine the actual maximum value for the calendar field. Subclasses should, if possible, override this with a more efficient implementation.

| Parameters ||
|---|---|
| `field` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the calendar field |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the maximum of the given calendar field for the time value of this `Calendar` |

**See Also**

- getMinimum
- getMaximum
- getGreatestMinimum
- getLeastMaximum
- getActualMinimum

### getActualMinimum

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getActualMinimum(field: Int): Int
```

Returns the minimum value that the specified calendar field could have, given the time value of this `Calendar`.

The default implementation of this method uses an iterative algorithm to determine the actual minimum value for the calendar field. Subclasses should, if possible, override this with a more efficient implementation - in many cases, they can simply return `getMinimum()`.

| Parameters ||
|---|---|
| `field` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the calendar field |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the minimum of the given calendar field for the time value of this `Calendar` |

**See Also**

- getMinimum
- getMaximum
- getGreatestMinimum
- getLeastMaximum
- getActualMaximum

### getAvailableCalendarTypes

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getAvailableCalendarTypes(): MutableSet<String!>
```

Returns an unmodifiable `Set` containing all calendar types supported by `Calendar` in the runtime environment. The available calendar types can be used for the [Unicode locale extensions](Locale.md). The `Set` returned contains at least `"gregory"`. The calendar types don't include aliases, such as `"gregorian"` for `"gregory"`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>` | an unmodifiable `Set` containing all available calendar types |

**See Also**

- getCalendarType
- setCalendarType
- getUnicodeLocaleType

### getAvailableLocales

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getAvailableLocales(): Array<Locale!>
```

Returns an array of all locales for which the `getInstance` methods of this class can return localized instances. The array returned must contain at least a `Locale` instance equal to `https://developer.android.com/reference/kotlin/java/util/Locale#US:java.util.Locale`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/util/Locale!>` | An array of locales for which localized `Calendar` instances are available. |

### getCalendarType

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCalendarType(): String
```

Returns the calendar type of this `Calendar`. Calendar types are defined by the *Unicode Locale Data Markup Language (LDML)* specification.

The default implementation of this method returns the class name of this `Calendar` instance. Any subclasses that implement LDML-defined calendar systems should override this method to return appropriate calendar types.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | the LDML-defined calendar type or the class name of this `Calendar` instance |

**See Also**

- setLocale
- setUnicodeLocaleKeyword

### getDisplayName

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDisplayName(
    field: Int, 
    style: Int, 
    locale: Locale
): String?
```

Returns the string representation of the calendar `field` value in the given `style` and `locale`. If no string representation is applicable, `null` is returned. This method calls get to get the calendar `field` value if the string representation is applicable to the given calendar `field`.

For example, if this `Calendar` is a `GregorianCalendar` and its date is 2005-01-01, then the string representation of the `https://developer.android.com/reference/kotlin/java/util/Calendar#MONTH:kotlin.Int` field would be "January" in the long style in an English locale or "Jan" in the short style. However, no string representation would be available for the `https://developer.android.com/reference/kotlin/java/util/Calendar#DAY_OF_MONTH:kotlin.Int` field, and this method would return `null`.

The default implementation supports the calendar fields for which a `https://developer.android.com/reference/kotlin/java/text/DateFormatSymbols.html#` has names in the given `locale`.

| Parameters ||
|---|---|
| `field` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the calendar field for which the string representation is returned |
| `style` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the style applied to the string representation; one of `https://developer.android.com/reference/kotlin/java/util/Calendar#SHORT_FORMAT:kotlin.Int` (`https://developer.android.com/reference/kotlin/java/util/Calendar#SHORT:kotlin.Int`), `https://developer.android.com/reference/kotlin/java/util/Calendar#SHORT_STANDALONE:kotlin.Int`, `https://developer.android.com/reference/kotlin/java/util/Calendar#LONG_FORMAT:kotlin.Int` (`https://developer.android.com/reference/kotlin/java/util/Calendar#LONG:kotlin.Int`), `https://developer.android.com/reference/kotlin/java/util/Calendar#LONG_STANDALONE:kotlin.Int`, `https://developer.android.com/reference/kotlin/java/util/Calendar#NARROW_FORMAT:kotlin.Int`, or `https://developer.android.com/reference/kotlin/java/util/Calendar#NARROW_STANDALONE:kotlin.Int`. |
| `locale` | [Locale](Locale.md): the locale for the string representation (any calendar types specified by `locale` are ignored) |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | the string representation of the given `field` in the given `style`, or `null` if no string representation is applicable. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `field` or `style` is invalid, or if this `Calendar` is non-lenient and any of the calendar fields have invalid values |
| `java.lang.NullPointerException` | if `locale` is null |

### getDisplayNames

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDisplayNames(
    field: Int, 
    style: Int, 
    locale: Locale
): MutableMap<String!, Int!>?
```

Returns a `Map` containing all names of the calendar `field` in the given `style` and `locale` and their corresponding field values. For example, if this `Calendar` is a GregorianCalendar, the returned map would contain "Jan" to `https://developer.android.com/reference/kotlin/java/util/Calendar#JANUARY:kotlin.Int`, "Feb" to `https://developer.android.com/reference/kotlin/java/util/Calendar#FEBRUARY:kotlin.Int`, and so on, in the [short](Calendar.md) style in an English locale.

Narrow names may not be unique due to use of single characters, such as "S" for Sunday and Saturday. In that case narrow names are not included in the returned `Map`.

The values of other calendar fields may be taken into account to determine a set of display names. For example, if this `Calendar` is a lunisolar calendar system and the year value given by the `https://developer.android.com/reference/kotlin/java/util/Calendar#YEAR:kotlin.Int` field has a leap month, this method would return month names containing the leap month name, and month names are mapped to their values specific for the year.

The default implementation supports display names contained in a `https://developer.android.com/reference/kotlin/java/text/DateFormatSymbols.html#`. For example, if `field` is `https://developer.android.com/reference/kotlin/java/util/Calendar#MONTH:kotlin.Int` and `style` is `https://developer.android.com/reference/kotlin/java/util/Calendar#ALL_STYLES:kotlin.Int`, this method returns a `Map` containing all strings returned by getShortMonths and getMonths.

| Parameters ||
|---|---|
| `field` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the calendar field for which the display names are returned |
| `style` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the style applied to the string representation; one of `https://developer.android.com/reference/kotlin/java/util/Calendar#SHORT_FORMAT:kotlin.Int` (`https://developer.android.com/reference/kotlin/java/util/Calendar#SHORT:kotlin.Int`), `https://developer.android.com/reference/kotlin/java/util/Calendar#SHORT_STANDALONE:kotlin.Int`, `https://developer.android.com/reference/kotlin/java/util/Calendar#LONG_FORMAT:kotlin.Int` (`https://developer.android.com/reference/kotlin/java/util/Calendar#LONG:kotlin.Int`), `https://developer.android.com/reference/kotlin/java/util/Calendar#LONG_STANDALONE:kotlin.Int`, `https://developer.android.com/reference/kotlin/java/util/Calendar#NARROW_FORMAT:kotlin.Int`, or `https://developer.android.com/reference/kotlin/java/util/Calendar#NARROW_STANDALONE:kotlin.Int` |
| `locale` | [Locale](Locale.md): the locale for the display names |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!>?` | a `Map` containing all display names in `style` and `locale` and their field values, or `null` if no display names are defined for `field` |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `field` or `style` is invalid, or if this `Calendar` is non-lenient and any of the calendar fields have invalid values |
| `java.lang.NullPointerException` | if `locale` is null |

### getFirstDayOfWeek

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getFirstDayOfWeek(): Int
```

Gets what the first day of the week is; e.g., `SUNDAY` in the U.S., `MONDAY` in France.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the first day of the week. |

**See Also**

- setFirstDayOfWeek
- getMinimalDaysInFirstWeek

### getGreatestMinimum

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getGreatestMinimum(field: Int): Int
```

Returns the highest minimum value for the given calendar field of this `Calendar` instance. The highest minimum value is defined as the largest value returned by getActualMinimum for any possible time value. The greatest minimum value depends on calendar system specific parameters of the instance.

| Parameters ||
|---|---|
| `field` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the calendar field. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the highest minimum value for the given calendar field. |

**See Also**

- getMinimum
- getMaximum
- getLeastMaximum
- getActualMinimum
- getActualMaximum

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getInstance(): Calendar
```

Gets a calendar using the default time zone and locale. The `Calendar` returned is based on the current time in the default time zone with the default `https://developer.android.com/reference/kotlin/java/util/Locale.Category` locale.

Since Android 13, if the locale contains the time zone with "tz" [Unicode extension](Locale.md), that time zone is used instead.

| Return ||
|---|---|
| Calendar | a Calendar. |

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getInstance(aLocale: Locale): Calendar
```

Gets a calendar using the default time zone and specified locale. The `Calendar` returned is based on the current time in the default time zone with the given locale.

Since Android 13, if the locale contains the time zone with "tz" [Unicode extension](Locale.md), that time zone is used instead.

| Parameters ||
|---|---|
| `aLocale` | [Locale](Locale.md): the locale for the week data |

| Return ||
|---|---|
| Calendar | a Calendar. |

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getInstance(zone: TimeZone): Calendar
```

Gets a calendar using the specified time zone and default locale. The `Calendar` returned is based on the current time in the given time zone with the default `https://developer.android.com/reference/kotlin/java/util/Locale.Category` locale.

| Parameters ||
|---|---|
| `zone` | [TimeZone](TimeZone.md): the time zone to use |

| Return ||
|---|---|
| Calendar | a Calendar. |

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getInstance(
    zone: TimeZone, 
    aLocale: Locale
): Calendar
```

Gets a calendar with the specified time zone and locale. The `Calendar` returned is based on the current time in the given time zone with the given locale.

| Parameters ||
|---|---|
| `zone` | [TimeZone](TimeZone.md): the time zone to use |
| `aLocale` | [Locale](Locale.md): the locale for the week data |

| Return ||
|---|---|
| Calendar | a Calendar. |

### getLeastMaximum

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getLeastMaximum(field: Int): Int
```

Returns the lowest maximum value for the given calendar field of this `Calendar` instance. The lowest maximum value is defined as the smallest value returned by getActualMaximum for any possible time value. The least maximum value depends on calendar system specific parameters of the instance. For example, a `Calendar` for the Gregorian calendar system returns 28 for the `DAY_OF_MONTH` field, because the 28th is the last day of the shortest month of this calendar, February in a common year.

| Parameters ||
|---|---|
| `field` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the calendar field. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the lowest maximum value for the given calendar field. |

**See Also**

- getMinimum
- getMaximum
- getGreatestMinimum
- getActualMinimum
- getActualMaximum

### getMaximum

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getMaximum(field: Int): Int
```

Returns the maximum value for the given calendar field of this `Calendar` instance. The maximum value is defined as the largest value returned by the get method for any possible time value. The maximum value depends on calendar system specific parameters of the instance.

| Parameters ||
|---|---|
| `field` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the calendar field. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the maximum value for the given calendar field. |

**See Also**

- getMinimum
- getGreatestMinimum
- getLeastMaximum
- getActualMinimum
- getActualMaximum

### getMinimalDaysInFirstWeek

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMinimalDaysInFirstWeek(): Int
```

Gets what the minimal days required in the first week of the year are; e.g., if the first week is defined as one that contains the first day of the first month of a year, this method returns 1. If the minimal days required must be a full week, this method returns 7.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the minimal days required in the first week of the year. |

**See Also**

- setMinimalDaysInFirstWeek

### getMinimum

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getMinimum(field: Int): Int
```

Returns the minimum value for the given calendar field of this `Calendar` instance. The minimum value is defined as the smallest value returned by the get method for any possible time value. The minimum value depends on calendar system specific parameters of the instance.

| Parameters ||
|---|---|
| `field` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the calendar field. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the minimum value for the given calendar field. |

**See Also**

- getMaximum
- getGreatestMinimum
- getLeastMaximum
- getActualMinimum
- getActualMaximum

### getTime

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTime(): Date
```

Returns a `Date` object representing this `Calendar`'s time value (millisecond offset from the [Epoch](Calendar.md)").

| Return ||
|---|---|
| Date | a `Date` representing the time value. |

**See Also**

- setTime
- getTimeInMillis

### getTimeInMillis

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTimeInMillis(): Long
```

Returns this Calendar's time value in milliseconds.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the current time as UTC milliseconds from the epoch. |

**See Also**

- getTime
- setTimeInMillis

### getTimeZone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTimeZone(): TimeZone
```

Gets the time zone.

| Return ||
|---|---|
| TimeZone | the time zone object associated with this calendar. |

### getWeekYear

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getWeekYear(): Int
```

Returns the week year represented by this `Calendar`. The week year is in sync with the week cycle. The [first day of the first week](Calendar.md)) is the first day of the week year.

The default implementation of this method throws an `https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the week year of this `Calendar` |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | if any week year numbering isn't supported in this `Calendar`. |

**See Also**

- isWeekDateSupported
- getFirstDayOfWeek
- getMinimalDaysInFirstWeek

### getWeeksInWeekYear

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getWeeksInWeekYear(): Int
```

Returns the number of weeks in the week year represented by this `Calendar`.

The default implementation of this method throws an `UnsupportedOperationException`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the number of weeks in the week year. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | if any week year numbering isn't supported in this `Calendar`. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/Calendar#WEEK_OF_YEAR:kotlin.Int`
- isWeekDateSupported
- getWeekYear
- getActualMaximum

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hashCode(): Int
```

Returns a hash code for this calendar.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

### isLenient

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isLenient(): Boolean
```

Tells whether date/time interpretation is to be lenient.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the interpretation mode of this calendar is lenient; `false` otherwise. |

**See Also**

- setLenient

### isSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isSet(field: Int): Boolean
```

Determines if the given calendar field has a value set, including cases that the value has been set by internal fields calculations triggered by a `get` method call.

| Parameters ||
|---|---|
| `field` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the calendar field to test |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the given calendar field has a value set; `false` otherwise. |

### isWeekDateSupported

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isWeekDateSupported(): Boolean
```

Returns whether this `Calendar` supports week dates.

The default implementation of this method returns `false`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this `Calendar` supports week dates; `false` otherwise. |

**See Also**

- getWeekYear
- setWeekDate
- getWeeksInWeekYear

### roll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun roll(
    field: Int, 
    up: Boolean
): Unit
```

Adds or subtracts (up/down) a single unit of time on the given time field without changing larger fields. For example, to roll the current date up by one day, you can achieve it by calling:

roll(Calendar.DATE, true). When rolling on the year or Calendar.YEAR field, it will roll the year value in the range between 1 and the value returned by calling `getMaximum(Calendar.YEAR)`. When rolling on the month or Calendar.MONTH field, other fields like date might conflict and, need to be changed. For instance, rolling the month on the date 01/31/96 will result in 02/29/96. When rolling on the hour-in-day or Calendar.HOUR_OF_DAY field, it will roll the hour value in the range between 0 and 23, which is zero-based.

| Parameters ||
|---|---|
| `field` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the time field. |
| `up` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): indicates if the value of the specified time field is to be rolled up or rolled down. Use true if rolling up, false otherwise. |

**See Also**

- add
- set

### roll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun roll(
    field: Int, 
    amount: Int
): Unit
```

Adds the specified (signed) amount to the specified calendar field without changing larger fields. A negative amount means to roll down.

NOTE: This default implementation on `Calendar` just repeatedly calls the version of roll that rolls by one unit. This may not always do the right thing. For example, if the `DAY_OF_MONTH` field is 31, rolling through February will leave it set to 28. The `GregorianCalendar` version of this function takes care of this problem. Other subclasses should also provide overrides of this function that do the right thing.

| Parameters ||
|---|---|
| `field` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the calendar field. |
| `amount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the signed amount to add to the calendar `field`. |

**See Also**

- roll
- add
- set

### set

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun set(
    field: Int, 
    value: Int
): Unit
```

Sets the given calendar field to the given value. The value is not interpreted by this method regardless of the leniency mode.

| Parameters ||
|---|---|
| `field` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the given calendar field. |
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the value to be set for the given calendar field. |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if the specified field is out of range (`field < 0 || field >= FIELD_COUNT`). in non-lenient mode. |

**See Also**

- set
- set
- set
- get

### set

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun set(
    year: Int, 
    month: Int, 
    date: Int
): Unit
```

Sets the values for the calendar fields `YEAR`, `MONTH`, and `DAY_OF_MONTH`. Previous values of other calendar fields are retained. If this is not desired, call clear first.

| Parameters ||
|---|---|
| `year` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the value used to set the `YEAR` calendar field. |
| `month` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the value used to set the `MONTH` calendar field. Month value is 0-based. e.g., 0 for January. |
| `date` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the value used to set the `DAY_OF_MONTH` calendar field. |
| --- | --- |

**See Also**

- set
- set
- set

### set

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun set(
    year: Int, 
    month: Int, 
    date: Int, 
    hourOfDay: Int, 
    minute: Int
): Unit
```

Sets the values for the calendar fields `YEAR`, `MONTH`, `DAY_OF_MONTH`, `HOUR_OF_DAY`, and `MINUTE`. Previous values of other fields are retained. If this is not desired, call clear first.

| Parameters ||
|---|---|
| `year` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the value used to set the `YEAR` calendar field. |
| `month` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the value used to set the `MONTH` calendar field. Month value is 0-based. e.g., 0 for January. |
| `date` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the value used to set the `DAY_OF_MONTH` calendar field. |
| --- | --- |
| `hourOfDay` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the value used to set the `HOUR_OF_DAY` calendar field. |
| `minute` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the value used to set the `MINUTE` calendar field. |

**See Also**

- set
- set
- set

### set

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun set(
    year: Int, 
    month: Int, 
    date: Int, 
    hourOfDay: Int, 
    minute: Int, 
    second: Int
): Unit
```

Sets the values for the fields `YEAR`, `MONTH`, `DAY_OF_MONTH`, `HOUR_OF_DAY`, `MINUTE`, and `SECOND`. Previous values of other fields are retained. If this is not desired, call clear first.

| Parameters ||
|---|---|
| `year` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the value used to set the `YEAR` calendar field. |
| `month` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the value used to set the `MONTH` calendar field. Month value is 0-based. e.g., 0 for January. |
| `date` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the value used to set the `DAY_OF_MONTH` calendar field. |
| --- | --- |
| `hourOfDay` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the value used to set the `HOUR_OF_DAY` calendar field. |
| `minute` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the value used to set the `MINUTE` calendar field. |
| `second` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the value used to set the `SECOND` calendar field. |
| --- | --- |

**See Also**

- set
- set
- set

### setFirstDayOfWeek

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setFirstDayOfWeek(value: Int): Unit
```

Sets what the first day of the week is; e.g., `SUNDAY` in the U.S., `MONDAY` in France.

| Parameters ||
|---|---|
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the given first day of the week. |

**See Also**

- getFirstDayOfWeek
- getMinimalDaysInFirstWeek

### setLenient

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setLenient(lenient: Boolean): Unit
```

Specifies whether or not date/time interpretation is to be lenient. With lenient interpretation, a date such as "February 942, 1996" will be treated as being equivalent to the 941st day after February 1, 1996. With strict (non-lenient) interpretation, such dates will cause an exception to be thrown. The default is lenient.

| Parameters ||
|---|---|
| `lenient` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): `true` if the lenient mode is to be turned on; `false` if it is to be turned off. |

**See Also**

- isLenient
- setLenient

### setMinimalDaysInFirstWeek

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setMinimalDaysInFirstWeek(value: Int): Unit
```

Sets what the minimal days required in the first week of the year are; For example, if the first week is defined as one that contains the first day of the first month of a year, call this method with value 1. If it must be a full week, use value 7.

| Parameters ||
|---|---|
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the given minimal days required in the first week of the year. |

**See Also**

- getMinimalDaysInFirstWeek

### setTime

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setTime(date: Date): Unit
```

Sets this Calendar's time with the given `Date`.

Note: Calling `setTime()` with `Date(Long.MAX_VALUE)` or `Date(Long.MIN_VALUE)` may yield incorrect field values from `get()`.

| Parameters ||
|---|---|
| `date` | [Date](Date.md): the given Date. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if `date` is `null` |

**See Also**

- getTime
- setTimeInMillis

### setTimeInMillis

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTimeInMillis(millis: Long): Unit
```

Sets this Calendar's current time from the given long value.

| Parameters ||
|---|---|
| `millis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the new time in UTC milliseconds from the epoch. |

**See Also**

- setTime
- getTimeInMillis

### setTimeZone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTimeZone(value: TimeZone): Unit
```

Sets the time zone with the given time zone value.

| Parameters ||
|---|---|
| `value` | [TimeZone](TimeZone.md): the given time zone. |

### setWeekDate

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setWeekDate(
    weekYear: Int, 
    weekOfYear: Int, 
    dayOfWeek: Int
): Unit
```

Sets the date of this `Calendar` with the given date specifiers - week year, week of year, and day of week.

Unlike the `set` method, all of the calendar fields and `time` values are calculated upon return.

If `weekOfYear` is out of the valid week-of-year range in `weekYear`, the `weekYear` and `weekOfYear` values are adjusted in lenient mode, or an `IllegalArgumentException` is thrown in non-lenient mode.

The default implementation of this method throws an `UnsupportedOperationException`.

| Parameters ||
|---|---|
| `weekYear` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the week year |
| `weekOfYear` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the week number based on `weekYear` |
| `dayOfWeek` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the day of week value: one of the constants for the `https://developer.android.com/reference/kotlin/java/util/Calendar#DAY_OF_WEEK:kotlin.Int` field: `https://developer.android.com/reference/kotlin/java/util/Calendar#SUNDAY:kotlin.Int`, ..., `https://developer.android.com/reference/kotlin/java/util/Calendar#SATURDAY:kotlin.Int`. |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if any of the given date specifiers is invalid or any of the calendar fields are inconsistent with the given date specifiers in non-lenient mode |
| `java.lang.UnsupportedOperationException` | if any week year numbering isn't supported in this `Calendar`. |

**See Also**

- isWeekDateSupported
- getFirstDayOfWeek
- getMinimalDaysInFirstWeek

### toInstant

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toInstant(): Instant
```

Converts this object to an `https://developer.android.com/reference/kotlin/java/time/Instant.html#`.

The conversion creates an `Instant` that represents the same point on the time-line as this `Calendar`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/Instant.html#` | the instant representing the same point on the time-line |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Return a string representation of this calendar. This method is intended to be used only for debugging purposes, and the format of the returned string may vary between implementations. The returned string may be empty but may not be `null`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of this calendar. |

## Protected methods

### complete

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun complete(): Unit
```

Fills in any unset fields in the calendar fields. First, the computeTime method is called if the time value (millisecond offset from the [Epoch](Calendar.md)) has not been calculated from calendar field values. Then, the computeFields method is called to calculate all calendar field values.

### computeFields

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected abstract fun computeFields(): Unit
```

Converts the current millisecond time value `https://developer.android.com/reference/kotlin/java/util/Calendar#time:kotlin.Long` to calendar field values in `https://developer.android.com/reference/kotlin/java/util/Calendar#fields:kotlin.IntArray`. This allows you to sync up the calendar field values with a new time that is set for the calendar. The time is *not* recomputed first; to recompute the time, then the fields, call the complete method.
**See Also**

- computeTime

### computeTime

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected abstract fun computeTime(): Unit
```

Converts the current calendar field values in `https://developer.android.com/reference/kotlin/java/util/Calendar#fields:kotlin.IntArray` to the millisecond time value `https://developer.android.com/reference/kotlin/java/util/Calendar#time:kotlin.Long`.
**See Also**

- complete
- computeFields

### internalGet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected fun internalGet(field: Int): Int
```

Returns the value of the given calendar field. This method does not involve normalization or validation of the field value.

| Parameters ||
|---|---|
| `field` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the given calendar field. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the value for the given calendar field. |

**See Also**

- get

## Properties

### areFieldsSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected var areFieldsSet: Boolean
```

True if `fields[]` are in sync with the currently set time. If false, then the next attempt to get the value of a field will force a recomputation of all fields from the current value of `time`.

### fields

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected var fields: IntArray
```

The calendar field values for the currently set time for this calendar. This is an array of `FIELD_COUNT` integers, with index values `ERA` through `DST_OFFSET`.

### isSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected var isSet: BooleanArray
```

The flags which tell if a specified calendar field for the calendar is set. A new object has no fields set. After the first call to a method which generates the fields, they all remain set after that. This is an array of `FIELD_COUNT` booleans, with index values `ERA` through `DST_OFFSET`.

### isTimeSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected var isTimeSet: Boolean
```

True if then the value of `time` is valid. The time is made invalid by a change to an item of `field[]`.
**See Also**

- `https://developer.android.com/reference/kotlin/java/util/Calendar#time:kotlin.Long`

### time

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected var time: Long
```

The currently set time for this calendar, expressed in milliseconds after January 1, 1970, 0:00:00 GMT.
**See Also**

- `https://developer.android.com/reference/kotlin/java/util/Calendar#isTimeSet:kotlin.Boolean`
