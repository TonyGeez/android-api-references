# GregorianCalendar

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GregorianCalendar

```
open class GregorianCalendar : Calendar
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [java.util.Calendar](https://developer.android.com/reference/kotlin/java/util/Calendar) ||
| | ↳ | [java.util.GregorianCalendar](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#) |

`GregorianCalendar`is a concrete subclass of`Calendar`and provides the standard calendar system used by most of the world.

`GregorianCalendar`is a hybrid calendar that supports both the Julian and Gregorian calendar systems with the support of a single discontinuity, which corresponds by default to the Gregorian date when the Gregorian calendar was instituted (October 15, 1582 in some countries, later in others). The cutover date may be changed by the caller by calling [setGregorianChange()](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#setGregorianChange(java.util.Date)).

Historically, in those countries which adopted the Gregorian calendar first, October 4, 1582 (Julian) was thus followed by October 15, 1582 (Gregorian). This calendar models this correctly. Before the Gregorian cutover,`GregorianCalendar`implements the Julian calendar. The only difference between the Gregorian and the Julian calendar is the leap year rule. The Julian calendar specifies leap years every four years, whereas the Gregorian calendar omits century years which are not divisible by 400.

`GregorianCalendar`implements*proleptic* Gregorian and Julian calendars. That is, dates are computed by extrapolating the current rules indefinitely far backward and forward in time. As a result,`GregorianCalendar`may be used for all years to generate meaningful and consistent results. However, dates obtained using`GregorianCalendar`are historically accurate only from March 1, 4 AD onward, when modern Julian calendar rules were adopted. Before this date, leap year rules were applied irregularly, and before 45 BC the Julian calendar did not even exist.

Prior to the institution of the Gregorian calendar, New Year's Day was March 25. To avoid confusion, this calendar always uses January 1. A manual adjustment may be made if desired for dates that are prior to the Gregorian changeover and which fall between January 1 and March 24.

## Week Of Year and Week Year

Values calculated for the [WEEK_OF_YEAR](https://developer.android.com/reference/kotlin/java/util/Calendar#WEEK_OF_YEAR:kotlin.Int) field range from 1 to 53. The first week of a calendar year is the earliest seven day period starting on [getFirstDayOfWeek()](https://developer.android.com/reference/kotlin/java/util/Calendar#getFirstDayOfWeek())that contains at least [getMinimalDaysInFirstWeek()](https://developer.android.com/reference/kotlin/java/util/Calendar#getMinimalDaysInFirstWeek())days from that year. It thus depends on the values of`getMinimalDaysInFirstWeek()`,`getFirstDayOfWeek()`, and the day of the week of January 1. Weeks between week 1 of one year and week 1 of the following year (exclusive) are numbered sequentially from 2 to 52 or 53 (except for year(s) involved in the Julian-Gregorian transition).

The`getFirstDayOfWeek()`and`getMinimalDaysInFirstWeek()`values are initialized using locale-dependent resources when constructing a`GregorianCalendar`. The week determination is compatible with the ISO 8601 standard when`getFirstDayOfWeek()`is`MONDAY`and`getMinimalDaysInFirstWeek()`is 4, which values are used in locales where the standard is preferred. These values can explicitly be set by calling [setFirstDayOfWeek()](https://developer.android.com/reference/kotlin/java/util/Calendar#setFirstDayOfWeek(kotlin.Int))and [setMinimalDaysInFirstWeek()](https://developer.android.com/reference/kotlin/java/util/Calendar#setMinimalDaysInFirstWeek(kotlin.Int)).

A*week year* is in sync with a`WEEK_OF_YEAR`cycle. All weeks between the first and last weeks (inclusive) have the same*week year*value. Therefore, the first and last days of a week year may have different calendar year values.

For example, January 1, 1998 is a Thursday. If`getFirstDayOfWeek()`is`MONDAY`and`getMinimalDaysInFirstWeek()`is 4 (ISO 8601 standard compatible setting), then week 1 of 1998 starts on December 29, 1997, and ends on January 4, 1998. The week year is 1998 for the last three days of calendar year 1997. If, however,`getFirstDayOfWeek()`is`SUNDAY`, then week 1 of 1998 starts on January 4, 1998, and ends on January 10, 1998; the first three days of 1998 then are part of week 53 of 1997 and their week year is 1997.

### Week Of Month

Values calculated for the`WEEK_OF_MONTH`field range from 0 to 6. Week 1 of a month (the days with`WEEK_OF_MONTH = 1`) is the earliest set of at least`getMinimalDaysInFirstWeek()`contiguous days in that month, ending on the day before`getFirstDayOfWeek()`. Unlike week 1 of a year, week 1 of a month may be shorter than 7 days, need not start on`getFirstDayOfWeek()`, and will not include days of the previous month. Days of a month before week 1 have a`WEEK_OF_MONTH`of 0.

For example, if`getFirstDayOfWeek()`is`SUNDAY`and`getMinimalDaysInFirstWeek()`is 4, then the first week of January 1998 is Sunday, January 4 through Saturday, January 10. These days have a`WEEK_OF_MONTH`of 1. Thursday, January 1 through Saturday, January 3 have a`WEEK_OF_MONTH`of 0. If`getMinimalDaysInFirstWeek()`is changed to 3, then January 1 through January 3 have a`WEEK_OF_MONTH`of 1.

### Default Fields Values

The`clear`method sets calendar field(s) undefined.`GregorianCalendar`uses the following default value for each calendar field if its value is undefined.

| Field | Default Value |
| `ERA` | `AD` |
| `YEAR` | `1970` |
| `MONTH` | `JANUARY` |
| `DAY_OF_MONTH` | `1` |
| `DAY_OF_WEEK` | `the first day of week` |
| `WEEK_OF_MONTH` | `0` |
| `DAY_OF_WEEK_IN_MONTH` | `1` |
| `AM_PM` | `AM` |
| `HOUR, HOUR_OF_DAY, MINUTE, SECOND, MILLISECOND` | `0` |
|--------------------------------------------------|-------------------------|

<br />

Default values are not applicable for the fields not listed above.

**Example:** 

```kotlin
// get the supported ids for GMT-08:00 (Pacific Standard Time)
  String[] ids = TimeZone.getAvailableIDs(-8 * 60 * 60 * 1000);
  // if no ids were returned, something is wrong. get out.
  if (ids.length == 0)
      System.exit(0);
 
   // begin output
  System.out.println("Current Time");
 
  // create a Pacific Standard Time time zone
  SimpleTimeZone pdt = new SimpleTimeZone(-8 * 60 * 60 * 1000, ids[0]);
 
  // set up rules for Daylight Saving Time
  pdt.setStartRule(Calendar.APRIL, 1, Calendar.SUNDAY, 2 * 60 * 60 * 1000);
  pdt.setEndRule(Calendar.OCTOBER, -1, Calendar.SUNDAY, 2 * 60 * 60 * 1000);
 
  // create a GregorianCalendar with the Pacific Daylight time zone
  // and the current date and time
  Calendar calendar = new GregorianCalendar(pdt);
  Date trialTime = new Date();
  calendar.setTime(trialTime);
 
  // print out a bunch of interesting things
  System.out.println("ERA: " + calendar.get(Calendar.ERA));
  System.out.println("YEAR: " + calendar.get(Calendar.YEAR));
  System.out.println("MONTH: " + calendar.get(Calendar.MONTH));
  System.out.println("WEEK_OF_YEAR: " + calendar.get(Calendar.WEEK_OF_YEAR));
  System.out.println("WEEK_OF_MONTH: " + calendar.get(Calendar.WEEK_OF_MONTH));
  System.out.println("DATE: " + calendar.get(Calendar.DATE));
  System.out.println("DAY_OF_MONTH: " + calendar.get(Calendar.DAY_OF_MONTH));
  System.out.println("DAY_OF_YEAR: " + calendar.get(Calendar.DAY_OF_YEAR));
  System.out.println("DAY_OF_WEEK: " + calendar.get(Calendar.DAY_OF_WEEK));
  System.out.println("DAY_OF_WEEK_IN_MONTH: "
                     + calendar.get(Calendar.DAY_OF_WEEK_IN_MONTH));
  System.out.println("AM_PM: " + calendar.get(Calendar.AM_PM));
  System.out.println("HOUR: " + calendar.get(Calendar.HOUR));
  System.out.println("HOUR_OF_DAY: " + calendar.get(Calendar.HOUR_OF_DAY));
  System.out.println("MINUTE: " + calendar.get(Calendar.MINUTE));
  System.out.println("SECOND: " + calendar.get(Calendar.SECOND));
  System.out.println("MILLISECOND: " + calendar.get(Calendar.MILLISECOND));
  System.out.println("ZONE_OFFSET: "
                     + (calendar.get(Calendar.ZONE_OFFSET)/(60*60*1000)));
  System.out.println("DST_OFFSET: "
                     + (calendar.get(Calendar.DST_OFFSET)/(60*60*1000)));
  System.out.println("Current Time, with hour reset to 3");
  calendar.clear(Calendar.HOUR_OF_DAY); // so doesn't override
  calendar.set(Calendar.HOUR, 3);
  System.out.println("ERA: " + calendar.get(Calendar.ERA));
  System.out.println("YEAR: " + calendar.get(Calendar.YEAR));
  System.out.println("MONTH: " + calendar.get(Calendar.MONTH));
  System.out.println("WEEK_OF_YEAR: " + calendar.get(Calendar.WEEK_OF_YEAR));
  System.out.println("WEEK_OF_MONTH: " + calendar.get(Calendar.WEEK_OF_MONTH));
  System.out.println("DATE: " + calendar.get(Calendar.DATE));
  System.out.println("DAY_OF_MONTH: " + calendar.get(Calendar.DAY_OF_MONTH));
  System.out.println("DAY_OF_YEAR: " + calendar.get(Calendar.DAY_OF_YEAR));
  System.out.println("DAY_OF_WEEK: " + calendar.get(Calendar.DAY_OF_WEEK));
  System.out.println("DAY_OF_WEEK_IN_MONTH: "
                     + calendar.get(Calendar.DAY_OF_WEEK_IN_MONTH));
  System.out.println("AM_PM: " + calendar.get(Calendar.AM_PM));
  System.out.println("HOUR: " + calendar.get(Calendar.HOUR));
  System.out.println("HOUR_OF_DAY: " + calendar.get(Calendar.HOUR_OF_DAY));
  System.out.println("MINUTE: " + calendar.get(Calendar.MINUTE));
  System.out.println("SECOND: " + calendar.get(Calendar.SECOND));
  System.out.println("MILLISECOND: " + calendar.get(Calendar.MILLISECOND));
  System.out.println("ZONE_OFFSET: "
         + (calendar.get(Calendar.ZONE_OFFSET)/(60*60*1000))); // in hours
  System.out.println("DST_OFFSET: "
         + (calendar.get(Calendar.DST_OFFSET)/(60*60*1000))); // in hours
  
```

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AD](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#AD:kotlin.Int) Value of the`ERA`field indicating the common era (Anno Domini), also known as CE. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BC](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#BC:kotlin.Int) Value of the`ERA`field indicating the period before the common era (before Christ), also known as BCE. |

| Inherited constants ||
|---|---|
| From class [Calendar](https://developer.android.com/reference/kotlin/java/util/Calendar) |----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ALL_STYLES](https://developer.android.com/reference/kotlin/java/util/Calendar#ALL_STYLES:kotlin.Int) <br /> A style specifier for [getDisplayNames](https://developer.android.com/reference/kotlin/java/util/Calendar#getDisplayNames(kotlin.Int,%20kotlin.Int,%20java.util.Locale))indicating names in all styles, such as "January" and "Jan". <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AM](https://developer.android.com/reference/kotlin/java/util/Calendar#AM:kotlin.Int) <br /> Value of the [AM_PM](https://developer.android.com/reference/kotlin/java/util/Calendar#AM_PM:kotlin.Int) field indicating the period of the day from midnight to just before noon. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AM_PM](https://developer.android.com/reference/kotlin/java/util/Calendar#AM_PM:kotlin.Int) <br /> Field number for`get`and`set`indicating whether the`HOUR`is before or after noon. E.g., at 10:04:15.250 PM the`AM_PM`is`PM`. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [APRIL](https://developer.android.com/reference/kotlin/java/util/Calendar#APRIL:kotlin.Int) <br /> Value of the [MONTH](https://developer.android.com/reference/kotlin/java/util/Calendar#MONTH:kotlin.Int) field indicating the fourth month of the year in the Gregorian and Julian calendars. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AUGUST](https://developer.android.com/reference/kotlin/java/util/Calendar#AUGUST:kotlin.Int) <br /> Value of the [MONTH](https://developer.android.com/reference/kotlin/java/util/Calendar#MONTH:kotlin.Int) field indicating the eighth month of the year in the Gregorian and Julian calendars. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DATE](https://developer.android.com/reference/kotlin/java/util/Calendar#DATE:kotlin.Int) <br /> Field number for`get`and`set`indicating the day of the month. This is a synonym for`DAY_OF_MONTH`. The first day of the month has value 1. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DAY_OF_MONTH](https://developer.android.com/reference/kotlin/java/util/Calendar#DAY_OF_MONTH:kotlin.Int) <br /> Field number for`get`and`set`indicating the day of the month. This is a synonym for`DATE`. The first day of the month has value 1. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DAY_OF_WEEK](https://developer.android.com/reference/kotlin/java/util/Calendar#DAY_OF_WEEK:kotlin.Int) <br /> Field number for`get`and`set`indicating the day of the week. This field takes values`SUNDAY`,`MONDAY`,`TUESDAY`,`WEDNESDAY`,`THURSDAY`,`FRIDAY`, and`SATURDAY`. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DAY_OF_WEEK_IN_MONTH](https://developer.android.com/reference/kotlin/java/util/Calendar#DAY_OF_WEEK_IN_MONTH:kotlin.Int) <br /> Field number for`get`and`set`indicating the ordinal number of the day of the week within the current month. Together with the`DAY_OF_WEEK`field, this uniquely specifies a day within a month. Unlike`WEEK_OF_MONTH`and`WEEK_OF_YEAR`, this field's value does*not* depend on`getFirstDayOfWeek()`or`getMinimalDaysInFirstWeek()`.`DAY_OF_MONTH 1`through`7`always correspond to`DAY_OF_WEEK_IN_MONTH 1`;`8`through`14`correspond to`DAY_OF_WEEK_IN_MONTH 2`, and so on.`DAY_OF_WEEK_IN_MONTH 0`indicates the week before`DAY_OF_WEEK_IN_MONTH 1`. Negative values count back from the end of the month, so the last Sunday of a month is specified as`DAY_OF_WEEK = SUNDAY, DAY_OF_WEEK_IN_MONTH = -1`. Because negative values count backward they will usually be aligned differently within the month than positive values. For example, if a month has 31 days,`DAY_OF_WEEK_IN_MONTH -1`will overlap`DAY_OF_WEEK_IN_MONTH 5`and the end of`4`. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DAY_OF_YEAR](https://developer.android.com/reference/kotlin/java/util/Calendar#DAY_OF_YEAR:kotlin.Int) <br /> Field number for`get`and`set`indicating the day number within the current year. The first day of the year has value 1. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DECEMBER](https://developer.android.com/reference/kotlin/java/util/Calendar#DECEMBER:kotlin.Int) <br /> Value of the [MONTH](https://developer.android.com/reference/kotlin/java/util/Calendar#MONTH:kotlin.Int) field indicating the twelfth month of the year in the Gregorian and Julian calendars. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DST_OFFSET](https://developer.android.com/reference/kotlin/java/util/Calendar#DST_OFFSET:kotlin.Int) <br /> Field number for`get`and`set`indicating the daylight saving offset in milliseconds. This field reflects the correct daylight saving offset value of the time zone of this`Calendar`if the`TimeZone`implementation subclass supports historical Daylight Saving Time schedule changes. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERA](https://developer.android.com/reference/kotlin/java/util/Calendar#ERA:kotlin.Int) <br /> Field number for`get`and`set`indicating the era, e.g., AD or BC in the Julian calendar. This is a calendar-specific value; see subclass documentation. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FEBRUARY](https://developer.android.com/reference/kotlin/java/util/Calendar#FEBRUARY:kotlin.Int) <br /> Value of the [MONTH](https://developer.android.com/reference/kotlin/java/util/Calendar#MONTH:kotlin.Int) field indicating the second month of the year in the Gregorian and Julian calendars. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FIELD_COUNT](https://developer.android.com/reference/kotlin/java/util/Calendar#FIELD_COUNT:kotlin.Int) <br /> The number of distinct fields recognized by`get`and`set`. Field numbers range from`0..FIELD_COUNT-1`. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FRIDAY](https://developer.android.com/reference/kotlin/java/util/Calendar#FRIDAY:kotlin.Int) <br /> Value of the [DAY_OF_WEEK](https://developer.android.com/reference/kotlin/java/util/Calendar#DAY_OF_WEEK:kotlin.Int) field indicating Friday. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HOUR](https://developer.android.com/reference/kotlin/java/util/Calendar#HOUR:kotlin.Int) <br /> Field number for`get`and`set`indicating the hour of the morning or afternoon.`HOUR`is used for the 12-hour clock (0 - 11). Noon and midnight are represented by 0, not by 12. E.g., at 10:04:15.250 PM the`HOUR`is 10. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HOUR_OF_DAY](https://developer.android.com/reference/kotlin/java/util/Calendar#HOUR_OF_DAY:kotlin.Int) <br /> Field number for`get`and`set`indicating the hour of the day.`HOUR_OF_DAY`is used for the 24-hour clock. E.g., at 10:04:15.250 PM the`HOUR_OF_DAY`is 22. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [JANUARY](https://developer.android.com/reference/kotlin/java/util/Calendar#JANUARY:kotlin.Int) <br /> Value of the [MONTH](https://developer.android.com/reference/kotlin/java/util/Calendar#MONTH:kotlin.Int) field indicating the first month of the year in the Gregorian and Julian calendars. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [JULY](https://developer.android.com/reference/kotlin/java/util/Calendar#JULY:kotlin.Int) <br /> Value of the [MONTH](https://developer.android.com/reference/kotlin/java/util/Calendar#MONTH:kotlin.Int) field indicating the seventh month of the year in the Gregorian and Julian calendars. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [JUNE](https://developer.android.com/reference/kotlin/java/util/Calendar#JUNE:kotlin.Int) <br /> Value of the [MONTH](https://developer.android.com/reference/kotlin/java/util/Calendar#MONTH:kotlin.Int) field indicating the sixth month of the year in the Gregorian and Julian calendars. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LONG](https://developer.android.com/reference/kotlin/java/util/Calendar#LONG:kotlin.Int) <br /> A style specifier for [getDisplayName](https://developer.android.com/reference/kotlin/java/util/Calendar#getDisplayName(kotlin.Int,%20kotlin.Int,%20java.util.Locale))and [getDisplayNames](https://developer.android.com/reference/kotlin/java/util/Calendar#getDisplayNames(kotlin.Int,%20kotlin.Int,%20java.util.Locale))equivalent to [LONG_FORMAT](https://developer.android.com/reference/kotlin/java/util/Calendar#LONG_FORMAT:kotlin.Int). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LONG_FORMAT](https://developer.android.com/reference/kotlin/java/util/Calendar#LONG_FORMAT:kotlin.Int) <br /> A style specifier for [getDisplayName](https://developer.android.com/reference/kotlin/java/util/Calendar#getDisplayName(kotlin.Int,%20kotlin.Int,%20java.util.Locale))and [getDisplayNames](https://developer.android.com/reference/kotlin/java/util/Calendar#getDisplayNames(kotlin.Int,%20kotlin.Int,%20java.util.Locale))indicating a long name used for format. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LONG_STANDALONE](https://developer.android.com/reference/kotlin/java/util/Calendar#LONG_STANDALONE:kotlin.Int) <br /> A style specifier for [getDisplayName](https://developer.android.com/reference/kotlin/java/util/Calendar#getDisplayName(kotlin.Int,%20kotlin.Int,%20java.util.Locale))and [getDisplayNames](https://developer.android.com/reference/kotlin/java/util/Calendar#getDisplayNames(kotlin.Int,%20kotlin.Int,%20java.util.Locale))indicating a long name used independently, such as a month name as calendar headers. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MARCH](https://developer.android.com/reference/kotlin/java/util/Calendar#MARCH:kotlin.Int) <br /> Value of the [MONTH](https://developer.android.com/reference/kotlin/java/util/Calendar#MONTH:kotlin.Int) field indicating the third month of the year in the Gregorian and Julian calendars. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MAY](https://developer.android.com/reference/kotlin/java/util/Calendar#MAY:kotlin.Int) <br /> Value of the [MONTH](https://developer.android.com/reference/kotlin/java/util/Calendar#MONTH:kotlin.Int) field indicating the fifth month of the year in the Gregorian and Julian calendars. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MILLISECOND](https://developer.android.com/reference/kotlin/java/util/Calendar#MILLISECOND:kotlin.Int) <br /> Field number for`get`and`set`indicating the millisecond within the second. E.g., at 10:04:15.250 PM the`MILLISECOND`is 250. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MINUTE](https://developer.android.com/reference/kotlin/java/util/Calendar#MINUTE:kotlin.Int) <br /> Field number for`get`and`set`indicating the minute within the hour. E.g., at 10:04:15.250 PM the`MINUTE`is 4. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MONDAY](https://developer.android.com/reference/kotlin/java/util/Calendar#MONDAY:kotlin.Int) <br /> Value of the [DAY_OF_WEEK](https://developer.android.com/reference/kotlin/java/util/Calendar#DAY_OF_WEEK:kotlin.Int) field indicating Monday. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MONTH](https://developer.android.com/reference/kotlin/java/util/Calendar#MONTH:kotlin.Int) <br /> Field number for`get`and`set`indicating the month. This is a calendar-specific value. The first month of the year in the Gregorian and Julian calendars is`JANUARY`which is 0; the last depends on the number of months in a year. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NARROW_FORMAT](https://developer.android.com/reference/kotlin/java/util/Calendar#NARROW_FORMAT:kotlin.Int) <br /> A style specifier for [getDisplayName](https://developer.android.com/reference/kotlin/java/util/Calendar#getDisplayName(kotlin.Int,%20kotlin.Int,%20java.util.Locale))and [getDisplayNames](https://developer.android.com/reference/kotlin/java/util/Calendar#getDisplayNames(kotlin.Int,%20kotlin.Int,%20java.util.Locale))indicating a narrow name used for format. Narrow names are typically single character strings, such as "M" for Monday. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NARROW_STANDALONE](https://developer.android.com/reference/kotlin/java/util/Calendar#NARROW_STANDALONE:kotlin.Int) <br /> A style specifier for [getDisplayName](https://developer.android.com/reference/kotlin/java/util/Calendar#getDisplayName(kotlin.Int,%20kotlin.Int,%20java.util.Locale))and [getDisplayNames](https://developer.android.com/reference/kotlin/java/util/Calendar#getDisplayNames(kotlin.Int,%20kotlin.Int,%20java.util.Locale))indicating a narrow name independently. Narrow names are typically single character strings, such as "M" for Monday. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NOVEMBER](https://developer.android.com/reference/kotlin/java/util/Calendar#NOVEMBER:kotlin.Int) <br /> Value of the [MONTH](https://developer.android.com/reference/kotlin/java/util/Calendar#MONTH:kotlin.Int) field indicating the eleventh month of the year in the Gregorian and Julian calendars. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [OCTOBER](https://developer.android.com/reference/kotlin/java/util/Calendar#OCTOBER:kotlin.Int) <br /> Value of the [MONTH](https://developer.android.com/reference/kotlin/java/util/Calendar#MONTH:kotlin.Int) field indicating the tenth month of the year in the Gregorian and Julian calendars. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PM](https://developer.android.com/reference/kotlin/java/util/Calendar#PM:kotlin.Int) <br /> Value of the [AM_PM](https://developer.android.com/reference/kotlin/java/util/Calendar#AM_PM:kotlin.Int) field indicating the period of the day from noon to just before midnight. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SATURDAY](https://developer.android.com/reference/kotlin/java/util/Calendar#SATURDAY:kotlin.Int) <br /> Value of the [DAY_OF_WEEK](https://developer.android.com/reference/kotlin/java/util/Calendar#DAY_OF_WEEK:kotlin.Int) field indicating Saturday. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECOND](https://developer.android.com/reference/kotlin/java/util/Calendar#SECOND:kotlin.Int) <br /> Field number for`get`and`set`indicating the second within the minute. E.g., at 10:04:15.250 PM the`SECOND`is 15. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SEPTEMBER](https://developer.android.com/reference/kotlin/java/util/Calendar#SEPTEMBER:kotlin.Int) <br /> Value of the [MONTH](https://developer.android.com/reference/kotlin/java/util/Calendar#MONTH:kotlin.Int) field indicating the ninth month of the year in the Gregorian and Julian calendars. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SHORT](https://developer.android.com/reference/kotlin/java/util/Calendar#SHORT:kotlin.Int) <br /> A style specifier for [getDisplayName](https://developer.android.com/reference/kotlin/java/util/Calendar#getDisplayName(kotlin.Int,%20kotlin.Int,%20java.util.Locale))and [getDisplayNames](https://developer.android.com/reference/kotlin/java/util/Calendar#getDisplayNames(kotlin.Int,%20kotlin.Int,%20java.util.Locale))equivalent to [SHORT_FORMAT](https://developer.android.com/reference/kotlin/java/util/Calendar#SHORT_FORMAT:kotlin.Int). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SHORT_FORMAT](https://developer.android.com/reference/kotlin/java/util/Calendar#SHORT_FORMAT:kotlin.Int) <br /> A style specifier for [getDisplayName](https://developer.android.com/reference/kotlin/java/util/Calendar#getDisplayName(kotlin.Int,%20kotlin.Int,%20java.util.Locale))and [getDisplayNames](https://developer.android.com/reference/kotlin/java/util/Calendar#getDisplayNames(kotlin.Int,%20kotlin.Int,%20java.util.Locale))indicating a short name used for format. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SHORT_STANDALONE](https://developer.android.com/reference/kotlin/java/util/Calendar#SHORT_STANDALONE:kotlin.Int) <br /> A style specifier for [getDisplayName](https://developer.android.com/reference/kotlin/java/util/Calendar#getDisplayName(kotlin.Int,%20kotlin.Int,%20java.util.Locale))and [getDisplayNames](https://developer.android.com/reference/kotlin/java/util/Calendar#getDisplayNames(kotlin.Int,%20kotlin.Int,%20java.util.Locale))indicating a short name used independently, such as a month abbreviation as calendar headers. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SUNDAY](https://developer.android.com/reference/kotlin/java/util/Calendar#SUNDAY:kotlin.Int) <br /> Value of the [DAY_OF_WEEK](https://developer.android.com/reference/kotlin/java/util/Calendar#DAY_OF_WEEK:kotlin.Int) field indicating Sunday. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [THURSDAY](https://developer.android.com/reference/kotlin/java/util/Calendar#THURSDAY:kotlin.Int) <br /> Value of the [DAY_OF_WEEK](https://developer.android.com/reference/kotlin/java/util/Calendar#DAY_OF_WEEK:kotlin.Int) field indicating Thursday. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TUESDAY](https://developer.android.com/reference/kotlin/java/util/Calendar#TUESDAY:kotlin.Int) <br /> Value of the [DAY_OF_WEEK](https://developer.android.com/reference/kotlin/java/util/Calendar#DAY_OF_WEEK:kotlin.Int) field indicating Tuesday. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UNDECIMBER](https://developer.android.com/reference/kotlin/java/util/Calendar#UNDECIMBER:kotlin.Int) <br /> Value of the [MONTH](https://developer.android.com/reference/kotlin/java/util/Calendar#MONTH:kotlin.Int) field indicating the thirteenth month of the year. Although`GregorianCalendar`does not use this value, lunar calendars do. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WEDNESDAY](https://developer.android.com/reference/kotlin/java/util/Calendar#WEDNESDAY:kotlin.Int) <br /> Value of the [DAY_OF_WEEK](https://developer.android.com/reference/kotlin/java/util/Calendar#DAY_OF_WEEK:kotlin.Int) field indicating Wednesday. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WEEK_OF_MONTH](https://developer.android.com/reference/kotlin/java/util/Calendar#WEEK_OF_MONTH:kotlin.Int) <br /> Field number for`get`and`set`indicating the week number within the current month. The first week of the month, as defined by`getFirstDayOfWeek()`and`getMinimalDaysInFirstWeek()`, has value 1. Subclasses define the value of`WEEK_OF_MONTH`for days before the first week of the month. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WEEK_OF_YEAR](https://developer.android.com/reference/kotlin/java/util/Calendar#WEEK_OF_YEAR:kotlin.Int) <br /> Field number for`get`and`set`indicating the week number within the current year. The first week of the year, as defined by`getFirstDayOfWeek()`and`getMinimalDaysInFirstWeek()`, has value 1. Subclasses define the value of`WEEK_OF_YEAR`for days before the first week of the year. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [YEAR](https://developer.android.com/reference/kotlin/java/util/Calendar#YEAR:kotlin.Int) <br /> Field number for`get`and`set`indicating the year. This is a calendar-specific value; see subclass documentation. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ZONE_OFFSET](https://developer.android.com/reference/kotlin/java/util/Calendar#ZONE_OFFSET:kotlin.Int) <br /> Field number for`get`and`set`indicating the raw offset from GMT in milliseconds. This field reflects the correct GMT offset value of the time zone of this`Calendar`if the`TimeZone`implementation subclass supports historical GMT offset changes. <br /> | ||

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [GregorianCalendar](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#GregorianCalendar())`()` Constructs a default`GregorianCalendar`using the current time in the default time zone with the default [FORMAT](https://developer.android.com/reference/kotlin/java/util/Locale.Category) locale. |
| [GregorianCalendar](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#GregorianCalendar(kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`year:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `month:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dayOfMonth:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs a`GregorianCalendar`with the given date set in the default time zone with the default locale. |
| [GregorianCalendar](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#GregorianCalendar(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`year:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `month:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dayOfMonth:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `hourOfDay:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `minute:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs a`GregorianCalendar`with the given date and time set for the default time zone with the default locale. |
| [GregorianCalendar](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#GregorianCalendar(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`year:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `month:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dayOfMonth:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `hourOfDay:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `minute:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `second:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs a GregorianCalendar with the given date and time set for the default time zone with the default locale. |
| [GregorianCalendar](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#GregorianCalendar(java.util.Locale))`(`aLocale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale)!`)` Constructs a`GregorianCalendar`based on the current time in the default time zone with the given locale. |
| [GregorianCalendar](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#GregorianCalendar(java.util.TimeZone))`(`zone:` ` [TimeZone](https://developer.android.com/reference/kotlin/java/util/TimeZone)!`)` Constructs a`GregorianCalendar`based on the current time in the given time zone with the default [FORMAT](https://developer.android.com/reference/kotlin/java/util/Locale.Category) locale. |
| [GregorianCalendar](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#GregorianCalendar(java.util.TimeZone,%20java.util.Locale))`(`zone:` ` [TimeZone](https://developer.android.com/reference/kotlin/java/util/TimeZone)!`, `aLocale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale)!`)` Constructs a`GregorianCalendar`based on the current time in the given time zone with the given locale. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [add](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#add(kotlin.Int,%20kotlin.Int))`(`field:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `amount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Adds the specified (signed) amount of time to the given calendar field, based on the calendar's rules. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [clone](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#clone())`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Compares this`GregorianCalendar`to the specified`Object`. |
| openstatic [GregorianCalendar](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#)! | [from](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#from(java.time.ZonedDateTime))`(`zdt:` ` [ZonedDateTime](https://developer.android.com/reference/kotlin/java/time/ZonedDateTime.html#)!`)` Obtains an instance of`GregorianCalendar`with the default locale from a`ZonedDateTime`object. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getActualMaximum](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#getActualMaximum(kotlin.Int))`(`field:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the maximum value that this calendar field could have, taking into consideration the given time value and the current values of the [getFirstDayOfWeek](https://developer.android.com/reference/kotlin/java/util/Calendar#getFirstDayOfWeek()), [getMinimalDaysInFirstWeek](https://developer.android.com/reference/kotlin/java/util/Calendar#getMinimalDaysInFirstWeek()), [getGregorianChange](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#getGregorianChange())and [getTimeZone](https://developer.android.com/reference/kotlin/java/util/Calendar#getTimeZone())methods. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getActualMinimum](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#getActualMinimum(kotlin.Int))`(`field:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the minimum value that this calendar field could have, taking into consideration the given time value and the current values of the [getFirstDayOfWeek](https://developer.android.com/reference/kotlin/java/util/Calendar#getFirstDayOfWeek()), [getMinimalDaysInFirstWeek](https://developer.android.com/reference/kotlin/java/util/Calendar#getMinimalDaysInFirstWeek()), [getGregorianChange](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#getGregorianChange())and [getTimeZone](https://developer.android.com/reference/kotlin/java/util/Calendar#getTimeZone())methods. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getCalendarType](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#getCalendarType())`()` Returns`"gregory"`as the calendar type. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGreatestMinimum](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#getGreatestMinimum(kotlin.Int))`(`field:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the highest minimum value for the given calendar field of this`GregorianCalendar`instance. |
| [Date](https://developer.android.com/reference/kotlin/java/util/Date)! | [getGregorianChange](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#getGregorianChange())`()` Gets the Gregorian Calendar change date. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLeastMaximum](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#getLeastMaximum(kotlin.Int))`(`field:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the lowest maximum value for the given calendar field of this`GregorianCalendar`instance. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaximum](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#getMaximum(kotlin.Int))`(`field:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the maximum value for the given calendar field of this`GregorianCalendar`instance. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMinimum](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#getMinimum(kotlin.Int))`(`field:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the minimum value for the given calendar field of this`GregorianCalendar`instance. |
| open [TimeZone](https://developer.android.com/reference/kotlin/java/util/TimeZone) | [getTimeZone](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#getTimeZone())`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getWeekYear](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#getWeekYear())`()` Returns the [week year](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#week_year) represented by this`GregorianCalendar`. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getWeeksInWeekYear](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#getWeeksInWeekYear())`()` Returns the number of weeks in the [week year](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#week_year) represented by this`GregorianCalendar`. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#hashCode())`()` Generates the hash code for this`GregorianCalendar`object. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLeapYear](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#isLeapYear(kotlin.Int))`(`year:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Determines if the given year is a leap year. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isWeekDateSupported](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#isWeekDateSupported())`()` Returns`true`indicating this`GregorianCalendar`supports week dates. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [roll](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#roll(kotlin.Int,%20kotlin.Boolean))`(`field:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `up:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Adds or subtracts (up/down) a single unit of time on the given time field without changing larger fields. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [roll](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#roll(kotlin.Int,%20kotlin.Int))`(`field:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `amount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Adds a signed amount to the specified calendar field without changing larger fields. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setGregorianChange](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#setGregorianChange(java.util.Date))`(`date:` ` [Date](https://developer.android.com/reference/kotlin/java/util/Date)!`)` Sets the`GregorianCalendar`change date. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTimeZone](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#setTimeZone(java.util.TimeZone))`(`zone:` ` [TimeZone](https://developer.android.com/reference/kotlin/java/util/TimeZone)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setWeekDate](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#setWeekDate(kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`weekYear:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `weekOfYear:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dayOfWeek:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets this`GregorianCalendar`to the date given by the date specifiers - [`weekYear`](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#week_year),`weekOfYear`, and`dayOfWeek`. |
| open [ZonedDateTime](https://developer.android.com/reference/kotlin/java/time/ZonedDateTime.html#)! | [toZonedDateTime](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#toZonedDateTime())`()` Converts this object to a`ZonedDateTime`that represents the same point on the time-line as this`GregorianCalendar`. |

| Protected methods ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [computeFields](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#computeFields())`()` Converts the time value (millisecond offset from the [Epoch](https://developer.android.com/reference/kotlin/java/util/Calendar#Epoch)) to calendar field values. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [computeTime](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#computeTime())`()` Converts calendar field values to the time value (millisecond offset from the [Epoch](https://developer.android.com/reference/kotlin/java/util/Calendar#Epoch)). |

| Inherited functions ||
|---|---|
| From class [Calendar](https://developer.android.com/reference/kotlin/java/util/Calendar) |--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [after](https://developer.android.com/reference/kotlin/java/util/Calendar#after(kotlin.Any))`(`when:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> Returns whether this`Calendar`represents a time after the time represented by the specified`Object`. This method is equivalent to: ```kotlin <code>compareTo(when) &gt; 0 </code> ``` if and only if`when`is a`Calendar`instance. Otherwise, the method returns`false`. <br /> <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [before](https://developer.android.com/reference/kotlin/java/util/Calendar#before(kotlin.Any))`(`when:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> Returns whether this`Calendar`represents a time before the time represented by the specified`Object`. This method is equivalent to: ```kotlin <code>compareTo(when) &lt; 0 </code> ``` if and only if`when`is a`Calendar`instance. Otherwise, the method returns`false`. <br /> <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](https://developer.android.com/reference/kotlin/java/util/Calendar#clear())`()` <br /> Sets all the calendar field values and the time value (millisecond offset from the [Epoch](https://developer.android.com/reference/kotlin/java/util/Calendar#Epoch)) of this`Calendar`undefined. This means that [isSet()](https://developer.android.com/reference/kotlin/java/util/Calendar#isSet(kotlin.Int))will return`false`for all the calendar fields, and the date and time calculations will treat the fields as if they had never been set. A`Calendar`implementation class may use its specific default field values for date/time calculations. For example,`GregorianCalendar`uses 1970 if the`YEAR`field value is undefined. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](https://developer.android.com/reference/kotlin/java/util/Calendar#clear(kotlin.Int))`(`field:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the given calendar field value and the time value (millisecond offset from the [Epoch](https://developer.android.com/reference/kotlin/java/util/Calendar#Epoch)) of this`Calendar`undefined. This means that [isSet(field)](https://developer.android.com/reference/kotlin/java/util/Calendar#isSet(kotlin.Int))will return`false`, and the date and time calculations will treat the field as if it had never been set. A`Calendar`implementation class may use the field's specific default value for date and time calculations. The [HOUR_OF_DAY](https://developer.android.com/reference/kotlin/java/util/Calendar#HOUR_OF_DAY:kotlin.Int), [HOUR](https://developer.android.com/reference/kotlin/java/util/Calendar#HOUR:kotlin.Int) and [AM_PM](https://developer.android.com/reference/kotlin/java/util/Calendar#AM_PM:kotlin.Int) fields are handled independently and the [the resolution rule for the time of day](https://developer.android.com/reference/kotlin/java/util/Calendar#time_resolution) is applied. Clearing one of the fields doesn't reset the hour of day value of this`Calendar`. Use [set(Calendar.HOUR_OF_DAY, 0)](https://developer.android.com/reference/kotlin/java/util/Calendar#set(kotlin.Int,%20kotlin.Int))to reset the hour value. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compareTo](https://developer.android.com/reference/kotlin/java/util/Calendar#compareTo(java.util.Calendar))`(`other:` ` [Calendar](https://developer.android.com/reference/kotlin/java/util/Calendar)`)` <br /> Compares the time values (millisecond offsets from the [Epoch](https://developer.android.com/reference/kotlin/java/util/Calendar#Epoch)) represented by two`Calendar`objects. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [complete](https://developer.android.com/reference/kotlin/java/util/Calendar#complete())`()` <br /> Fills in any unset fields in the calendar fields. First, the [computeTime()](https://developer.android.com/reference/kotlin/java/util/Calendar#computeTime())method is called if the time value (millisecond offset from the [Epoch](https://developer.android.com/reference/kotlin/java/util/Calendar#Epoch)) has not been calculated from calendar field values. Then, the [computeFields()](https://developer.android.com/reference/kotlin/java/util/Calendar#computeFields())method is called to calculate all calendar field values. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [get](https://developer.android.com/reference/kotlin/java/util/Calendar#get(kotlin.Int))`(`field:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Returns the value of the given calendar field. In lenient mode, all calendar fields are normalized. In non-lenient mode, all calendar fields are validated and this method throws an exception if any calendar fields have out-of-range values. The normalization and validation are handled by the [complete()](https://developer.android.com/reference/kotlin/java/util/Calendar#complete())method, which process is calendar system dependent. <br /> | | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!> | [getAvailableCalendarTypes](https://developer.android.com/reference/kotlin/java/util/Calendar#getAvailableCalendarTypes())`()` <br /> Returns an unmodifiable`Set`containing all calendar types supported by`Calendar`in the runtime environment. The available calendar types can be used for the [Unicode locale extensions](https://developer.android.com/reference/kotlin/java/util/Locale#def_locale_extension). The`Set`returned contains at least`"gregory"`. The calendar types don't include aliases, such as`"gregorian"`for`"gregory"`. <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Locale](https://developer.android.com/reference/kotlin/java/util/Locale)!> | [getAvailableLocales](https://developer.android.com/reference/kotlin/java/util/Calendar#getAvailableLocales())`()` <br /> Returns an array of all locales for which the`getInstance`methods of this class can return localized instances. The array returned must contain at least a`Locale`instance equal to [Locale.US](https://developer.android.com/reference/kotlin/java/util/Locale#US:java.util.Locale). <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getDisplayName](https://developer.android.com/reference/kotlin/java/util/Calendar#getDisplayName(kotlin.Int,%20kotlin.Int,%20java.util.Locale))`(`field:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `style:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `locale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale)`)` <br /> Returns the string representation of the calendar`field`value in the given`style`and`locale`. If no string representation is applicable,`null`is returned. This method calls [get(field)](https://developer.android.com/reference/kotlin/java/util/Calendar#get(kotlin.Int))to get the calendar`field`value if the string representation is applicable to the given calendar`field`. For example, if this`Calendar`is a`GregorianCalendar`and its date is 2005-01-01, then the string representation of the [MONTH](https://developer.android.com/reference/kotlin/java/util/Calendar#MONTH:kotlin.Int) field would be "January" in the long style in an English locale or "Jan" in the short style. However, no string representation would be available for the [DAY_OF_MONTH](https://developer.android.com/reference/kotlin/java/util/Calendar#DAY_OF_MONTH:kotlin.Int) field, and this method would return`null`. The default implementation supports the calendar fields for which a [DateFormatSymbols](https://developer.android.com/reference/kotlin/java/text/DateFormatSymbols.html#) has names in the given`locale`. <br /> | | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!>? | [getDisplayNames](https://developer.android.com/reference/kotlin/java/util/Calendar#getDisplayNames(kotlin.Int,%20kotlin.Int,%20java.util.Locale))`(`field:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `style:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `locale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale)`)` <br /> Returns a`Map`containing all names of the calendar`field`in the given`style`and`locale`and their corresponding field values. For example, if this`Calendar`is a [GregorianCalendar](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#), the returned map would contain "Jan" to [JANUARY](https://developer.android.com/reference/kotlin/java/util/Calendar#JANUARY:kotlin.Int), "Feb" to [FEBRUARY](https://developer.android.com/reference/kotlin/java/util/Calendar#FEBRUARY:kotlin.Int), and so on, in the [short](https://developer.android.com/reference/kotlin/java/util/Calendar#SHORT:kotlin.Int) style in an English locale. Narrow names may not be unique due to use of single characters, such as "S" for Sunday and Saturday. In that case narrow names are not included in the returned`Map`. The values of other calendar fields may be taken into account to determine a set of display names. For example, if this`Calendar`is a lunisolar calendar system and the year value given by the [YEAR](https://developer.android.com/reference/kotlin/java/util/Calendar#YEAR:kotlin.Int) field has a leap month, this method would return month names containing the leap month name, and month names are mapped to their values specific for the year. The default implementation supports display names contained in a [DateFormatSymbols](https://developer.android.com/reference/kotlin/java/text/DateFormatSymbols.html#). For example, if`field`is [MONTH](https://developer.android.com/reference/kotlin/java/util/Calendar#MONTH:kotlin.Int) and`style`is [ALL_STYLES](https://developer.android.com/reference/kotlin/java/util/Calendar#ALL_STYLES:kotlin.Int), this method returns a`Map`containing all strings returned by [DateFormatSymbols.getShortMonths()](https://developer.android.com/reference/kotlin/java/text/DateFormatSymbols.html#getShortMonths())and [DateFormatSymbols.getMonths()](https://developer.android.com/reference/kotlin/java/text/DateFormatSymbols.html#getMonths()). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getFirstDayOfWeek](https://developer.android.com/reference/kotlin/java/util/Calendar#getFirstDayOfWeek())`()` <br /> Gets what the first day of the week is; e.g.,`SUNDAY`in the U.S.,`MONDAY`in France. <br /> | | [Calendar](https://developer.android.com/reference/kotlin/java/util/Calendar) | [getInstance](https://developer.android.com/reference/kotlin/java/util/Calendar#getInstance())`()` <br /> Gets a calendar using the default time zone and locale. The`Calendar`returned is based on the current time in the default time zone with the default [FORMAT](https://developer.android.com/reference/kotlin/java/util/Locale.Category) locale. Since Android 13, if the locale contains the time zone with "tz" [Unicode extension](https://developer.android.com/reference/kotlin/java/util/Locale#def_locale_extension), that time zone is used instead. <br /> | | [Calendar](https://developer.android.com/reference/kotlin/java/util/Calendar) | [getInstance](https://developer.android.com/reference/kotlin/java/util/Calendar#getInstance(java.util.Locale))`(`aLocale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale)`)` <br /> Gets a calendar using the default time zone and specified locale. The`Calendar`returned is based on the current time in the default time zone with the given locale. Since Android 13, if the locale contains the time zone with "tz" [Unicode extension](https://developer.android.com/reference/kotlin/java/util/Locale#def_locale_extension), that time zone is used instead. <br /> | | [Calendar](https://developer.android.com/reference/kotlin/java/util/Calendar) | [getInstance](https://developer.android.com/reference/kotlin/java/util/Calendar#getInstance(java.util.TimeZone))`(`zone:` ` [TimeZone](https://developer.android.com/reference/kotlin/java/util/TimeZone)`)` <br /> Gets a calendar using the specified time zone and default locale. The`Calendar`returned is based on the current time in the given time zone with the default [FORMAT](https://developer.android.com/reference/kotlin/java/util/Locale.Category) locale. <br /> | | [Calendar](https://developer.android.com/reference/kotlin/java/util/Calendar) | [getInstance](https://developer.android.com/reference/kotlin/java/util/Calendar#getInstance(java.util.TimeZone,%20java.util.Locale))`(`zone:` ` [TimeZone](https://developer.android.com/reference/kotlin/java/util/TimeZone)`, `aLocale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale)`)` <br /> Gets a calendar with the specified time zone and locale. The`Calendar`returned is based on the current time in the given time zone with the given locale. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMinimalDaysInFirstWeek](https://developer.android.com/reference/kotlin/java/util/Calendar#getMinimalDaysInFirstWeek())`()` <br /> Gets what the minimal days required in the first week of the year are; e.g., if the first week is defined as one that contains the first day of the first month of a year, this method returns 1. If the minimal days required must be a full week, this method returns 7. <br /> | | [Date](https://developer.android.com/reference/kotlin/java/util/Date) | [getTime](https://developer.android.com/reference/kotlin/java/util/Calendar#getTime())`()` <br /> Returns a`Date`object representing this`Calendar`'s time value (millisecond offset from the [Epoch](https://developer.android.com/reference/kotlin/java/util/Calendar#Epoch)"). <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getTimeInMillis](https://developer.android.com/reference/kotlin/java/util/Calendar#getTimeInMillis())`()` <br /> Returns this Calendar's time value in milliseconds. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [internalGet](https://developer.android.com/reference/kotlin/java/util/Calendar#internalGet(kotlin.Int))`(`field:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Returns the value of the given calendar field. This method does not involve normalization or validation of the field value. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLenient](https://developer.android.com/reference/kotlin/java/util/Calendar#isLenient())`()` <br /> Tells whether date/time interpretation is to be lenient. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSet](https://developer.android.com/reference/kotlin/java/util/Calendar#isSet(kotlin.Int))`(`field:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Determines if the given calendar field has a value set, including cases that the value has been set by internal fields calculations triggered by a`get`method call. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [set](https://developer.android.com/reference/kotlin/java/util/Calendar#set(kotlin.Int,%20kotlin.Int))`(`field:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the given calendar field to the given value. The value is not interpreted by this method regardless of the leniency mode. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [set](https://developer.android.com/reference/kotlin/java/util/Calendar#set(kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`year:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `month:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `date:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the values for the calendar fields`YEAR`,`MONTH`, and`DAY_OF_MONTH`. Previous values of other calendar fields are retained. If this is not desired, call [clear()](https://developer.android.com/reference/kotlin/java/util/Calendar#clear())first. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [set](https://developer.android.com/reference/kotlin/java/util/Calendar#set(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`year:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `month:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `date:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `hourOfDay:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `minute:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the values for the calendar fields`YEAR`,`MONTH`,`DAY_OF_MONTH`,`HOUR_OF_DAY`, and`MINUTE`. Previous values of other fields are retained. If this is not desired, call [clear()](https://developer.android.com/reference/kotlin/java/util/Calendar#clear())first. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [set](https://developer.android.com/reference/kotlin/java/util/Calendar#set(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`year:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `month:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `date:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `hourOfDay:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `minute:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `second:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the values for the fields`YEAR`,`MONTH`,`DAY_OF_MONTH`,`HOUR_OF_DAY`,`MINUTE`, and`SECOND`. Previous values of other fields are retained. If this is not desired, call [clear()](https://developer.android.com/reference/kotlin/java/util/Calendar#clear())first. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFirstDayOfWeek](https://developer.android.com/reference/kotlin/java/util/Calendar#setFirstDayOfWeek(kotlin.Int))`(`value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets what the first day of the week is; e.g.,`SUNDAY`in the U.S.,`MONDAY`in France. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLenient](https://developer.android.com/reference/kotlin/java/util/Calendar#setLenient(kotlin.Boolean))`(`lenient:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Specifies whether or not date/time interpretation is to be lenient. With lenient interpretation, a date such as "February 942, 1996" will be treated as being equivalent to the 941st day after February 1, 1996. With strict (non-lenient) interpretation, such dates will cause an exception to be thrown. The default is lenient. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMinimalDaysInFirstWeek](https://developer.android.com/reference/kotlin/java/util/Calendar#setMinimalDaysInFirstWeek(kotlin.Int))`(`value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets what the minimal days required in the first week of the year are; For example, if the first week is defined as one that contains the first day of the first month of a year, call this method with value 1. If it must be a full week, use value 7. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTime](https://developer.android.com/reference/kotlin/java/util/Calendar#setTime(java.util.Date))`(`date:` ` [Date](https://developer.android.com/reference/kotlin/java/util/Date)`)` <br /> Sets this Calendar's time with the given`Date`. Note: Calling`setTime()`with`Date(Long.MAX_VALUE)`or`Date(Long.MIN_VALUE)`may yield incorrect field values from`get()`. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTimeInMillis](https://developer.android.com/reference/kotlin/java/util/Calendar#setTimeInMillis(kotlin.Long))`(`millis:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Sets this Calendar's current time from the given long value. <br /> | | [Instant](https://developer.android.com/reference/kotlin/java/time/Instant.html#) | [toInstant](https://developer.android.com/reference/kotlin/java/util/Calendar#toInstant())`()` <br /> Converts this object to an [Instant](https://developer.android.com/reference/kotlin/java/time/Instant.html#). The conversion creates an`Instant`that represents the same point on the time-line as this`Calendar`. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/util/Calendar#toString())`()` <br /> Return a string representation of this calendar. This method is intended to be used only for debugging purposes, and the format of the returned string may vary between implementations. The returned string may be empty but may not be`null`. <br /> | ||

| Inherited properties ||
|---|---|
| From class [Calendar](https://developer.android.com/reference/kotlin/java/util/Calendar) |-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [areFieldsSet](https://developer.android.com/reference/kotlin/java/util/Calendar#areFieldsSet:kotlin.Boolean) <br /> True if`fields[]`are in sync with the currently set time. If false, then the next attempt to get the value of a field will force a recomputation of all fields from the current value of`time`. <br /> | | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | [fields](https://developer.android.com/reference/kotlin/java/util/Calendar#fields:kotlin.IntArray) <br /> The calendar field values for the currently set time for this calendar. This is an array of`FIELD_COUNT`integers, with index values`ERA`through`DST_OFFSET`. <br /> | | [BooleanArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html) | [isSet](https://developer.android.com/reference/kotlin/java/util/Calendar#isSet:kotlin.BooleanArray) <br /> The flags which tell if a specified calendar field for the calendar is set. A new object has no fields set. After the first call to a method which generates the fields, they all remain set after that. This is an array of`FIELD_COUNT`booleans, with index values`ERA`through`DST_OFFSET`. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isTimeSet](https://developer.android.com/reference/kotlin/java/util/Calendar#isTimeSet:kotlin.Boolean) <br /> True if then the value of`time`is valid. The time is made invalid by a change to an item of`field[]`. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [time](https://developer.android.com/reference/kotlin/java/util/Calendar#time:kotlin.Long) <br /> The currently set time for this calendar, expressed in milliseconds after January 1, 1970, 0:00:00 GMT. <br /> | ||

## Constants

### AD

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AD: Int
```

Value of the`ERA`field indicating the common era (Anno Domini), also known as CE. The sequence of years at the transition from`BC`to`AD`is ..., 2 BC, 1 BC, 1 AD, 2 AD,... 

 Value: 1

**See Also**

- [#ERA](https://developer.android.com/reference/kotlin/java/util/Calendar#ERA:kotlin.Int) 

### BC

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BC: Int
```

Value of the`ERA`field indicating the period before the common era (before Christ), also known as BCE. The sequence of years at the transition from`BC`to`AD`is ..., 2 BC, 1 BC, 1 AD, 2 AD,... 

 Value: 0

**See Also**

- [#ERA](https://developer.android.com/reference/kotlin/java/util/Calendar#ERA:kotlin.Int)

## Public constructors

### GregorianCalendar

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
GregorianCalendar()
```

Constructs a default`GregorianCalendar`using the current time in the default time zone with the default [FORMAT](https://developer.android.com/reference/kotlin/java/util/Locale.Category) locale. 

### GregorianCalendar

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
GregorianCalendar(
    year: Int, 
    month: Int, 
    dayOfMonth: Int)
```

Constructs a`GregorianCalendar`with the given date set in the default time zone with the default locale.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `year` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the value used to set the`YEAR`calendar field in the calendar. |
| `month` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the value used to set the`MONTH`calendar field in the calendar. Month value is 0-based. e.g., 0 for January. |
| `dayOfMonth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the value used to set the`DAY_OF_MONTH`calendar field in the calendar. |

### GregorianCalendar

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
GregorianCalendar(
    year: Int, 
    month: Int, 
    dayOfMonth: Int, 
    hourOfDay: Int, 
    minute: Int)
```

Constructs a`GregorianCalendar`with the given date and time set for the default time zone with the default locale.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `year` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the value used to set the`YEAR`calendar field in the calendar. |
| `month` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the value used to set the`MONTH`calendar field in the calendar. Month value is 0-based. e.g., 0 for January. |
| `dayOfMonth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the value used to set the`DAY_OF_MONTH`calendar field in the calendar. |
| `hourOfDay` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the value used to set the`HOUR_OF_DAY`calendar field in the calendar. |
| `minute` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the value used to set the`MINUTE`calendar field in the calendar. |

### GregorianCalendar

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
GregorianCalendar(
    year: Int, 
    month: Int, 
    dayOfMonth: Int, 
    hourOfDay: Int, 
    minute: Int, 
    second: Int)
```

Constructs a GregorianCalendar with the given date and time set for the default time zone with the default locale.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `year` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the value used to set the`YEAR`calendar field in the calendar. |
| `month` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the value used to set the`MONTH`calendar field in the calendar. Month value is 0-based. e.g., 0 for January. |
| `dayOfMonth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the value used to set the`DAY_OF_MONTH`calendar field in the calendar. |
| `hourOfDay` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the value used to set the`HOUR_OF_DAY`calendar field in the calendar. |
| `minute` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the value used to set the`MINUTE`calendar field in the calendar. |
| `second` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the value used to set the`SECOND`calendar field in the calendar. |

### GregorianCalendar

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
GregorianCalendar(aLocale: Locale!)
```

Constructs a`GregorianCalendar`based on the current time in the default time zone with the given locale.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------|
| `aLocale` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale)!:the given locale. |

### GregorianCalendar

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
GregorianCalendar(zone: TimeZone!)
```

Constructs a`GregorianCalendar`based on the current time in the given time zone with the default [FORMAT](https://developer.android.com/reference/kotlin/java/util/Locale.Category) locale.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------|
| `zone` | [TimeZone](https://developer.android.com/reference/kotlin/java/util/TimeZone)!:the given time zone. |

### GregorianCalendar

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
GregorianCalendar(
    zone: TimeZone!, 
    aLocale: Locale!)
```

Constructs a`GregorianCalendar`based on the current time in the given time zone with the given locale.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------|
| `zone` | [TimeZone](https://developer.android.com/reference/kotlin/java/util/TimeZone)!:the given time zone. |
| `aLocale` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale)!:the given locale. |

## Public methods

### add

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun add(
    field: Int, 
    amount: Int
): Unit
```

Adds the specified (signed) amount of time to the given calendar field, based on the calendar's rules.

*Add rule 1* . The value of`field`after the call minus the value of`field`before the call is`amount`, modulo any overflow that has occurred in`field`. Overflow occurs when a field value exceeds its range and, as a result, the next larger field is incremented or decremented and the field value is adjusted back into its range.

*Add rule 2* . If a smaller field is expected to be invariant, but it is impossible for it to be equal to its prior value because of changes in its minimum or maximum after`field`is changed, then its value is adjusted to be as close as possible to its expected value. A smaller field represents a smaller unit of time.`HOUR`is a smaller field than`DAY_OF_MONTH`. No adjustment is made to smaller fields that are not expected to be invariant. The calendar system determines what fields are expected to be invariant.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------|
| `field` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the calendar field. |
| `amount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the amount of date or time to be added to the field. |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if`field`is`ZONE_OFFSET`,`DST_OFFSET`, or unknown, or if any calendar fields have out-of-range values in non-lenient mode. |

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clone(): Any
```

| Return ||
|----------------------------------------------------------------------------|------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | a copy of this object. |

| Exceptions ||
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the`Cloneable`interface. Subclasses that override the`clone`method can also throw this exception to indicate that an instance cannot be cloned. |

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

Compares this`GregorianCalendar`to the specified`Object`. The result is`true`if and only if the argument is a`GregorianCalendar`object that represents the same time value (millisecond offset from the [Epoch](https://developer.android.com/reference/kotlin/java/util/Calendar#Epoch)) under the same`Calendar`parameters and Gregorian change date as this object.

| Parameters ||
|-------|-----------------------------|
| `obj` | the object to compare with. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is equal to`obj`;`false`otherwise. |

**See Also**

- [java.util.Calendar#compareTo(Calendar)](https://developer.android.com/reference/kotlin/java/util/Calendar#compareTo(java.util.Calendar)) 

### from

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun from(zdt: ZonedDateTime!): GregorianCalendar!
```

Obtains an instance of`GregorianCalendar`with the default locale from a`ZonedDateTime`object.

Since`ZonedDateTime`does not support a Julian-Gregorian cutover date and uses ISO calendar system, the return GregorianCalendar is a pure Gregorian calendar and uses ISO 8601 standard for week definitions, which has`MONDAY`as the [FirstDayOfWeek](https://developer.android.com/reference/kotlin/java/util/Calendar#getFirstDayOfWeek())and`4`as the value of the [MinimalDaysInFirstWeek](https://developer.android.com/reference/kotlin/java/util/Calendar#getMinimalDaysInFirstWeek()).

`ZoneDateTime`can store points on the time-line further in the future and further in the past than`GregorianCalendar`. In this scenario, this method will throw an`IllegalArgumentException`exception.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------------------|
| `zdt` | [ZonedDateTime](https://developer.android.com/reference/kotlin/java/time/ZonedDateTime.html#)!:the zoned date-time object to convert |

| Return ||
|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [GregorianCalendar](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#)! | the gregorian calendar representing the same point on the time-line as the zoned date-time provided |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if`zdt`is null |
| `java.lang.IllegalArgumentException` | if the zoned date-time is too large to represent as a`GregorianCalendar` |

### getActualMaximum

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getActualMaximum(field: Int): Int
```

Returns the maximum value that this calendar field could have, taking into consideration the given time value and the current values of the [getFirstDayOfWeek](https://developer.android.com/reference/kotlin/java/util/Calendar#getFirstDayOfWeek()), [getMinimalDaysInFirstWeek](https://developer.android.com/reference/kotlin/java/util/Calendar#getMinimalDaysInFirstWeek()), [getGregorianChange](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#getGregorianChange())and [getTimeZone](https://developer.android.com/reference/kotlin/java/util/Calendar#getTimeZone())methods. For example, if the date of this instance is February 1, 2004, the actual maximum value of the`DAY_OF_MONTH`field is 29 because 2004 is a leap year, and if the date of this instance is February 1, 2005, it's 28.

This method calculates the maximum value of [WEEK_OF_YEAR](https://developer.android.com/reference/kotlin/java/util/Calendar#WEEK_OF_YEAR:kotlin.Int) based on the [YEAR](https://developer.android.com/reference/kotlin/java/util/Calendar#YEAR:kotlin.Int)(calendar year) value, not the [week year](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#week_year). Call [getWeeksInWeekYear()](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#getWeeksInWeekYear())to get the maximum value of`WEEK_OF_YEAR`in the week year of this`GregorianCalendar`.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------|
| `field` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the calendar field |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the maximum of the given field for the time value of this`GregorianCalendar` |

**See Also**

- [#getMinimum(int)](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#getMinimum(kotlin.Int))
- [#getMaximum(int)](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#getMaximum(kotlin.Int))
- [#getGreatestMinimum(int)](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#getGreatestMinimum(kotlin.Int))
- [#getLeastMaximum(int)](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#getLeastMaximum(kotlin.Int))
- [#getActualMinimum(int)](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#getActualMinimum(kotlin.Int)) 

### getActualMinimum

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getActualMinimum(field: Int): Int
```

Returns the minimum value that this calendar field could have, taking into consideration the given time value and the current values of the [getFirstDayOfWeek](https://developer.android.com/reference/kotlin/java/util/Calendar#getFirstDayOfWeek()), [getMinimalDaysInFirstWeek](https://developer.android.com/reference/kotlin/java/util/Calendar#getMinimalDaysInFirstWeek()), [getGregorianChange](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#getGregorianChange())and [getTimeZone](https://developer.android.com/reference/kotlin/java/util/Calendar#getTimeZone())methods.

For example, if the Gregorian change date is January 10, 1970 and the date of this`GregorianCalendar`is January 20, 1970, the actual minimum value of the`DAY_OF_MONTH`field is 10 because the previous date of January 10, 1970 is December 27, 1996 (in the Julian calendar). Therefore, December 28, 1969 to January 9, 1970 don't exist.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------|
| `field` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the calendar field |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the minimum of the given field for the time value of this`GregorianCalendar` |

**See Also**

- [#getMinimum(int)](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#getMinimum(kotlin.Int))
- [#getMaximum(int)](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#getMaximum(kotlin.Int))
- [#getGreatestMinimum(int)](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#getGreatestMinimum(kotlin.Int))
- [#getLeastMaximum(int)](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#getLeastMaximum(kotlin.Int))
- [#getActualMaximum(int)](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#getActualMaximum(kotlin.Int)) 

### getCalendarType

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCalendarType(): String
```

Returns`"gregory"`as the calendar type.

| Return ||
|----------------------------------------------------------------------------------|-------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `"gregory"` |

### getGreatestMinimum

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getGreatestMinimum(field: Int): Int
```

Returns the highest minimum value for the given calendar field of this`GregorianCalendar`instance. The highest minimum value is defined as the largest value returned by [getActualMinimum(int)](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#getActualMinimum(kotlin.Int))for any possible time value, taking into consideration the current values of the [getFirstDayOfWeek](https://developer.android.com/reference/kotlin/java/util/Calendar#getFirstDayOfWeek()), [getMinimalDaysInFirstWeek](https://developer.android.com/reference/kotlin/java/util/Calendar#getMinimalDaysInFirstWeek()), [getGregorianChange](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#getGregorianChange())and [getTimeZone](https://developer.android.com/reference/kotlin/java/util/Calendar#getTimeZone())methods.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------|
| `field` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the calendar field. |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the highest minimum value for the given calendar field. |

**See Also**

- [#getMinimum(int)](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#getMinimum(kotlin.Int))
- [#getMaximum(int)](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#getMaximum(kotlin.Int))
- [#getLeastMaximum(int)](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#getLeastMaximum(kotlin.Int))
- [#getActualMinimum(int)](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#getActualMinimum(kotlin.Int))
- [#getActualMaximum(int)](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#getActualMaximum(kotlin.Int)) 

### getGregorianChange

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getGregorianChange(): Date!
```

Gets the Gregorian Calendar change date. This is the point when the switch from Julian dates to Gregorian dates occurred. Default is October 15, 1582 (Gregorian). Previous to this, dates will be in the Julian calendar.

| Return ||
|------------------------------------------------------------------------|---------------------------------------------------------------|
| [Date](https://developer.android.com/reference/kotlin/java/util/Date)! | the Gregorian cutover date for this`GregorianCalendar`object. |

### getLeastMaximum

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLeastMaximum(field: Int): Int
```

Returns the lowest maximum value for the given calendar field of this`GregorianCalendar`instance. The lowest maximum value is defined as the smallest value returned by [getActualMaximum(int)](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#getActualMaximum(kotlin.Int))for any possible time value, taking into consideration the current values of the [getFirstDayOfWeek](https://developer.android.com/reference/kotlin/java/util/Calendar#getFirstDayOfWeek()), [getMinimalDaysInFirstWeek](https://developer.android.com/reference/kotlin/java/util/Calendar#getMinimalDaysInFirstWeek()), [getGregorianChange](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#getGregorianChange())and [getTimeZone](https://developer.android.com/reference/kotlin/java/util/Calendar#getTimeZone())methods.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------|
| `field` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the calendar field |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the lowest maximum value for the given calendar field. |

**See Also**

- [#getMinimum(int)](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#getMinimum(kotlin.Int))
- [#getMaximum(int)](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#getMaximum(kotlin.Int))
- [#getGreatestMinimum(int)](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#getGreatestMinimum(kotlin.Int))
- [#getActualMinimum(int)](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#getActualMinimum(kotlin.Int))
- [#getActualMaximum(int)](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#getActualMaximum(kotlin.Int)) 

### getMaximum

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMaximum(field: Int): Int
```

Returns the maximum value for the given calendar field of this`GregorianCalendar`instance. The maximum value is defined as the largest value returned by the [get](https://developer.android.com/reference/kotlin/java/util/Calendar#get(kotlin.Int))method for any possible time value, taking into consideration the current values of the [getFirstDayOfWeek](https://developer.android.com/reference/kotlin/java/util/Calendar#getFirstDayOfWeek()), [getMinimalDaysInFirstWeek](https://developer.android.com/reference/kotlin/java/util/Calendar#getMinimalDaysInFirstWeek()), [getGregorianChange](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#getGregorianChange())and [getTimeZone](https://developer.android.com/reference/kotlin/java/util/Calendar#getTimeZone())methods.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------|
| `field` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the calendar field. |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the maximum value for the given calendar field. |

**See Also**

- [#getMinimum(int)](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#getMinimum(kotlin.Int))
- [#getGreatestMinimum(int)](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#getGreatestMinimum(kotlin.Int))
- [#getLeastMaximum(int)](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#getLeastMaximum(kotlin.Int))
- [#getActualMinimum(int)](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#getActualMinimum(kotlin.Int))
- [#getActualMaximum(int)](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#getActualMaximum(kotlin.Int)) 

### getMinimum

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMinimum(field: Int): Int
```

Returns the minimum value for the given calendar field of this`GregorianCalendar`instance. The minimum value is defined as the smallest value returned by the [get](https://developer.android.com/reference/kotlin/java/util/Calendar#get(kotlin.Int))method for any possible time value, taking into consideration the current values of the [getFirstDayOfWeek](https://developer.android.com/reference/kotlin/java/util/Calendar#getFirstDayOfWeek()), [getMinimalDaysInFirstWeek](https://developer.android.com/reference/kotlin/java/util/Calendar#getMinimalDaysInFirstWeek()), [getGregorianChange](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#getGregorianChange())and [getTimeZone](https://developer.android.com/reference/kotlin/java/util/Calendar#getTimeZone())methods.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------|
| `field` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the calendar field. |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the minimum value for the given calendar field. |

**See Also**

- [#getMaximum(int)](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#getMaximum(kotlin.Int))
- [#getGreatestMinimum(int)](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#getGreatestMinimum(kotlin.Int))
- [#getLeastMaximum(int)](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#getLeastMaximum(kotlin.Int))
- [#getActualMinimum(int)](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#getActualMinimum(kotlin.Int))
- [#getActualMaximum(int)](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#getActualMaximum(kotlin.Int)) 

### getTimeZone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTimeZone(): TimeZone
```

| Return ||
|-------------------------------------------------------------------------------|-----------------------------------------------------|
| [TimeZone](https://developer.android.com/reference/kotlin/java/util/TimeZone) | the time zone object associated with this calendar. |

### getWeekYear

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getWeekYear(): Int
```

Returns the [week year](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#week_year) represented by this`GregorianCalendar`. The dates in the weeks between 1 and the maximum week number of the week year have the same week year value that may be one year before or after the [YEAR](https://developer.android.com/reference/kotlin/java/util/Calendar#YEAR:kotlin.Int)(calendar year) value.

This method calls [Calendar.complete()](https://developer.android.com/reference/kotlin/java/util/Calendar#complete())before calculating the week year.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the week year represented by this`GregorianCalendar`. If the [ERA](https://developer.android.com/reference/kotlin/java/util/Calendar#ERA:kotlin.Int) value is [BC](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#BC:kotlin.Int), the year is represented by 0 or a negative number: BC 1 is 0, BC 2 is -1, BC 3 is -2, and so on. |

| Exceptions ||
|-------------------------------------------|---------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if any week year numbering isn't supported in this`Calendar`. |
| `java.lang.IllegalArgumentException` | if any of the calendar fields is invalid in non-lenient mode. |

**See Also**

- <https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#isWeekDateSupported()>
- <https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#getWeeksInWeekYear()>
- [java.util.Calendar#getFirstDayOfWeek()](https://developer.android.com/reference/kotlin/java/util/Calendar#getFirstDayOfWeek())
- [java.util.Calendar#getMinimalDaysInFirstWeek()](https://developer.android.com/reference/kotlin/java/util/Calendar#getMinimalDaysInFirstWeek()) 

### getWeeksInWeekYear

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getWeeksInWeekYear(): Int
```

Returns the number of weeks in the [week year](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#week_year) represented by this`GregorianCalendar`.

For example, if this`GregorianCalendar`'s date is December 31, 2008 with [the ISO 8601 compatible setting](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#iso8601_compatible_setting), this method will return 53 for the period: December 29, 2008 to January 3, 2010 while [getActualMaximum(WEEK_OF_YEAR)](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#getActualMaximum(kotlin.Int))will return 52 for the period: December 31, 2007 to December 28, 2008.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of weeks in the week year. |

| Exceptions ||
|-------------------------------------------|---------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if any week year numbering isn't supported in this`Calendar`. |

**See Also**

- [java.util.Calendar#WEEK_OF_YEAR](https://developer.android.com/reference/kotlin/java/util/Calendar#WEEK_OF_YEAR:kotlin.Int)
- <https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#getWeekYear()>
- [#getActualMaximum(int)](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#getActualMaximum(kotlin.Int)) 

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

Generates the hash code for this`GregorianCalendar`object.

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### isLeapYear

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isLeapYear(year: Int): Boolean
```

Determines if the given year is a leap year. Returns`true`if the given year is a leap year. To specify BC year numbers,`1 - year number`must be given. For example, year BC 4 is specified as -3.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------|
| `year` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the given year. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the given year is a leap year;`false`otherwise. |

### isWeekDateSupported

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isWeekDateSupported(): Boolean
```

Returns`true`indicating this`GregorianCalendar`supports week dates.

| Return ||
|------------------------------------------------------------------------------------|----------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`(always) |

**See Also**

- <https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#getWeekYear()>
- [#setWeekDate(int,int,int)](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#setWeekDate(kotlin.Int,%20kotlin.Int,%20kotlin.Int))
- <https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#getWeeksInWeekYear()> 

### roll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun roll(
    field: Int, 
    up: Boolean
): Unit
```

Adds or subtracts (up/down) a single unit of time on the given time field without changing larger fields.

*Example* : Consider a`GregorianCalendar`originally set to December 31, 1999. Calling [roll(Calendar.MONTH, true)](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#roll(kotlin.Int,%20kotlin.Boolean))sets the calendar to January 31, 1999. The`YEAR`field is unchanged because it is a larger field than`MONTH`.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `field` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the time field. |
| `up` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):indicates if the value of the specified calendar field is to be rolled up or rolled down. Use`true`if rolling up,`false`otherwise. |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if`field`is`ZONE_OFFSET`,`DST_OFFSET`, or unknown, or if any calendar fields have out-of-range values in non-lenient mode. |

**See Also**

- [#add(int,int)](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#add(kotlin.Int,%20kotlin.Int))
- [#set(int,int)](https://developer.android.com/reference/kotlin/java/util/Calendar#set(kotlin.Int,%20kotlin.Int)) 

### roll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun roll(
    field: Int, 
    amount: Int
): Unit
```

Adds a signed amount to the specified calendar field without changing larger fields. A negative roll amount means to subtract from field without changing larger fields. If the specified amount is 0, this method performs nothing.

This method calls [complete()](https://developer.android.com/reference/kotlin/java/util/Calendar#complete())before adding the amount so that all the calendar fields are normalized. If there is any calendar field having an out-of-range value in non-lenient mode, then an`IllegalArgumentException`is thrown.

*Example* : Consider a`GregorianCalendar`originally set to August 31, 1999. Calling`roll(Calendar.MONTH, 8)`sets the calendar to April 30,**1999** . Using a`GregorianCalendar`, the`DAY_OF_MONTH`field cannot be 31 in the month April.`DAY_OF_MONTH`is set to the closest possible value, 30. The`YEAR`field maintains the value of 1999 because it is a larger field than`MONTH`.

*Example* : Consider a`GregorianCalendar`originally set to Sunday June 6, 1999. Calling`roll(Calendar.WEEK_OF_MONTH, -1)`sets the calendar to Tuesday June 1, 1999, whereas calling`add(Calendar.WEEK_OF_MONTH, -1)`sets the calendar to Sunday May 30, 1999. This is because the roll rule imposes an additional constraint: The`MONTH`must not change when the`WEEK_OF_MONTH`is rolled. Taken together with add rule 1, the resultant date must be between Tuesday June 1 and Saturday June 5. According to add rule 2, the`DAY_OF_WEEK`, an invariant when changing the`WEEK_OF_MONTH`, is set to Tuesday, the closest possible value to Sunday (where Sunday is the first day of the week).

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------|
| `field` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the calendar field. |
| `amount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the signed amount to add to`field`. |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if`field`is`ZONE_OFFSET`,`DST_OFFSET`, or unknown, or if any calendar fields have out-of-range values in non-lenient mode. |

**See Also**

- [#roll(int,boolean)](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#roll(kotlin.Int,%20kotlin.Boolean))
- [#add(int,int)](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#add(kotlin.Int,%20kotlin.Int))
- [#set(int,int)](https://developer.android.com/reference/kotlin/java/util/Calendar#set(kotlin.Int,%20kotlin.Int)) 

### setGregorianChange

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setGregorianChange(date: Date!): Unit
```

Sets the`GregorianCalendar`change date. This is the point when the switch from Julian dates to Gregorian dates occurred. Default is October 15, 1582 (Gregorian). Previous to this, dates will be in the Julian calendar.

To obtain a pure Julian calendar, set the change date to`Date(Long.MAX_VALUE)`. To obtain a pure Gregorian calendar, set the change date to`Date(Long.MIN_VALUE)`.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------|
| `date` | [Date](https://developer.android.com/reference/kotlin/java/util/Date)!:the given Gregorian cutover date. |

### setTimeZone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTimeZone(zone: TimeZone): Unit
```

| Parameters ||
|---------|----------------------|
| `value` | the given time zone. |

### setWeekDate

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setWeekDate(
    weekYear: Int, 
    weekOfYear: Int, 
    dayOfWeek: Int
): Unit
```

Sets this`GregorianCalendar`to the date given by the date specifiers - [`weekYear`](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#week_year),`weekOfYear`, and`dayOfWeek`.`weekOfYear`follows the [`WEEK_OF_YEAR`numbering](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#week_and_year). The`dayOfWeek`value must be one of the [DAY_OF_WEEK](https://developer.android.com/reference/kotlin/java/util/Calendar#DAY_OF_WEEK:kotlin.Int) values: [SUNDAY](https://developer.android.com/reference/kotlin/java/util/Calendar#SUNDAY:kotlin.Int) to [SATURDAY](https://developer.android.com/reference/kotlin/java/util/Calendar#SATURDAY:kotlin.Int).

Note that the numeric day-of-week representation differs from the ISO 8601 standard, and that the`weekOfYear`numbering is compatible with the standard when`getFirstDayOfWeek()`is`MONDAY`and`getMinimalDaysInFirstWeek()`is 4.

Unlike the`set`method, all of the calendar fields and the instant of time value are calculated upon return.

If`weekOfYear`is out of the valid week-of-year range in`weekYear`, the`weekYear`and`weekOfYear`values are adjusted in lenient mode, or an`IllegalArgumentException`is thrown in non-lenient mode.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `weekYear` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the week year |
| `weekOfYear` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the week number based on`weekYear` |
| `dayOfWeek` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the day of week value: one of the constants for the [DAY_OF_WEEK](https://developer.android.com/reference/kotlin/java/util/Calendar#DAY_OF_WEEK:kotlin.Int) field: [SUNDAY](https://developer.android.com/reference/kotlin/java/util/Calendar#SUNDAY:kotlin.Int), ..., [SATURDAY](https://developer.android.com/reference/kotlin/java/util/Calendar#SATURDAY:kotlin.Int). |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if any of the given date specifiers is invalid, or if any of the calendar fields are inconsistent with the given date specifiers in non-lenient mode |
| `java.lang.UnsupportedOperationException` | if any week year numbering isn't supported in this`Calendar`. |

**See Also**

- [java.util.GregorianCalendar#isWeekDateSupported()](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar#isWeekDateSupported())
- [java.util.Calendar#getFirstDayOfWeek()](https://developer.android.com/reference/kotlin/java/util/Calendar#getFirstDayOfWeek())
- [java.util.Calendar#getMinimalDaysInFirstWeek()](https://developer.android.com/reference/kotlin/java/util/Calendar#getMinimalDaysInFirstWeek()) 

### toZonedDateTime

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toZonedDateTime(): ZonedDateTime!
```

Converts this object to a`ZonedDateTime`that represents the same point on the time-line as this`GregorianCalendar`.

Since this object supports a Julian-Gregorian cutover date and`ZonedDateTime`does not, it is possible that the resulting year, month and day will have different values. The result will represent the correct date in the ISO calendar system, which will also be the same value for Modified Julian Days.

| Return ||
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [ZonedDateTime](https://developer.android.com/reference/kotlin/java/time/ZonedDateTime.html#)! | a zoned date-time representing the same point on the time-line as this gregorian calendar |

## Protected methods

### computeFields

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun computeFields(): Unit
```

Converts the time value (millisecond offset from the [Epoch](https://developer.android.com/reference/kotlin/java/util/Calendar#Epoch)) to calendar field values. The time is*not* recomputed first; to recompute the time, then the fields, call the`complete`method. 
**See Also**

- [java.util.Calendar#complete](https://developer.android.com/reference/kotlin/java/util/Calendar#complete()) 

### computeTime

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun computeTime(): Unit
```

Converts calendar field values to the time value (millisecond offset from the [Epoch](https://developer.android.com/reference/kotlin/java/util/Calendar#Epoch)).

| Exceptions ||
|--------------------------------------|-------------------------------------|
| `java.lang.IllegalArgumentException` | if any calendar fields are invalid. |
