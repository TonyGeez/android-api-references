# HebrewCalendar

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# HebrewCalendar

Kotlin| [Java](../android/icu/util/HebrewCalendar.md) 
| --- | --- |

```
open class HebrewCalendar : Calendar
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.icu.util.Calendar](../android/icu/util/Calendar.md) ||
| | ↳ | [android.icu.util.HebrewCalendar](../android/icu/util/HebrewCalendar.md) |

`HebrewCalendar`is a subclass of`Calendar`that that implements the traditional Hebrew calendar. This is the civil calendar in Israel and the liturgical calendar of the Jewish faith worldwide.

The Hebrew calendar is lunisolar and thus has a number of interesting properties that distinguish it from the Gregorian. Months start on the day of (an arithmetic approximation of) each new moon. Since the solar year (approximately 365.24 days) is not an even multiple of the lunar month (approximately 29.53 days) an extra "leap month" is inserted in 7 out of every 19 years. To make matters even more interesting, the start of a year can be delayed by up to three days in order to prevent certain holidays from falling on the Sabbath and to prevent certain illegal year lengths. Finally, the lengths of certain months can vary depending on the number of days in the year.

The leap month is known as "Adar 1" and is inserted between the months of Shevat and Adar in leap years. Since the leap month does not come at the end of the year, calculations involving month numbers are particularly complex. Users of this class should make sure to use the #roll and [add](../android/icu/util/HebrewCalendar.md))methods rather than attempting to perform date arithmetic by manipulating the fields directly.

**Note:**In the traditional Hebrew calendar, days start at sunset. However, in order to keep the time fields in this class synchronized with those of the other calendars and with local clock time, we treat days and months as beginning at midnight, roughly 6 hours after the corresponding sunset.

If you are interested in more information on the rules behind the Hebrew calendar, see one of the following references:

- " [Calendrical Calculations](http://www.amazon.com/exec/obidos/ASIN/0521564743)", by Nachum Dershowitz \& Edward Reingold, Cambridge University Press, 1997, pages 85-91.
- Hebrew Calendar Science and Myths,<http://web.archive.org/web/20090423084613/http://www.geocities.com/Athens/1584/>
- The Calendar FAQ,<http://www.faqs.org/faqs/calendars/faq/>

This class should not be subclassed.

HebrewCalendar usually should be instantiated using [android.icu.util.Calendar#getInstance(ULocale)](../android/icu/util/Calendar.md))passing in a`ULocale`with the tag`"@calendar=hebrew"`.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ADAR](../android/icu/util/HebrewCalendar.md) Constant for the Adar, the 7th month of the Hebrew year. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ADAR_1](../android/icu/util/HebrewCalendar.md) Constant for Adar I, the 6th month of the Hebrew year (present in leap years only). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AV](../android/icu/util/HebrewCalendar.md) Constant for Av, the 12th month of the Hebrew year. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ELUL](../android/icu/util/HebrewCalendar.md) Constant for Elul, the 13th month of the Hebrew year. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HESHVAN](../android/icu/util/HebrewCalendar.md) Constant for Heshvan, the 2nd month of the Hebrew year. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [IYAR](../android/icu/util/HebrewCalendar.md) Constant for Iyar, the 9th month of the Hebrew year. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [KISLEV](../android/icu/util/HebrewCalendar.md) Constant for Kislev, the 3rd month of the Hebrew year. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NISAN](../android/icu/util/HebrewCalendar.md) Constant for Nisan, the 8th month of the Hebrew year. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SHEVAT](../android/icu/util/HebrewCalendar.md) Constant for Shevat, the 5th month of the Hebrew year. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SIVAN](../android/icu/util/HebrewCalendar.md) Constant for Sivan, the 10th month of the Hebrew year. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TAMUZ](../android/icu/util/HebrewCalendar.md) Constant for Tammuz, the 11th month of the Hebrew year. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TEVET](../android/icu/util/HebrewCalendar.md) Constant for Tevet, the 4th month of the Hebrew year. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TISHRI](../android/icu/util/HebrewCalendar.md) Constant for Tishri, the 1st month of the Hebrew year. |

| Inherited constants ||
|---|---|
| From class [Calendar](../android/icu/util/Calendar.md) |------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AM](../android/icu/util/Calendar.md) <br /> Value of the`AM_PM`field indicating the period of the day from midnight to just before noon. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AM_PM](../android/icu/util/Calendar.md) <br /> Field number for`get`and`set`indicating whether the`HOUR`is before or after noon. E.g., at 10:04:15.250 PM the`AM_PM`is`PM`. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [APRIL](../android/icu/util/Calendar.md) <br /> Value of the`MONTH`field indicating the fourth month of the year. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AUGUST](../android/icu/util/Calendar.md) <br /> Value of the`MONTH`field indicating the eighth month of the year. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DATE](../android/icu/util/Calendar.md) <br /> Field number for`get`and`set`indicating the day of the month. This is a synonym for [DAY_OF_MONTH](../android/icu/util/Calendar.md). The first day of the month has value 1. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DAY_OF_MONTH](../android/icu/util/Calendar.md) <br /> Field number for`get`and`set`indicating the day of the month. This is a synonym for [DATE](../android/icu/util/Calendar.md). The first day of the month has value 1. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DAY_OF_WEEK](../android/icu/util/Calendar.md) <br /> Field number for`get`and`set`indicating the day of the week. This field takes values [SUNDAY](../android/icu/util/Calendar.md), [MONDAY](../android/icu/util/Calendar.md), [TUESDAY](../android/icu/util/Calendar.md), [WEDNESDAY](../android/icu/util/Calendar.md), [THURSDAY](../android/icu/util/Calendar.md), [FRIDAY](../android/icu/util/Calendar.md), and [SATURDAY](../android/icu/util/Calendar.md). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DAY_OF_WEEK_IN_MONTH](../android/icu/util/Calendar.md) <br /> Field number for`get`and`set`indicating the ordinal number of the day of the week within the current month. Together with the [DAY_OF_WEEK](../android/icu/util/Calendar.md) field, this uniquely specifies a day within a month. Unlike [WEEK_OF_MONTH](../android/icu/util/Calendar.md) and [WEEK_OF_YEAR](../android/icu/util/Calendar.md), this field's value does*not* depend on [getFirstDayOfWeek()](../android/icu/util/Calendar.md))or [getMinimalDaysInFirstWeek()](../android/icu/util/Calendar.md)).`DAY_OF_MONTH 1`through`7`always correspond to`DAY_OF_WEEK_IN_MONTH 1`;`8`through`15`correspond to`DAY_OF_WEEK_IN_MONTH 2`, and so on.`DAY_OF_WEEK_IN_MONTH 0`indicates the week before`DAY_OF_WEEK_IN_MONTH 1`. Negative values count back from the end of the month, so the last Sunday of a month is specified as`DAY_OF_WEEK = SUNDAY, DAY_OF_WEEK_IN_MONTH = -1`. Because negative values count backward they will usually be aligned differently within the month than positive values. For example, if a month has 31 days,`DAY_OF_WEEK_IN_MONTH -1`will overlap`DAY_OF_WEEK_IN_MONTH 5`and the end of`4`. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DAY_OF_YEAR](../android/icu/util/Calendar.md) <br /> Field number for`get`and`set`indicating the day number within the current year. The first day of the year has value 1. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DECEMBER](../android/icu/util/Calendar.md) <br /> Value of the`MONTH`field indicating the twelfth month of the year. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DOW_LOCAL](../android/icu/util/Calendar.md) <br /> **\[icu\]** Field number for`get()`and`set()`indicating the localized day of week. This will be a value from 1 to 7 inclusive, with 1 being the localized first day of the week. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DST_OFFSET](../android/icu/util/Calendar.md) <br /> Field number for`get`and`set`indicating the daylight savings offset in milliseconds. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EPOCH_JULIAN_DAY](../android/icu/util/Calendar.md) <br /> The Julian day of the epoch, that is, January 1, 1970 on the Gregorian calendar. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERA](../android/icu/util/Calendar.md) <br /> Field number for`get`and`set`indicating the era, e.g., AD or BC in the Julian calendar. This is a calendar-specific value; see subclass documentation. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EXTENDED_YEAR](../android/icu/util/Calendar.md) <br /> **\[icu\]** Field number for`get()`and`set()`indicating the extended year. This is a single number designating the year of this calendar system, encompassing all supra-year fields. For example, for the Julian calendar system, year numbers are positive, with an era of BCE or CE. An extended year value for the Julian calendar system assigns positive values to CE years and negative values to BCE years, with 1 BCE being year 0. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FEBRUARY](../android/icu/util/Calendar.md) <br /> Value of the`MONTH`field indicating the second month of the year. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FRIDAY](../android/icu/util/Calendar.md) <br /> Value of the`DAY_OF_WEEK`field indicating Friday. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GREATEST_MINIMUM](../android/icu/util/Calendar.md) <br /> Limit type for`getLimit()`and`handleGetLimit()`indicating the greatest minimum value that a field can take. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HOUR](../android/icu/util/Calendar.md) <br /> Field number for`get`and`set`indicating the hour of the morning or afternoon.`HOUR`is used for the 12-hour clock. E.g., at 10:04:15.250 PM the`HOUR`is 10. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HOUR_OF_DAY](../android/icu/util/Calendar.md) <br /> Field number for`get`and`set`indicating the hour of the day.`HOUR_OF_DAY`is used for the 24-hour clock. E.g., at 10:04:15.250 PM the`HOUR_OF_DAY`is 22. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INTERNALLY_SET](../android/icu/util/Calendar.md) <br /> Value of the time stamp`stamp[]`indicating that a field has been set via computations from the time or from other fields. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [IS_LEAP_MONTH](../android/icu/util/Calendar.md) <br /> **\[icu\]**Field indicating whether or not the current month is a leap month. Should have a value of 0 for non-leap months, and 1 for leap months. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [JANUARY](../android/icu/util/Calendar.md) <br /> Value of the`MONTH`field indicating the first month of the year. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [JAN_1_1_JULIAN_DAY](../android/icu/util/Calendar.md) <br /> The Julian day of the Gregorian epoch, that is, January 1, 1 on the Gregorian calendar. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [JULIAN_DAY](../android/icu/util/Calendar.md) <br /> **\[icu\]** Field number for`get()`and`set()`indicating the modified Julian day number. This is different from the conventional Julian day number in two regards. First, it demarcates days at local zone midnight, rather than noon GMT. Second, it is a local number; that is, it depends on the local time zone. It can be thought of as a single number that encompasses all the date-related fields. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [JULY](../android/icu/util/Calendar.md) <br /> Value of the`MONTH`field indicating the seventh month of the year. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [JUNE](../android/icu/util/Calendar.md) <br /> Value of the`MONTH`field indicating the sixth month of the year. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LEAST_MAXIMUM](../android/icu/util/Calendar.md) <br /> Limit type for`getLimit()`and`handleGetLimit()`indicating the least maximum value that a field can take. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MARCH](../android/icu/util/Calendar.md) <br /> Value of the`MONTH`field indicating the third month of the year. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MAXIMUM](../android/icu/util/Calendar.md) <br /> Limit type for`getLimit()`and`handleGetLimit()`indicating the maximum value that a field can take (greatest maximum). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MAX_FIELD_COUNT](../android/icu/util/Calendar.md) <br /> The maximum number of fields possible. Subclasses must not define more total fields than this number. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MAX_JULIAN](../android/icu/util/Calendar.md) <br /> The maximum supported Julian day. This value is equivalent to [MAX_MILLIS](../android/icu/util/Calendar.md) and [MAX_DATE](../android/icu/util/Calendar.md). <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [MAX_MILLIS](../android/icu/util/Calendar.md) <br /> The maximum supported epoch milliseconds. This value is equivalent to [MAX_JULIAN](../android/icu/util/Calendar.md) and [MAX_DATE](../android/icu/util/Calendar.md). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MAY](../android/icu/util/Calendar.md) <br /> Value of the`MONTH`field indicating the fifth month of the year. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MILLISECOND](../android/icu/util/Calendar.md) <br /> Field number for`get`and`set`indicating the millisecond within the second. E.g., at 10:04:15.250 PM the`MILLISECOND`is 250. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MILLISECONDS_IN_DAY](../android/icu/util/Calendar.md) <br /> **\[icu\]** Field number for`get()`and`set()`indicating the milliseconds in the day. This ranges from 0 to 23:59:59.999 (regardless of DST). This field behaves*exactly*like a composite of all time-related fields, not including the zone fields. As such, it also reflects discontinuities of those fields on DST transition days. On a day of DST onset, it will jump forward. On a day of DST cessation, it will jump backward. This reflects the fact that is must be combined with the DST_OFFSET field to obtain a unique local time value. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MINIMUM](../android/icu/util/Calendar.md) <br /> Limit type for`getLimit()`and`handleGetLimit()`indicating the minimum value that a field can take (least minimum). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MINIMUM_USER_STAMP](../android/icu/util/Calendar.md) <br /> If the time stamp`stamp[]`has a value greater than or equal to`MINIMUM_USER_SET`then it has been set by the user via a call to`set()`. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MINUTE](../android/icu/util/Calendar.md) <br /> Field number for`get`and`set`indicating the minute within the hour. E.g., at 10:04:15.250 PM the`MINUTE`is 4. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MIN_JULIAN](../android/icu/util/Calendar.md) <br /> The minimum supported Julian day. This value is equivalent to [MIN_MILLIS](../android/icu/util/Calendar.md) and [MIN_DATE](../android/icu/util/Calendar.md). <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [MIN_MILLIS](../android/icu/util/Calendar.md) <br /> The minimum supported epoch milliseconds. This value is equivalent to [MIN_JULIAN](../android/icu/util/Calendar.md) and [MIN_DATE](../android/icu/util/Calendar.md). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MONDAY](../android/icu/util/Calendar.md) <br /> Value of the`DAY_OF_WEEK`field indicating Monday. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MONTH](../android/icu/util/Calendar.md) <br /> Field number for`get`and`set`indicating the month. This is a calendar-specific value. The first month of the year is`JANUARY`; the last depends on the number of months in a year. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NOVEMBER](../android/icu/util/Calendar.md) <br /> Value of the`MONTH`field indicating the eleventh month of the year. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [OCTOBER](../android/icu/util/Calendar.md) <br /> Value of the`MONTH`field indicating the tenth month of the year. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [ONE_DAY](../android/icu/util/Calendar.md) <br /> The number of milliseconds in one day. Although ONE_DAY and ONE_WEEK can fit into ints, they must be longs in order to prevent arithmetic overflow when performing (bug 4173516). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ONE_HOUR](../android/icu/util/Calendar.md) <br /> The number of milliseconds in one hour. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ONE_MINUTE](../android/icu/util/Calendar.md) <br /> The number of milliseconds in one minute. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ONE_SECOND](../android/icu/util/Calendar.md) <br /> The number of milliseconds in one second. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [ONE_WEEK](../android/icu/util/Calendar.md) <br /> The number of milliseconds in one week. Although ONE_DAY and ONE_WEEK can fit into ints, they must be longs in order to prevent arithmetic overflow when performing (bug 4173516). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ORDINAL_MONTH](../android/icu/util/Calendar.md) <br /> **\[icu\]**Field indicating the month. This is a calendar-specific value. Differ from MONTH, this value is continuous and unique within a year and range from 0 to 11 or 0 to 12 depending on how many months in a year, the calendar system has leap month or not, and in leap year or not. It is the ordinal position of that month in the corresponding year of the calendar. For Chinese, Dangi, and Hebrew calendar, the range is 0 to 11 in non-leap years and 0 to 12 in leap years. For Coptic and Ethiopian calendar, the range is always 0 to 12. For other calendars supported by ICU now, the range is 0 to 11. When the number of months in a year of the identified calendar is variable, a different ORDINAL_MONTH value can be used for dates that are part of the same named month in different years. For example, in the Hebrew calendar, "1 Nisan 5781" is associated with ORDINAL_MONTH value 6 while "1 Nisan 5782" is associated with ORDINAL_MONTH value 7 because 5782 is a leap year and Nisan follows the insertion of Adar I. In Chinese calendar, "Year 4664 Month 6 Day 2" is associated with ORDINAL_MONTH value 5 while "Year 4665 Month 6 Day 2" is associated with ORDINAL_MONTH value 6 because 4665 is a leap year and there is an extra "Leap Month 5" which associated with ORDINAL_MONTH value 5 before "Month 6" of year 4664. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PM](../android/icu/util/Calendar.md) <br /> Value of the`AM_PM`field indicating the period of the day from noon to just before midnight. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESOLVE_REMAP](../android/icu/util/Calendar.md) <br /> Value to OR against resolve table field values for remapping. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SATURDAY](../android/icu/util/Calendar.md) <br /> Value of the`DAY_OF_WEEK`field indicating Saturday. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECOND](../android/icu/util/Calendar.md) <br /> Field number for`get`and`set`indicating the second within the minute. E.g., at 10:04:15.250 PM the`SECOND`is 15. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SEPTEMBER](../android/icu/util/Calendar.md) <br /> Value of the`MONTH`field indicating the ninth month of the year. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SUNDAY](../android/icu/util/Calendar.md) <br /> Value of the`DAY_OF_WEEK`field indicating Sunday. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [THURSDAY](../android/icu/util/Calendar.md) <br /> Value of the`DAY_OF_WEEK`field indicating Thursday. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TUESDAY](../android/icu/util/Calendar.md) <br /> Value of the`DAY_OF_WEEK`field indicating Tuesday. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UNDECIMBER](../android/icu/util/Calendar.md) <br /> Value of the`MONTH`field indicating the thirteenth month of the year. Although [GregorianCalendar](../android/icu/util/GregorianCalendar.md) does not use this value, lunar calendars do. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UNSET](../android/icu/util/Calendar.md) <br /> Value of the time stamp`stamp[]`indicating that a field has not been set since the last call to`clear()`. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WALLTIME_FIRST](../android/icu/util/Calendar.md) <br /> **\[icu\]** Option used by [setRepeatedWallTimeOption(int)](../android/icu/util/Calendar.md))and [setSkippedWallTimeOption(int)](../android/icu/util/Calendar.md))specifying an ambiguous wall time to be interpreted as the earliest. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WALLTIME_LAST](../android/icu/util/Calendar.md) <br /> **\[icu\]** Option used by [setRepeatedWallTimeOption(int)](../android/icu/util/Calendar.md))and [setSkippedWallTimeOption(int)](../android/icu/util/Calendar.md))specifying an ambiguous wall time to be interpreted as the latest. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WALLTIME_NEXT_VALID](../android/icu/util/Calendar.md) <br /> **\[icu\]** Option used by [setSkippedWallTimeOption(int)](../android/icu/util/Calendar.md))specifying an ambiguous wall time to be interpreted as the next valid wall time. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WEDNESDAY](../android/icu/util/Calendar.md) <br /> Value of the`DAY_OF_WEEK`field indicating Wednesday. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WEEK_OF_MONTH](../android/icu/util/Calendar.md) <br /> Field number for`get`and`set`indicating the week number within the current month. The first week of the month, as defined by [getFirstDayOfWeek()](../android/icu/util/Calendar.md))and [getMinimalDaysInFirstWeek()](../android/icu/util/Calendar.md)), has value 1. Subclasses define the value of [WEEK_OF_MONTH](../android/icu/util/Calendar.md) for days before the first week of the month. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WEEK_OF_YEAR](../android/icu/util/Calendar.md) <br /> Field number for`get`and`set`indicating the week number within the current year. The first week of the year, as defined by [getFirstDayOfWeek()](../android/icu/util/Calendar.md))and [getMinimalDaysInFirstWeek()](../android/icu/util/Calendar.md)), has value 1. Subclasses define the value of [WEEK_OF_YEAR](../android/icu/util/Calendar.md) for days before the first week of the year. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [YEAR](../android/icu/util/Calendar.md) <br /> Field number for`get`and`set`indicating the year. This is a calendar-specific value; see subclass documentation. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [YEAR_WOY](../android/icu/util/Calendar.md) <br /> **\[icu\]** Field number for`get()`and`set()`indicating the extended year corresponding to the [WEEK_OF_YEAR](../android/icu/util/Calendar.md) field. This may be one greater or less than the value of [EXTENDED_YEAR](../android/icu/util/Calendar.md). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ZONE_OFFSET](../android/icu/util/Calendar.md) <br /> Field number for`get`and`set`indicating the raw offset from GMT in milliseconds. <br /> | ||

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [HebrewCalendar](../android/icu/util/HebrewCalendar.md))`()` Constructs a default`HebrewCalendar`using the current time in the default time zone with the default`FORMAT`locale. |
| [HebrewCalendar](../android/icu/util/HebrewCalendar.md))`(`zone:` ` [TimeZone](../android/icu/util/TimeZone.md)!`)` Constructs a`HebrewCalendar`based on the current time in the given time zone with the default`FORMAT`locale. |
| [HebrewCalendar](../android/icu/util/HebrewCalendar.md))`(`zone:` ` [TimeZone](../android/icu/util/TimeZone.md)!`, `locale:` ` [ULocale](../android/icu/util/ULocale.md)!`)` Constructs a`HebrewCalendar`based on the current time in the given time zone with the given locale. |
| [HebrewCalendar](../android/icu/util/HebrewCalendar.md))`(`zone:` ` [TimeZone](../android/icu/util/TimeZone.md)!`, `aLocale:` ` [Locale](../java/util/Locale.md)!`)` Constructs a`HebrewCalendar`based on the current time in the given time zone with the given locale. |
| [HebrewCalendar](../android/icu/util/HebrewCalendar.md))`(`locale:` ` [ULocale](../android/icu/util/ULocale.md)!`)` Constructs a`HebrewCalendar`based on the current time in the default time zone with the given locale. |
| [HebrewCalendar](../android/icu/util/HebrewCalendar.md))`(`year:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `month:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `date:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs a`HebrewCalendar`with the given date set in the default time zone with the default`FORMAT`locale. |
| [HebrewCalendar](../android/icu/util/HebrewCalendar.md))`(`year:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `month:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `date:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `hour:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `minute:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `second:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs a`HebrewCalendar`with the given date and time set for the default time zone with the default`FORMAT`locale. |
| [HebrewCalendar](../android/icu/util/HebrewCalendar.md))`(`date:` ` [Date](../java/util/Date.md)!`)` Constructs a`HebrewCalendar`with the given date set in the default time zone with the default`FORMAT`locale. |
| [HebrewCalendar](../android/icu/util/HebrewCalendar.md))`(`aLocale:` ` [Locale](../java/util/Locale.md)!`)` Constructs a`HebrewCalendar`based on the current time in the default time zone with the given locale. |

| Public methods ||
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [add](../android/icu/util/HebrewCalendar.md))`(`field:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `amount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Add a signed amount to a specified field, using this calendar's rules. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getTemporalMonthCode](../android/icu/util/HebrewCalendar.md))`()` Gets The Temporal monthCode value corresponding to the month for the date. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getType](../android/icu/util/HebrewCalendar.md))`()` **\[icu\]**Returns the calendar type name string for this Calendar object. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [inTemporalLeapYear](../android/icu/util/HebrewCalendar.md))`()` **\[icu\]**Returns true if the date is in a leap year. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [roll](../android/icu/util/HebrewCalendar.md))`(`field:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `amount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Rolls (up/down) a specified amount time on the given field. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTemporalMonthCode](../android/icu/util/HebrewCalendar.md))`(`temporalMonth:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets The Temporal monthCode which is a string identifier that starts with the literal grapheme "M" followed by two graphemes representing the zero-padded month number of the current month in a normal (non-leap) year and suffixed by an optional literal grapheme "L" if this is a leap month in a lunisolar calendar. |
| --- | --- |

| Protected methods ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [handleComputeFields](../android/icu/util/HebrewCalendar.md))`(`julianDay:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Subclasses may override this method to compute several fields specific to each calendar system. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [handleComputeMonthStart](../android/icu/util/HebrewCalendar.md))`(`eyear:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `month:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `useMonth:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Return JD of start of given month/year. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [handleGetExtendedYear](../android/icu/util/HebrewCalendar.md))`()` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [handleGetLimit](../android/icu/util/HebrewCalendar.md))`(`field:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `limitType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [handleGetMonthLength](../android/icu/util/HebrewCalendar.md))`(`extendedYear:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `month:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the length of the given month in the given year |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [handleGetYearLength](../android/icu/util/HebrewCalendar.md))`(`eyear:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the number of days in the given Hebrew year |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [Calendar](../android/icu/util/Calendar.md) |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [after](../android/icu/util/Calendar.md))`(`when:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> Compares the time field records. Equivalent to comparing result of conversion to UTC. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [before](../android/icu/util/Calendar.md))`(`when:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> Compares the time field records. Equivalent to comparing result of conversion to UTC. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](../android/icu/util/Calendar.md))`()` <br /> Clears the values of all the time fields. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](../android/icu/util/Calendar.md))`(`field:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Clears the value in the given time field. <br /> | | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [clone](../android/icu/util/Calendar.md))`()` <br /> Overrides Cloneable <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compareTo](../android/icu/util/Calendar.md))`(`other:` ` [Calendar](../android/icu/util/Calendar.md)!`)` <br /> Compares the times (in millis) represented by two`Calendar`objects. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [complete](../android/icu/util/Calendar.md))`()` <br /> Fills in any unset fields in the time field list. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [computeFields](../android/icu/util/Calendar.md))`()` <br /> Converts the current millisecond time value`time`to field values in`fields[]`. This synchronizes the time field values with a new time that is set for the calendar. The time is*not* recomputed first; to recompute the time, then the fields, call the`complete`method. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [computeGregorianFields](../android/icu/util/Calendar.md))`(`julianDay:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Compute the Gregorian calendar year, month, and day of month from the Julian day. These values are not stored in fields, but in member variables gregorianXxx. They are used for time zone computations and by subclasses that are Gregorian derivatives. Subclasses may call this method to perform a Gregorian calendar millis-\>fields computation. To perform a Gregorian calendar fields-\>millis computation, call computeGregorianMonthStart(). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [computeGregorianMonthStart](../android/icu/util/Calendar.md))`(`year:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `month:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Compute the Julian day of a month of the Gregorian calendar. Subclasses may call this method to perform a Gregorian calendar fields-\>millis computation. To perform a Gregorian calendar millis-\>fields computation, call computeGregorianFields(). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [computeJulianDay](../android/icu/util/Calendar.md))`()` <br /> Compute the Julian day number as specified by this calendar's fields. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [computeMillisInDay](../android/icu/util/Calendar.md))`()` <br /> Compute the milliseconds in the day from the fields. This is a value from 0 to 23:59:59.999 inclusive, unless fields are out of range, in which case it can be an arbitrary value. This value reflects local zone wall time. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [computeTime](../android/icu/util/Calendar.md))`()` <br /> Converts the current field values in`fields[]`to the millisecond time value`time`. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [computeZoneOffset](../android/icu/util/Calendar.md))`(`millis:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `millisInDay:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> This method can assume EXTENDED_YEAR has been set. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/icu/util/Calendar.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> Compares this calendar to the specified object. The result is`true`if and only if the argument is not`null`and is a`Calendar`object that represents the same calendar as this object. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [fieldDifference](../android/icu/util/Calendar.md))`(`when:` ` [Date](../java/util/Date.md)!`, `field:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> **\[icu\]** Returns the difference between the given time and the time this calendar object is set to. If this calendar is set*before* the given time, the returned value will be positive. If this calendar is set*after* the given time, the returned value will be negative. The`field`parameter specifies the units of the return value. For example, if`fieldDifference(when, Calendar.MONTH)`returns 3, then this calendar is set to 3 months before , and possibly some additional time less than one month. As a side effect of this call, this calendar is advanced toward`when`by the given amount. That is, calling this method has the side effect of calling`add(field, n)`, where`n`is the return value. Usage: To use this method, call it first with the largest field of interest, then with progressively smaller fields. For example: ```kotlin int y = cal.fieldDifference(when, Calendar.YEAR); int m = cal.fieldDifference(when, Calendar.MONTH); int d = cal.fieldDifference(when, Calendar.DATE); ``` computes the difference between`cal`and`when`in years, months, and days. Note:`fieldDifference()`is*asymmetrical*. That is, in the following code: ```kotlin cal.setTime(date1); int m1 = cal.fieldDifference(date2, Calendar.MONTH); int d1 = cal.fieldDifference(date2, Calendar.DATE); cal.setTime(date2); int m2 = cal.fieldDifference(date1, Calendar.MONTH); int d2 = cal.fieldDifference(date1, Calendar.DATE); ``` one might expect that`m1 == -m2 && d1 == -d2`. However, this is not generally the case, because of irregularities in the underlying calendar system (e.g., the Gregorian calendar has a varying number of days per month). <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [fieldName](../android/icu/util/Calendar.md))`(`field:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Returns a string name for a field, for debugging and exceptions. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [floorDivide](../android/icu/util/Calendar.md))`(`numerator:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `denominator:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Divide two integers, returning the floor of the quotient. Unlike the built-in division, this is mathematically well-behaved. E.g.,`-1/4`=\> 0 but`floorDivide(-1,4)`=\> -1. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [floorDivide](../android/icu/util/Calendar.md))`(`numerator:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `denominator:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `remainder:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` <br /> Divide two integers, returning the floor of the quotient, and the modulus remainder. Unlike the built-in division, this is mathematically well-behaved. E.g.,`-1/4`=\> 0 and`-1%4`=\> -1, but`floorDivide(-1,4)`=\> -1 with`remainder[0]`=\> 3. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [floorDivide](../android/icu/util/Calendar.md))`(`numerator:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `denominator:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `remainder:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` <br /> Divide two integers, returning the floor of the quotient, and the modulus remainder. Unlike the built-in division, this is mathematically well-behaved. E.g.,`-1/4`=\> 0 and`-1%4`=\> -1, but`floorDivide(-1,4)`=\> -1 with`remainder[0]`=\> 3. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [floorDivide](../android/icu/util/Calendar.md))`(`numerator:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `denominator:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Divide two long integers, returning the floor of the quotient. Unlike the built-in division, this is mathematically well-behaved. E.g.,`-1/4`=\> 0 but`floorDivide(-1,4)`=\> -1. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [get](../android/icu/util/Calendar.md))`(`field:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Returns the value for a given time field. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getActualMaximum](../android/icu/util/Calendar.md))`(`field:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Returns the maximum value that this field could have, given the current date. For example, with the Gregorian date February 3, 1997 and the [DAY_OF_MONTH](../android/icu/util/Calendar.md) field, the actual maximum is 28; for February 3, 1996 it is 29. The actual maximum computation ignores smaller fields and the current value of like-sized fields. For example, the actual maximum of the DAY_OF_YEAR or MONTH depends only on the year and supra-year fields. The actual maximum of the DAY_OF_MONTH depends, in addition, on the MONTH field and any other fields at that granularity (such as IS_LEAP_MONTH). The DAY_OF_WEEK_IN_MONTH field does not depend on the current DAY_OF_WEEK; it returns the maximum for any day of week in the current month. Likewise for the WEEK_OF_MONTH and WEEK_OF_YEAR fields. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getActualMinimum](../android/icu/util/Calendar.md))`(`field:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Returns the minimum value that this field could have, given the current date. For most fields, this is the same as [getMinimum](../android/icu/util/Calendar.md))and [getGreatestMinimum](../android/icu/util/Calendar.md)). However, some fields, especially those related to week number, are more complicated. For example, assume [getMinimalDaysInFirstWeek](../android/icu/util/Calendar.md))returns 4 and [getFirstDayOfWeek](../android/icu/util/Calendar.md))returns SUNDAY. If the first day of the month is Sunday, Monday, Tuesday, or Wednesday there will be four or more days in the first week, so it will be week number 1, and`getActualMinimum(WEEK_OF_MONTH)`will return 1. However, if the first of the month is a Thursday, Friday, or Saturday, there are*not* four days in that week, so it is week number 0, and`getActualMinimum(WEEK_OF_MONTH)`will return 0. <br /> <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Locale](../java/util/Locale.md)!>! | [getAvailableLocales](../android/icu/util/Calendar.md))`()` <br /> Returns the list of locales for which Calendars are installed. <br /> | | [DateFormat](../android/icu/text/DateFormat.md)! | [getDateTimeFormat](../android/icu/util/Calendar.md))`(`dateStyle:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `timeStyle:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `loc:` ` [ULocale](../android/icu/util/ULocale.md)!`)` <br /> **\[icu\]** Returns a`DateFormat`appropriate to this calendar. Subclasses wishing to specialize this behavior should override #handleGetDateFormat. <br /> | | [DateFormat](../android/icu/text/DateFormat.md)! | [getDateTimeFormat](../android/icu/util/Calendar.md))`(`dateStyle:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `timeStyle:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `loc:` ` [Locale](../java/util/Locale.md)!`)` <br /> **\[icu\]** Returns a`DateFormat`appropriate to this calendar. Subclasses wishing to specialize this behavior should override #handleGetDateFormat. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDisplayName](../android/icu/util/Calendar.md))`(`loc:` ` [ULocale](../android/icu/util/ULocale.md)!`)` <br /> Returns the name of this calendar in the language of the given locale. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDisplayName](../android/icu/util/Calendar.md))`(`loc:` ` [Locale](../java/util/Locale.md)!`)` <br /> Returns the name of this calendar in the language of the given locale. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getFieldCount](../android/icu/util/Calendar.md))`()` <br /> **\[icu\]** Returns the number of fields defined by this calendar. Valid field arguments to`set()`and`get()`are`0..getFieldCount()-1`. <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!>!>! | [getFieldResolutionTable](../android/icu/util/Calendar.md))`()` <br /> Returns the field resolution array for this calendar. Calendars that define additional fields or change the semantics of existing fields should override this method to adjust the field resolution semantics accordingly. Other subclasses should not override this method. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getFirstDayOfWeek](../android/icu/util/Calendar.md))`()` <br /> Returns what the first day of the week is, where 1 = [SUNDAY](../android/icu/util/Calendar.md) and 7 = [SATURDAY](../android/icu/util/Calendar.md). e.g., Sunday in US, Monday in France <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGreatestMinimum](../android/icu/util/Calendar.md))`(`field:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Returns the highest minimum value for the given field if varies. Otherwise same as getMinimum(). For Gregorian, no difference. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGregorianDayOfMonth](../android/icu/util/Calendar.md))`()` <br /> Returns the day of month (1-based) on the Gregorian calendar as computed by`computeGregorianFields()`. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGregorianDayOfYear](../android/icu/util/Calendar.md))`()` <br /> Returns the day of year (1-based) on the Gregorian calendar as computed by`computeGregorianFields()`. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGregorianMonth](../android/icu/util/Calendar.md))`()` <br /> Returns the month (0-based) on the Gregorian calendar as computed by`computeGregorianFields()`. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGregorianYear](../android/icu/util/Calendar.md))`()` <br /> Returns the extended year on the Gregorian calendar as computed by`computeGregorianFields()`. <br /> | | [Calendar](../android/icu/util/Calendar.md)! | [getInstance](../android/icu/util/Calendar.md))`()` <br /> Returns a calendar using the default time zone and locale. <br /> | | [Calendar](../android/icu/util/Calendar.md)! | [getInstance](../android/icu/util/Calendar.md))`(`zone:` ` [TimeZone](../android/icu/util/TimeZone.md)!`)` <br /> Returns a calendar using the specified time zone and default locale. <br /> | | [Calendar](../android/icu/util/Calendar.md)! | [getInstance](../android/icu/util/Calendar.md))`(`zone:` ` [TimeZone](../android/icu/util/TimeZone.md)!`, `locale:` ` [ULocale](../android/icu/util/ULocale.md)!`)` <br /> Returns a calendar with the specified time zone and locale. <br /> | | [Calendar](../android/icu/util/Calendar.md)! | [getInstance](../android/icu/util/Calendar.md))`(`zone:` ` [TimeZone](../android/icu/util/TimeZone.md)!`, `aLocale:` ` [Locale](../java/util/Locale.md)!`)` <br /> Returns a calendar with the specified time zone and locale. <br /> | | [Calendar](../android/icu/util/Calendar.md)! | [getInstance](../android/icu/util/Calendar.md))`(`locale:` ` [ULocale](../android/icu/util/ULocale.md)!`)` <br /> Returns a calendar using the default time zone and specified locale. <br /> | | [Calendar](../android/icu/util/Calendar.md)! | [getInstance](../android/icu/util/Calendar.md))`(`aLocale:` ` [Locale](../java/util/Locale.md)!`)` <br /> Returns a calendar using the default time zone and specified locale. <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | [getKeywordValuesForLocale](../android/icu/util/Calendar.md))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `locale:` ` [ULocale](../android/icu/util/ULocale.md)!`, `commonlyUsed:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> **\[icu\]**Given a key and a locale, returns an array of string values in a preferred order that would make a difference. These are all and only those values where the open (creation) of the service with the locale formed from the input locale plus input keyword and that value has different behavior than creation with the input locale alone. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLeastMaximum](../android/icu/util/Calendar.md))`(`field:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Returns the lowest maximum value for the given field if varies. Otherwise same as getMaximum(). e.g., for Gregorian DAY_OF_MONTH, 28. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLimit](../android/icu/util/Calendar.md))`(`field:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `limitType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Returns a limit for a field. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaximum](../android/icu/util/Calendar.md))`(`field:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Returns the maximum value for the given time field. e.g. for Gregorian DAY_OF_MONTH, 31. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMinimalDaysInFirstWeek](../android/icu/util/Calendar.md))`()` <br /> Returns what the minimal days required in the first week of the year are. That is, if the first week is defined as one that contains the first day of the first month of a year, getMinimalDaysInFirstWeek returns 1. If the minimal days required must be a full week, getMinimalDaysInFirstWeek returns 7. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMinimum](../android/icu/util/Calendar.md))`(`field:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Returns the minimum value for the given time field. e.g., for Gregorian DAY_OF_MONTH, 1. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRepeatedWallTimeOption](../android/icu/util/Calendar.md))`()` <br /> **\[icu\]**Gets the behavior for handling wall time repeating multiple times at negative time zone offset transitions. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSkippedWallTimeOption](../android/icu/util/Calendar.md))`()` <br /> **\[icu\]**Gets the behavior for handling skipped wall time at positive time zone offset transitions. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getStamp](../android/icu/util/Calendar.md))`(`field:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Returns the timestamp of a field. <br /> | | [Date](../java/util/Date.md)! | [getTime](../android/icu/util/Calendar.md))`()` <br /> Returns this Calendar's current time. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getTimeInMillis](../android/icu/util/Calendar.md))`()` <br /> Returns this Calendar's current time as a long. <br /> | | [TimeZone](../android/icu/util/TimeZone.md)! | [getTimeZone](../android/icu/util/Calendar.md))`()` <br /> Returns the time zone. <br /> | | [Calendar.WeekData](../android/icu/util/Calendar.WeekData.md)! | [getWeekData](../android/icu/util/Calendar.md))`()` <br /> **\[icu\]**Return simple, immutable struct-like class for access to the week data in this calendar. <br /> | | [Calendar.WeekData](../android/icu/util/Calendar.WeekData.md)! | [getWeekDataForRegion](../android/icu/util/Calendar.md))`(`region:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> **\[icu\]**Return simple, immutable struct-like class for access to the CLDR week data. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [gregorianMonthLength](../android/icu/util/Calendar.md))`(`y:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `m:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Returns the length of a month of the Gregorian calendar. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [gregorianPreviousMonthLength](../android/icu/util/Calendar.md))`(`y:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `m:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Returns the length of a previous month of the Gregorian calendar. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [handleComputeJulianDay](../android/icu/util/Calendar.md))`(`bestField:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Subclasses may override this. This method calls handleGetMonthLength() to obtain the calendar-specific month length. <br /> | | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | [handleCreateFields](../android/icu/util/Calendar.md))`()` <br /> Subclasses that use additional fields beyond those defined in`Calendar`should override this method to return an`int[]`array of the appropriate length. The length must be at least`BASE_FIELD_COUNT`and no more than`MAX_FIELD_COUNT`. <br /> | | [DateFormat](../android/icu/text/DateFormat.md)! | [handleGetDateFormat](../android/icu/util/Calendar.md))`(`pattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `locale:` ` [ULocale](../android/icu/util/ULocale.md)!`)` <br /> Creates a`DateFormat`appropriate to this calendar. This is a framework method for subclasses to override. This method is responsible for creating the calendar-specific DateFormat and DateFormatSymbols objects as needed. <br /> | | [DateFormat](../android/icu/text/DateFormat.md)! | [handleGetDateFormat](../android/icu/util/Calendar.md))`(`pattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `override:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `locale:` ` [Locale](../java/util/Locale.md)!`)` <br /> Creates a`DateFormat`appropriate to this calendar. This is a framework method for subclasses to override. This method is responsible for creating the calendar-specific DateFormat and DateFormatSymbols objects as needed. <br /> | | [DateFormat](../android/icu/text/DateFormat.md)! | [handleGetDateFormat](../android/icu/util/Calendar.md))`(`pattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `locale:` ` [Locale](../java/util/Locale.md)!`)` <br /> Creates a`DateFormat`appropriate to this calendar. This is a framework method for subclasses to override. This method is responsible for creating the calendar-specific DateFormat and DateFormatSymbols objects as needed. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/icu/util/Calendar.md))`()` <br /> Returns a hash code for this calendar. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [internalGet](../android/icu/util/Calendar.md))`(`field:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Returns the value for a given time field. This is an internal method for subclasses that does*not*trigger any calculations. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [internalGet](../android/icu/util/Calendar.md))`(`field:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `defaultValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Returns the value for a given time field, or return the given default value if the field is not set. This is an internal method for subclasses that does*not*trigger any calculations. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [internalGetTimeInMillis](../android/icu/util/Calendar.md))`()` <br /> Returns the current milliseconds without recomputing. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [internalSet](../android/icu/util/Calendar.md))`(`field:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Set a field to a value. Subclasses should use this method when computing fields. It sets the time stamp in the`stamp[]`array to`INTERNALLY_SET`. If a field that may not be set by subclasses is passed in, an`IllegalArgumentException`is thrown. This prevents subclasses from modifying fields that are intended to be calendar-system invariant. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEquivalentTo](../android/icu/util/Calendar.md))`(`other:` ` [Calendar](../android/icu/util/Calendar.md)!`)` <br /> **\[icu\]**Returns true if the given Calendar object is equivalent to this one. An equivalent Calendar will behave exactly as this one does, but it may be set to a different time. By contrast, for the equals() method to return true, the other Calendar must be set to the same time. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isGregorianLeapYear](../android/icu/util/Calendar.md))`(`year:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Determines if the given year is a leap year. Returns true if the given year is a leap year. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLenient](../android/icu/util/Calendar.md))`()` <br /> Tell whether date/time interpretation is to be lenient. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSet](../android/icu/util/Calendar.md))`(`field:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Determines if the given time field has a value set. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isWeekend](../android/icu/util/Calendar.md))`()` <br /> **\[icu\]**Returns true if this Calendar's current date and time is in the weekend in this calendar system. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isWeekend](../android/icu/util/Calendar.md))`(`date:` ` [Date](../java/util/Date.md)!`)` <br /> **\[icu\]**Returns true if the given date and time is in the weekend in this calendar system. Equivalent to calling setTime() followed by isWeekend(). Note: This method changes the time this calendar is set to. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [julianDayToDayOfWeek](../android/icu/util/Calendar.md))`(`julian:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Returns the day of week, from SUNDAY to SATURDAY, given a Julian day. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [julianDayToMillis](../android/icu/util/Calendar.md))`(`julian:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Converts Julian day to time as milliseconds. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [millisToJulianDay](../android/icu/util/Calendar.md))`(`millis:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Converts time as milliseconds to Julian day. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [newerField](../android/icu/util/Calendar.md))`(`defaultField:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `alternateField:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Returns the field that is newer, either defaultField, or alternateField. If neither is newer or neither is set, return defaultField. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [newestStamp](../android/icu/util/Calendar.md))`(`first:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `last:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bestStampSoFar:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Returns the newest stamp of a given range of fields. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [pinField](../android/icu/util/Calendar.md))`(`field:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Adjust the specified field so that it is within the allowable range for the date to which this calendar is set. For example, in a Gregorian calendar pinning the [DAY_OF_MONTH](../android/icu/util/Calendar.md) field for a calendar set to April 31 would cause it to be set to April 30. **Subclassing:** This utility method is intended for use by subclasses that need to implement their own overrides of #roll and [add](../android/icu/util/Calendar.md)). **Note:** `pinField`is implemented in terms of [getActualMinimum](../android/icu/util/Calendar.md))and [getActualMaximum](../android/icu/util/Calendar.md)). If either of those methods uses a slow, iterative algorithm for a particular field, it would be unwise to attempt to call`pinField`for that field. If you really do need to do so, you should override this method to do something more efficient for that field. <br /> <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [prepareGetActual](../android/icu/util/Calendar.md))`(`field:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `isMinimum:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Prepare this calendar for computing the actual minimum or maximum. This method modifies this calendar's fields; it is called on a temporary calendar. Rationale: The semantics of getActualXxx() is to return the maximum or minimum value that the given field can take, taking into account other relevant fields. In general these other fields are larger fields. For example, when computing the actual maximum DAY_OF_MONTH, the current value of DAY_OF_MONTH itself is ignored, as is the value of any field smaller. The time fields all have fixed minima and maxima, so we don't need to worry about them. This also lets us set the MILLISECONDS_IN_DAY to zero to erase any effects the time fields might have when computing date fields. DAY_OF_WEEK is adjusted specially for the WEEK_OF_MONTH and WEEK_OF_YEAR fields to ensure that they are computed correctly. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [resolveFields](../android/icu/util/Calendar.md))`(`precedenceTable:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!>!>!`)` <br /> Given a precedence table, return the newest field combination in the table, or -1 if none is found. The precedence table is a 3-dimensional array of integers. It may be thought of as an array of groups. Each group is an array of lines. Each line is an array of field numbers. Within a line, if all fields are set, then the time stamp of the line is taken to be the stamp of the most recently set field. If any field of a line is unset, then the line fails to match. Within a group, the line with the newest time stamp is selected. The first field of the line is returned to indicate which line matched. In some cases, it may be desirable to map a line to field that whose stamp is NOT examined. For example, if the best field is DAY_OF_WEEK then the DAY_OF_WEEK_IN_MONTH algorithm may be used. In order to do this, insert the value`REMAP_RESOLVE | F`at the start of the line, where`F`is the desired return field value. This field will NOT be examined; it only determines the return value if the other fields in the line are the newest. If all lines of a group contain at least one unset field, then no line will match, and the group as a whole will fail to match. In that case, the next group will be processed. If all groups fail to match, then -1 is returned. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [roll](../android/icu/util/Calendar.md))`(`field:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `up:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Rolls (up/down) a single unit of time on the given field. If the field is rolled past its maximum allowable value, it will "wrap" back to its minimum and continue rolling. For example, to roll the current date up by one day, you can call: `roll(` [DATE](../android/icu/util/Calendar.md)`, true)` When rolling on the [YEAR](../android/icu/util/Calendar.md) field, it will roll the year value in the range between 1 and the value returned by calling [getMaximum](../android/icu/util/Calendar.md))([YEAR](../android/icu/util/Calendar.md)). When rolling on certain fields, the values of other fields may conflict and need to be changed. For example, when rolling the`MONTH`field for the Gregorian date 1/31/96 upward, the`DAY_OF_MONTH`field must be adjusted so that the result is 2/29/96 rather than the invalid 2/31/96. Rolling up always means rolling forward in time (unless the limit of the field is reached, in which case it may pin or wrap), so for the Gregorian calendar, starting with 100 BC and rolling the year up results in 99 BC. When eras have a definite beginning and end (as in the Chinese calendar, or as in most eras in the Japanese calendar) then rolling the year past either limit of the era will cause the year to wrap around. When eras only have a limit at one end, then attempting to roll the year past that limit will result in pinning the year at that limit. Note that for most calendars in which era 0 years move forward in time (such as Buddhist, Hebrew, or Islamic), it is possible for add or roll to result in negative years for era 0 (that is the only way to represent years before the calendar epoch in such calendars). **Note:** Calling roll(field, true) N times is*not*necessarily equivalent to calling roll(field, N). For example, imagine that you start with the date Gregorian date January 31, 1995. If you call roll(Calendar.MONTH, 2), the result will be March 31, 1995. But if you call roll(Calendar.MONTH, true), the result will be February 28, 1995. Calling it one more time will give March 28, 1995, which is usually not the desired result. **Note:**You should always use roll and add rather than attempting to perform arithmetic operations directly on the fields of a Calendar. It is quite possible for Calendar subclasses to have fields with non-linear behavior, for example missing months or days during non-leap years. The subclasses' add and roll methods will take this into account, while simple arithmetic manipulations may give invalid results. <br /> <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [set](../android/icu/util/Calendar.md))`(`field:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the time field with the given value. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [set](../android/icu/util/Calendar.md))`(`year:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `month:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `date:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the values for the fields year, month, and date. Previous values of other fields are retained. If this is not desired, call [clear()](../android/icu/util/Calendar.md))first. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [set](../android/icu/util/Calendar.md))`(`year:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `month:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `date:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `hour:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `minute:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the values for the fields year, month, date, hour, and minute. Previous values of other fields are retained. If this is not desired, call [clear()](../android/icu/util/Calendar.md))first. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [set](../android/icu/util/Calendar.md))`(`year:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `month:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `date:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `hour:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `minute:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `second:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the values for the fields year, month, date, hour, minute, and second. Previous values of other fields are retained. If this is not desired, call #clear first. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFirstDayOfWeek](../android/icu/util/Calendar.md))`(`value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets what the first day of the week is, where 1 = [SUNDAY](../android/icu/util/Calendar.md) and 7 = [SATURDAY](../android/icu/util/Calendar.md). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLenient](../android/icu/util/Calendar.md))`(`lenient:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Specify whether or not date/time interpretation is to be lenient. With lenient interpretation, a date such as "February 942, 1996" will be treated as being equivalent to the 941st day after February 1, 1996. With strict interpretation, such dates will cause an exception to be thrown. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMinimalDaysInFirstWeek](../android/icu/util/Calendar.md))`(`value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets what the minimal days required in the first week of the year are. For example, if the first week is defined as one that contains the first day of the first month of a year, call the method with value 1. If it must be a full week, use value 7. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRepeatedWallTimeOption](../android/icu/util/Calendar.md))`(`option:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> **\[icu\]** Sets the behavior for handling wall time repeating multiple times at negative time zone offset transitions. For example, 1:30 AM on November 6, 2011 in US Eastern time (America/New_York) occurs twice; 1:30 AM EDT, then 1:30 AM EST one hour later. When`WALLTIME_FIRST`is used, the wall time 1:30AM in this example will be interpreted as 1:30 AM EDT (first occurrence). When`WALLTIME_LAST`is used, it will be interpreted as 1:30 AM EST (last occurrence). The default value is`WALLTIME_LAST`. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSkippedWallTimeOption](../android/icu/util/Calendar.md))`(`option:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> **\[icu\]** Sets the behavior for handling skipped wall time at positive time zone offset transitions. For example, 2:30 AM on March 13, 2011 in US Eastern time (America/New_York) does not exist because the wall time jump from 1:59 AM EST to 3:00 AM EDT. When`WALLTIME_FIRST`is used, 2:30 AM is interpreted as 30 minutes before 3:00 AM EDT, therefore, it will be resolved as 1:30 AM EST. When`WALLTIME_LAST`is used, 2:30 AM is interpreted as 31 minutes after 1:59 AM EST, therefore, it will be resolved as 3:30 AM EDT. When`WALLTIME_NEXT_VALID`is used, 2:30 AM will be resolved as next valid wall time, that is 3:00 AM EDT. The default value is`WALLTIME_LAST`. **Note:** This option is effective only when this calendar is [lenient](../android/icu/util/Calendar.md)). When the calendar is strict, such non-existing wall time will cause an exception. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTime](../android/icu/util/Calendar.md))`(`date:` ` [Date](../java/util/Date.md)!`)` <br /> Sets this Calendar's current time with the given Date. Note: Calling`setTime`with`Date(Long.MAX_VALUE)`or`Date(Long.MIN_VALUE)`may yield incorrect field values from [get(int)](../android/icu/util/Calendar.md)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTimeInMillis](../android/icu/util/Calendar.md))`(`millis:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Sets this Calendar's current time from the given long value. An IllegalIcuArgumentException is thrown when millis is outside the range permitted by a Calendar object when in strict mode. When in lenient mode the out of range values are pinned to their respective min/max. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTimeZone](../android/icu/util/Calendar.md))`(`value:` ` [TimeZone](../android/icu/util/TimeZone.md)!`)` <br /> Sets the time zone with the given time zone value. <br /> | | [Calendar](../android/icu/util/Calendar.md)! | [setWeekData](../android/icu/util/Calendar.md))`(`wdata:` ` [Calendar.WeekData](../android/icu/util/Calendar.WeekData.md)!`)` <br /> **\[icu\]**Set data in this calendar based on the WeekData input. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/icu/util/Calendar.md))`()` <br /> Returns a string representation of this calendar. This method is intended to be used only for debugging purposes, and the format of the returned string may vary between implementations. The returned string may be empty but may not be`null`. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [validateField](../android/icu/util/Calendar.md))`(`field:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `min:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `max:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Validate a single field of this calendar given its minimum and maximum allowed value. If the field is out of range, throw a descriptive`IllegalArgumentException`. Subclasses may use this method in their implementation of [validateField(int)](../android/icu/util/Calendar.md)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [validateFields](../android/icu/util/Calendar.md))`()` <br /> Ensure that each field is within its valid range by calling [validateField(int)](../android/icu/util/Calendar.md))on each field that has been set. This method should only be called if this calendar is not lenient. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [weekNumber](../android/icu/util/Calendar.md))`(`dayOfPeriod:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dayOfWeek:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Returns the week number of a day, within a period. This may be the week number in a year, or the week number in a month. Usually this will be a value \>= 1, but if some initial days of the period are excluded from week 1, because [getMinimalDaysInFirstWeek](../android/icu/util/Calendar.md))is \> 1, then the week number will be zero for those initial days. This method requires the day of week for the given date in order to determine the result. **Subclassing:** This method is intended for use by subclasses in implementing their [computeTime](../android/icu/util/Calendar.md))and/or [computeFields](../android/icu/util/Calendar.md))methods. It is often useful in [getActualMinimum](../android/icu/util/Calendar.md))and [getActualMaximum](../android/icu/util/Calendar.md))as well. <br /> <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [weekNumber](../android/icu/util/Calendar.md))`(`desiredDay:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dayOfPeriod:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dayOfWeek:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Returns the week number of a day, within a period. This may be the week number in a year or the week number in a month. Usually this will be a value \>= 1, but if some initial days of the period are excluded from week 1, because [getMinimalDaysInFirstWeek](../android/icu/util/Calendar.md))is \> 1, then the week number will be zero for those initial days. This method requires the day number and day of week for some known date in the period in order to determine the day of week on the desired day. **Subclassing:** This method is intended for use by subclasses in implementing their [computeTime](../android/icu/util/Calendar.md))and/or [computeFields](../android/icu/util/Calendar.md))methods. It is often useful in [getActualMinimum](../android/icu/util/Calendar.md))and [getActualMaximum](../android/icu/util/Calendar.md))as well. This variant is handy for computing the week number of some other day of a period (often the first or last day of the period) when its day of the week is not known but the day number and day of week for some other day in the period (e.g. the current date)*is*known. <br /> <br /> | ||

| Inherited properties ||
|---|---|
| From class [Calendar](../android/icu/util/Calendar.md) |------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Date](../java/util/Date.md)! | [MAX_DATE](../android/icu/util/Calendar.md) <br /> The maximum supported`Date`. This value is equivalent to [MAX_JULIAN](../android/icu/util/Calendar.md) and [MAX_MILLIS](../android/icu/util/Calendar.md). <br /> | | [Date](../java/util/Date.md)! | [MIN_DATE](../android/icu/util/Calendar.md) <br /> The minimum supported`Date`. This value is equivalent to [MIN_JULIAN](../android/icu/util/Calendar.md) and [MIN_MILLIS](../android/icu/util/Calendar.md). <br /> | ||

## Constants

### ADAR

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ADAR: Int
```

Constant for the Adar, the 7th month of the Hebrew year. 

 Value: 6

### ADAR_1

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ADAR_1: Int
```

Constant for Adar I, the 6th month of the Hebrew year (present in leap years only). In non-leap years, the calendar jumps from Shevat (5th month) to Adar (7th month). 

 Value: 5

### AV

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AV: Int
```

Constant for Av, the 12th month of the Hebrew year. 

 Value: 11

### ELUL

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ELUL: Int
```

Constant for Elul, the 13th month of the Hebrew year. 

 Value: 12

### HESHVAN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HESHVAN: Int
```

Constant for Heshvan, the 2nd month of the Hebrew year. 

 Value: 1

### IYAR

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val IYAR: Int
```

Constant for Iyar, the 9th month of the Hebrew year. 

 Value: 8

### KISLEV

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KISLEV: Int
```

Constant for Kislev, the 3rd month of the Hebrew year. 

 Value: 2

### NISAN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NISAN: Int
```

Constant for Nisan, the 8th month of the Hebrew year. 

 Value: 7

### SHEVAT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SHEVAT: Int
```

Constant for Shevat, the 5th month of the Hebrew year. 

 Value: 4

### SIVAN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SIVAN: Int
```

Constant for Sivan, the 10th month of the Hebrew year. 

 Value: 9

### TAMUZ

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAMUZ: Int
```

Constant for Tammuz, the 11th month of the Hebrew year. 

 Value: 10

### TEVET

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TEVET: Int
```

Constant for Tevet, the 4th month of the Hebrew year. 

 Value: 3

### TISHRI

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TISHRI: Int
```

Constant for Tishri, the 1st month of the Hebrew year. 

 Value: 0

## Public constructors

### HebrewCalendar

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
HebrewCalendar()
```

Constructs a default`HebrewCalendar`using the current time in the default time zone with the default`FORMAT`locale. 
**See Also**

- [android.icu.util.ULocale.Category#FORMAT](../android/icu/util/ULocale.Category.md) 

### HebrewCalendar

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
HebrewCalendar(zone: TimeZone!)
```

Constructs a`HebrewCalendar`based on the current time in the given time zone with the default`FORMAT`locale.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------|
| `zone` | [TimeZone](../android/icu/util/TimeZone.md)!:The time zone for the new calendar. |

**See Also**

- [android.icu.util.ULocale.Category#FORMAT](../android/icu/util/ULocale.Category.md) 

### HebrewCalendar

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
HebrewCalendar(
    zone: TimeZone!, 
    locale: ULocale!)
```

Constructs a`HebrewCalendar`based on the current time in the given time zone with the given locale.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------|
| `zone` | [TimeZone](../android/icu/util/TimeZone.md)!:The time zone for the new calendar. |
| `locale` | [ULocale](../android/icu/util/ULocale.md)!:The locale for the new calendar. |

### HebrewCalendar

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
HebrewCalendar(
    zone: TimeZone!, 
    aLocale: Locale!)
```

Constructs a`HebrewCalendar`based on the current time in the given time zone with the given locale.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------|
| `zone` | [TimeZone](../android/icu/util/TimeZone.md)!:The time zone for the new calendar. |
| `aLocale` | [Locale](../java/util/Locale.md)!:The locale for the new calendar. |

### HebrewCalendar

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
HebrewCalendar(locale: ULocale!)
```

Constructs a`HebrewCalendar`based on the current time in the default time zone with the given locale.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------|
| `locale` | [ULocale](../android/icu/util/ULocale.md)!:The locale for the new calendar. |

### HebrewCalendar

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
HebrewCalendar(
    year: Int, 
    month: Int, 
    date: Int)
```

Constructs a`HebrewCalendar`with the given date set in the default time zone with the default`FORMAT`locale.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `year` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The value used to set the calendar's [YEAR](../android/icu/util/Calendar.md) time field. |
| `month` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The value used to set the calendar's [MONTH](../android/icu/util/Calendar.md) time field. The value is 0-based. e.g., 0 for Tishri. |
| `date` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The value used to set the calendar's [DATE](../android/icu/util/Calendar.md) time field. |
| --- | --- |

**See Also**

- [android.icu.util.ULocale.Category#FORMAT](../android/icu/util/ULocale.Category.md) 

### HebrewCalendar

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
HebrewCalendar(
    year: Int, 
    month: Int, 
    date: Int, 
    hour: Int, 
    minute: Int, 
    second: Int)
```

Constructs a`HebrewCalendar`with the given date and time set for the default time zone with the default`FORMAT`locale.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `year` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The value used to set the calendar's [YEAR](../android/icu/util/Calendar.md) time field. |
| `month` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The value used to set the calendar's [MONTH](../android/icu/util/Calendar.md) time field. The value is 0-based. e.g., 0 for Tishri. |
| `date` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The value used to set the calendar's [DATE](../android/icu/util/Calendar.md) time field. |
| --- | --- |
| `hour` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The value used to set the calendar's [HOUR_OF_DAY](../android/icu/util/Calendar.md) time field. |
| `minute` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The value used to set the calendar's [MINUTE](../android/icu/util/Calendar.md) time field. |
| `second` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The value used to set the calendar's [SECOND](../android/icu/util/Calendar.md) time field. |
| --- | --- |

**See Also**

- [android.icu.util.ULocale.Category#FORMAT](../android/icu/util/ULocale.Category.md) 

### HebrewCalendar

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
HebrewCalendar(date: Date!)
```

Constructs a`HebrewCalendar`with the given date set in the default time zone with the default`FORMAT`locale.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------|
| `date` | [Date](../java/util/Date.md)!:The date to which the new calendar is set. |

**See Also**

- [android.icu.util.ULocale.Category#FORMAT](../android/icu/util/ULocale.Category.md) 

### HebrewCalendar

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
HebrewCalendar(aLocale: Locale!)
```

Constructs a`HebrewCalendar`based on the current time in the default time zone with the given locale.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------|
| `aLocale` | [Locale](../java/util/Locale.md)!:The locale for the new calendar. |

## Public methods

### add

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun add(
    field: Int, 
    amount: Int
): Unit
```

Add a signed amount to a specified field, using this calendar's rules. For example, to add three days to the current date, you can call`add(Calendar.DATE, 3)`.

When adding to certain fields, the values of other fields may conflict and need to be changed. For example, when adding one to the [MONTH](../android/icu/util/Calendar.md) field for the date "30 Av 5758", the [DAY_OF_MONTH](../android/icu/util/Calendar.md) field must be adjusted so that the result is "29 Elul 5758" rather than the invalid "30 Elul 5758".

This method is able to add to all fields except for [ERA](../android/icu/util/Calendar.md), [DST_OFFSET](../android/icu/util/Calendar.md), and [ZONE_OFFSET](../android/icu/util/Calendar.md).

**Note:** You should always use #roll and add rather than attempting to perform arithmetic operations directly on the fields of a HebrewCalendar. Since the [MONTH](../android/icu/util/Calendar.md) field behaves discontinuously in non-leap years, simple arithmetic can give invalid results.

<br />

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------|
| `field` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the time field. |
| `amount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the amount to add to the field. |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the field is invalid or refers to a field that cannot be handled by this method. |

### getTemporalMonthCode

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTemporalMonthCode(): String!
```

Gets The Temporal monthCode value corresponding to the month for the date. The value is a string identifier that starts with the literal grapheme "M" followed by two graphemes representing the zero-padded month number of the current month in a normal (non-leap) year and suffixed by an optional literal grapheme "L" if this is a leap month in a lunisolar calendar. For the Hebrew calendar, the values are "M01" .. "M12" for non-leap year, and "M01" .. "M05", "M05L", "M06" .. "M12" for leap year.

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | One of 13 possible strings in {"M01".. "M05", "M05L", "M06" .. "M12"}. |

### getType

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getType(): String!
```

**\[icu\]**Returns the calendar type name string for this Calendar object. The returned string is the legacy ICU calendar attribute value, for example, "gregorian" or "japanese".

See type="old type name" for the calendar attribute of locale IDs at http://www.unicode.org/reports/tr35/#Key_Type_Definitions

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | legacy calendar type name string |

### inTemporalLeapYear

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun inTemporalLeapYear(): Boolean
```

**\[icu\]**Returns true if the date is in a leap year. Recalculate the current time field values if the time value has been changed by a call to \* setTime(). This method is semantically const, but may alter the object in memory. A "leap year" is a year that contains more days than other years (for solar or lunar calendars) or more months than other years (for lunisolar calendars like Hebrew or Chinese), as defined in the ECMAScript Temporal proposal.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the date in the fields is in a Temporal proposal defined leap year. False otherwise. |

### roll

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun roll(
    field: Int, 
    amount: Int
): Unit
```

Rolls (up/down) a specified amount time on the given field. For example, to roll the current date up by three days, you can call`roll(Calendar.DATE, 3)`. If the field is rolled past its maximum allowable value, it will "wrap" back to its minimum and continue rolling. For example, calling`roll(Calendar.DATE, 10)`on a Hebrew calendar set to "25 Av 5758" will result in the date "5 Av 5758".

When rolling certain fields, the values of other fields may conflict and need to be changed. For example, when rolling the [MONTH](../android/icu/util/Calendar.md) field upward by one for the date "30 Av 5758", the [DAY_OF_MONTH](../android/icu/util/Calendar.md) field must be adjusted so that the result is "29 Elul 5758" rather than the invalid "30 Elul".

This method is able to roll all fields except for [ERA](../android/icu/util/Calendar.md), [DST_OFFSET](../android/icu/util/Calendar.md), and [ZONE_OFFSET](../android/icu/util/Calendar.md). Subclasses may, of course, add support for additional fields in their overrides of`roll`.

**Note:** You should always use roll and [add](../android/icu/util/HebrewCalendar.md))rather than attempting to perform arithmetic operations directly on the fields of a HebrewCalendar. Since the [MONTH](../android/icu/util/Calendar.md) field behaves discontinuously in non-leap years, simple arithmetic can give invalid results.

<br />

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------|
| `field` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the time field. |
| `amount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the amount by which the field should be rolled. |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the field is invalid or refers to a field that cannot be handled by this method. |

### setTemporalMonthCode

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTemporalMonthCode(temporalMonth: String!): Unit
```

Sets The Temporal monthCode which is a string identifier that starts with the literal grapheme "M" followed by two graphemes representing the zero-padded month number of the current month in a normal (non-leap) year and suffixed by an optional literal grapheme "L" if this is a leap month in a lunisolar calendar. For Hebrew calendar, the values are "M01" .. "M12" for non-leap years, and "M01" .. "M05", "M05L", "M06" .. "M12" for leap year.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------------------------|
| `temporalMonth` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The value to be set for temporal monthCode. |

## Protected methods

### handleComputeFields

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun handleComputeFields(julianDay: Int): Unit
```

Subclasses may override this method to compute several fields specific to each calendar system. These are:

- ERA
- YEAR
- MONTH
- DAY_OF_MONTH
- DAY_OF_YEAR
- EXTENDED_YEAR

Subclasses can refer to the DAY_OF_WEEK and DOW_LOCAL fields, which will be set when this method is called. Subclasses can also call the getGregorianXxx() methods to obtain Gregorian calendar equivalents for the given Julian day.

<br />

In addition, subclasses should compute any subclass-specific fields, that is, fields from BASE_FIELD_COUNT to getFieldCount() - 1. 

### handleComputeMonthStart

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun handleComputeMonthStart(
    eyear: Int, 
    month: Int, 
    useMonth: Boolean
): Int
```

Return JD of start of given month/year.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `eyear` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the extended year |
| `month` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the zero-based month, or 0 if useMonth is false |
| `useMonth` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):if false, compute the day before the first day of the given year, otherwise, compute the day before the first day of the given month |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the Julian day number of the day before the first day of the given month and year |

### handleGetExtendedYear

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun handleGetExtendedYear(): Int
```

| Return ||
|----------------------------------------------------------------------------|-------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the extended year |

### handleGetLimit

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun handleGetLimit(
    field: Int, 
    limitType: Int
): Int
```

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `field` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):one of the above field numbers |
| `limitType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):one of`MINIMUM`,`GREATEST_MINIMUM`,`LEAST_MAXIMUM`, or`MAXIMUM` |

### handleGetMonthLength

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun handleGetMonthLength(
    extendedYear: Int, 
    month: Int
): Int
```

Returns the length of the given month in the given year 

### handleGetYearLength

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun handleGetYearLength(eyear: Int): Int
```

Returns the number of days in the given Hebrew year
