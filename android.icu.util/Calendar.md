Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Calendar

Kotlin | [Java](https://developer.android.com/reference/android/icu/util/Calendar "View this page in Java")
| --- | --- |

```
abstract class Calendar : Cloneable, Comparable<Calendar!>, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.icu.util.Calendar](https://developer.android.com/reference/kotlin/android/icu/util/Calendar#) |

| Known Direct Subclasses [ChineseCalendar](https://developer.android.com/reference/kotlin/android/icu/util/ChineseCalendar), [CopticCalendar](https://developer.android.com/reference/kotlin/android/icu/util/CopticCalendar), [EthiopicCalendar](https://developer.android.com/reference/kotlin/android/icu/util/EthiopicCalendar), [GregorianCalendar](https://developer.android.com/reference/kotlin/android/icu/util/GregorianCalendar), [HebrewCalendar](https://developer.android.com/reference/kotlin/android/icu/util/HebrewCalendar), [IndianCalendar](https://developer.android.com/reference/kotlin/android/icu/util/IndianCalendar), [IslamicCalendar](https://developer.android.com/reference/kotlin/android/icu/util/IslamicCalendar) |---|---| | [ChineseCalendar](https://developer.android.com/reference/kotlin/android/icu/util/ChineseCalendar) | `ChineseCalendar` is a concrete subclass of `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#` that implements a traditional Chinese calendar. | | [CopticCalendar](https://developer.android.com/reference/kotlin/android/icu/util/CopticCalendar) | Implement the Coptic calendar system. | | [EthiopicCalendar](https://developer.android.com/reference/kotlin/android/icu/util/EthiopicCalendar) | Implement the Ethiopic calendar system. | | [GregorianCalendar](https://developer.android.com/reference/kotlin/android/icu/util/GregorianCalendar) | **\[icu enhancement\]** ICU's replacement for `https://developer.android.com/reference/kotlin/java/util/GregorianCalendar.html#`. | | [HebrewCalendar](https://developer.android.com/reference/kotlin/android/icu/util/HebrewCalendar) | `HebrewCalendar` is a subclass of `Calendar` that that implements the traditional Hebrew calendar. | | [IndianCalendar](https://developer.android.com/reference/kotlin/android/icu/util/IndianCalendar) | `IndianCalendar` is a subclass of `GregorianCalendar` that numbers years since the birth of the Buddha. | | [IslamicCalendar](https://developer.android.com/reference/kotlin/android/icu/util/IslamicCalendar) | `IslamicCalendar` is a subclass of `Calendar` that that implements the Islamic civil and religious calendars. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [BuddhistCalendar](https://developer.android.com/reference/kotlin/android/icu/util/BuddhistCalendar), [JapaneseCalendar](https://developer.android.com/reference/kotlin/android/icu/util/JapaneseCalendar), [TaiwanCalendar](https://developer.android.com/reference/kotlin/android/icu/util/TaiwanCalendar) |---|---| | [BuddhistCalendar](https://developer.android.com/reference/kotlin/android/icu/util/BuddhistCalendar) | `BuddhistCalendar` is a subclass of `GregorianCalendar` that numbers years since the birth of the Buddha. | | [JapaneseCalendar](https://developer.android.com/reference/kotlin/android/icu/util/JapaneseCalendar) | `JapaneseCalendar` is a subclass of `GregorianCalendar` that numbers years and eras based on the reigns of the Japanese emperors. | | [TaiwanCalendar](https://developer.android.com/reference/kotlin/android/icu/util/TaiwanCalendar) | `TaiwanCalendar` is a subclass of `GregorianCalendar` that numbers years since 1912. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

**\[icu enhancement\]** ICU's replacement for `https://developer.android.com/reference/kotlin/java/util/Calendar.html#`. Methods, fields, and other functionality specific to ICU are labeled '**\[icu\]**'.

`Calendar` is an abstract base class for converting between a `Date` object and a set of integer fields such as `YEAR`, `MONTH`, `DAY`, `HOUR`, and so on. (A `Date` object represents a specific instant in time with millisecond precision. See `https://developer.android.com/reference/kotlin/java/util/Date.html#` for information about the `Date` class.)

Subclasses of `Calendar` interpret a `Date` according to the rules of a specific calendar system. ICU4J contains several subclasses implementing different international calendar systems.

Like other locale-sensitive classes, `Calendar` provides a class method, `getInstance`, for getting a generally useful object of this type. `Calendar`'s `getInstance` method returns a calendar of a type appropriate to the locale, whose time fields have been initialized with the current date and time:

```kotlin
Calendar rightNow = Calendar.getInstance()
```

When a `ULocale` is used by `getInstance`, its '`calendar`' tag and value are retrieved if present. If a recognized value is supplied, a calendar is provided and configured as appropriate. Currently recognized tags are "buddhist", "chinese", "coptic", "ethiopic", "gregorian", "hebrew", "islamic", "islamic-civil", "japanese", and "roc". For example:

```kotlin
Calendar cal = Calendar.getInstance(new ULocale("en_US@calendar=japanese"));
```
will return an instance of JapaneseCalendar (using en_US conventions for minimum days in first week, start day of week, et cetera).

A `Calendar` object can produce all the time field values needed to implement the date-time formatting for a particular language and calendar style (for example, Japanese-Gregorian, Japanese-Traditional). `Calendar` defines the range of values returned by certain fields, as well as their meaning. For example, the first month of the year has value `MONTH` == `JANUARY` for all calendars. Other values are defined by the concrete subclass, such as `ERA` and `YEAR`. See individual field documentation and subclass documentation for details.

When a `Calendar` is *lenient* , it accepts a wider range of field values than it produces. For example, a lenient `GregorianCalendar` interprets `MONTH` == `JANUARY`, `DAY_OF_MONTH` == 32 as February 1. A non-lenient `GregorianCalendar` throws an exception when given out-of-range field settings. When calendars recompute field values for return by `get()`, they normalize them. For example, a `GregorianCalendar` always produces `DAY_OF_MONTH` values between 1 and the length of the month.

`Calendar` defines a locale-specific seven day week using two parameters: the first day of the week and the minimal days in first week (from 1 to 7). These numbers are taken from the locale resource data when a `Calendar` is constructed. They may also be specified explicitly through the API.

When setting or getting the `WEEK_OF_MONTH` or `WEEK_OF_YEAR` fields, `Calendar` must determine the first week of the month or year as a reference point. The first week of a month or year is defined as the earliest seven day period beginning on `getFirstDayOfWeek()` and containing at least `getMinimalDaysInFirstWeek()` days of that month or year. Weeks numbered ..., -1, 0 precede the first week; weeks numbered 2, 3,... follow it. Note that the normalized numbering returned by `get()` may be different. For example, a specific `Calendar` subclass may designate the week before week 1 of a year as week *n* of the previous year.

When computing a `Date` from time fields, some special circumstances may arise: there may be insufficient information to compute the `Date` (such as only year and month but no day in the month), there may be inconsistent information (such as "Tuesday, July 15, 1996" -- July 15, 1996 is actually a Monday), or the input time might be ambiguous because of time zone transition.

**Insufficient information.** The calendar will use default information to specify the missing fields. This may vary by calendar; for the Gregorian calendar, the default for a field is the same as that of the start of the epoch: i.e., YEAR = 1970, MONTH = JANUARY, DATE = 1, etc.

**Inconsistent information.** If fields conflict, the calendar will give preference to fields set more recently. For example, when determining the day, the calendar will look for one of the following combinations of fields. The most recent combination, as determined by the most recently set single field, will be used.

```kotlin
MONTH + DAY_OF_MONTH
  MONTH + WEEK_OF_MONTH + DAY_OF_WEEK
  MONTH + DAY_OF_WEEK_IN_MONTH + DAY_OF_WEEK
  DAY_OF_YEAR
  DAY_OF_WEEK + WEEK_OF_YEAR
```
For the time of day:

```kotlin
HOUR_OF_DAY
  AM_PM + HOUR
```

**Ambiguous Wall Clock Time.** When time offset from UTC has changed, it produces an ambiguous time slot around the transition. For example, many US locations observe daylight saving time. On the date switching to daylight saving time in US, wall clock time jumps from 12:59 AM (standard) to 2:00 AM (daylight). Therefore, wall clock time from 1:00 AM to 1:59 AM do not exist on the date. When the input wall time fall into this missing time slot, the ICU Calendar resolves the time using the UTC offset before the transition by default. In this example, 1:30 AM is interpreted as 1:30 AM standard time (non-exist), so the final result will be 2:30 AM daylight time.

On the date switching back to standard time, wall clock time is moved back one hour at 2:00 AM. So wall clock time from 1:00 AM to 1:59 AM occur twice. In this case, the ICU Calendar resolves the time using the UTC offset after the transition by default. For example, 1:30 AM on the date is resolved as 1:30 AM standard time.

Ambiguous wall clock time resolution behaviors can be customized by Calendar APIs `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#setRepeatedWallTimeOption(kotlin.Int)` and `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#setSkippedWallTimeOption(kotlin.Int)`. These methods are available in ICU 49 or later versions.

**Note:** for some non-Gregorian calendars, different fields may be necessary for complete disambiguation. For example, a full specification of the historial Arabic astronomical calendar requires year, month, day-of-month *and* day-of-week in some cases.

**Note:** There are certain possible ambiguities in interpretation of certain singular times, which are resolved in the following ways:

1. 24:00:00 "belongs" to the following day. That is, 23:59 on Dec 31, 1969 \< 24:00 on Jan 1, 1970 \< 24:01:00 on Jan 1, 1970
2. Although historically not precise, midnight also belongs to "am", and noon belongs to "pm", so on the same day, 12:00 am (midnight) \< 12:01 am, and 12:00 pm (noon) \< 12:01 pm

The date or time format strings are not part of the definition of a calendar, as those must be modifiable or overridable by the user at runtime. Use `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat.html#` to format dates.

**Field manipulation methods**

`Calendar` fields can be changed using three methods: `set()`, `add()`, and `roll()`.

**`set(f, value)`** changes field `f` to `value`. In addition, it sets an internal member variable to indicate that field `f` has been changed. Although field `f` is changed immediately, the calendar's milliseconds is not recomputed until the next call to `get()`, `getTime()`, or `getTimeInMillis()` is made. Thus, multiple calls to `set()` do not trigger multiple, unnecessary computations. As a result of changing a field using `set()`, other fields may also change, depending on the field, the field value, and the calendar system. In addition, `get(f)` will not necessarily return `value` after the fields have been recomputed. The specifics are determined by the concrete calendar class.

*Example* : Consider a `GregorianCalendar` originally set to August 31, 1999. Calling `set(Calendar.MONTH, Calendar.SEPTEMBER)` sets the calendar to September 31, 1999. This is a temporary internal representation that resolves to October 1, 1999 if `getTime()`is then called. However, a call to `set(Calendar.DAY_OF_MONTH, 30)` before the call to `getTime()` sets the calendar to September 30, 1999, since no recomputation occurs after `set()` itself.

**`add(f, delta)`** adds `delta` to field `f`. This is equivalent to calling `set(f, get(f) + delta)` with two adjustments:

**Add rule 1** . The value of field `f` after the call minus the value of field `f` before the call is `delta`, modulo any overflow that has occurred in field `f`. Overflow occurs when a field value exceeds its range and, as a result, the next larger field is incremented or decremented and the field value is adjusted back into its range.

**Add rule 2** . If a smaller field is expected to be invariant, but it is impossible for it to be equal to its prior value because of changes in its minimum or maximum after field `f` is changed, then its value is adjusted to be as close as possible to its expected value. A smaller field represents a smaller unit of time. `HOUR` is a smaller field than `DAY_OF_MONTH`. No adjustment is made to smaller fields that are not expected to be invariant. The calendar system determines what fields are expected to be invariant.

In addition, unlike `set()`, `add()` forces an immediate recomputation of the calendar's milliseconds and all fields.

*Example* : Consider a `GregorianCalendar` originally set to August 31, 1999. Calling `add(Calendar.MONTH, 13)` sets the calendar to September 30, 2000. **Add rule 1** sets the `MONTH` field to September, since adding 13 months to August gives September of the next year. Since `DAY_OF_MONTH` cannot be 31 in September in a `GregorianCalendar`, **add rule 2** sets the `DAY_OF_MONTH` to 30, the closest possible value. Although it is a smaller field, `DAY_OF_WEEK` is not adjusted by rule 2, since it is expected to change when the month changes in a `GregorianCalendar`.

**`roll(f, delta)`** adds `delta` to field `f` without changing larger fields. This is equivalent to calling `add(f, delta)` with the following adjustment:

**Roll rule** . Larger fields are unchanged after the call. A larger field represents a larger unit of time. `DAY_OF_MONTH` is a larger field than `HOUR`.

*Example* : Consider a `GregorianCalendar` originally set to August 31, 1999. Calling `roll(Calendar.MONTH, 8)` sets the calendar to April 30, **1999** . Add rule 1 sets the `MONTH` field to April. Using a `GregorianCalendar`, the `DAY_OF_MONTH` cannot be 31 in the month April. Add rule 2 sets it to the closest possible value, 30. Finally, the **roll rule** maintains the `YEAR` field value of 1999.

*Example* : Consider a `GregorianCalendar` originally set to Sunday June 6, 1999. Calling `roll(Calendar.WEEK_OF_MONTH, -1)` sets the calendar to Tuesday June 1, 1999, whereas calling `add(Calendar.WEEK_OF_MONTH, -1)` sets the calendar to Sunday May 30, 1999. This is because the roll rule imposes an additional constraint: The `MONTH` must not change when the `WEEK_OF_MONTH` is rolled. Taken together with add rule 1, the resultant date must be between Tuesday June 1 and Saturday June 5. According to add rule 2, the `DAY_OF_WEEK`, an invariant when changing the `WEEK_OF_MONTH`, is set to Tuesday, the closest possible value to Sunday (where Sunday is the first day of the week).

**Usage model** . To motivate the behavior of `add()` and `roll()`, consider a user interface component with increment and decrement buttons for the month, day, and year, and an underlying `GregorianCalendar`. If the interface reads January 31, 1999 and the user presses the month increment button, what should it read? If the underlying implementation uses `set()`, it might read March 3, 1999. A better result would be February 28, 1999. Furthermore, if the user presses the month increment button again, it should read March 31, 1999, not March 28, 1999. By saving the original date and using either `add()` or `roll()`, depending on whether larger fields should be affected, the user interface can behave as most users will intuitively expect.

**Note:** You should always use #roll and `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#add(kotlin.Int,%20kotlin.Int)` rather than attempting to perform arithmetic operations directly on the fields of a `Calendar`. It is quite possible for `Calendar` subclasses to have fields with non-linear behavior, for example missing months or days during non-leap years. The subclasses' `add` and `roll` methods will take this into account, while simple arithmetic manipulations may give invalid results.

Calendar Architecture in ICU4J

Recently the implementation of `Calendar` has changed significantly in order to better support subclassing. The original `Calendar` class was designed to support subclassing, but it had only one implemented subclass, `GregorianCalendar`. With the implementation of several new calendar subclasses, including the `BuddhistCalendar`, `ChineseCalendar`, `HebrewCalendar`, `IslamicCalendar`, and `JapaneseCalendar`, the subclassing API has been reworked thoroughly. This section details the new subclassing API and other ways in which `android.icu.util.Calendar` differs from `java.util.Calendar`.

Changes

Overview of changes between the classic `Calendar` architecture and the new architecture.

- The `fields[]` array is `private` now instead of `protected`. Subclasses must access it using the methods `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#internalSet(kotlin.Int,%20kotlin.Int)` and #internalGet. **Motivation:** Subclasses should not directly access data members.
- The `time` long word is `private` now instead of `protected`. Subclasses may access it using the method `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#internalGetTimeInMillis()`, which does not provoke an update. **Motivation:** Subclasses should not directly access data members.
- The scope of responsibility of subclasses has been drastically reduced. As much functionality as possible is implemented in the `Calendar` base class. As a result, it is much easier to subclass `Calendar`. **Motivation:** Subclasses should not have to reimplement common code. Certain behaviors are common across calendar systems: The definition and behavior of week-related fields and time fields, the arithmetic (`https://developer.android.com/reference/kotlin/android/icu/util/Calendar#add(kotlin.Int,%20kotlin.Int)` and `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#roll(kotlin.Int,%20kotlin.Int)`) behavior of many fields, and the field validation system.
- The subclassing API has been completely redesigned.
- The `Calendar` base class contains some Gregorian calendar algorithmic support that subclasses can use (specifically in `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#handleComputeFields(kotlin.Int)`). Subclasses can use the methods `getGregorianXxx()` to obtain precomputed values. **Motivation:** This is required by all `Calendar` subclasses in order to implement consistent time zone behavior, and Gregorian-derived systems can use the already computed data.
- The `FIELD_COUNT` constant has been removed. Use `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getFieldCount()`. In addition, framework API has been added to allow subclasses to define additional fields. **Motivation:**The number of fields is not constant across calendar systems.
- The range of handled dates has been narrowed from +/- \~300,000,000 years to +/- \~5,000,000 years. In practical terms this should not affect clients. However, it does mean that client code cannot be guaranteed well-behaved results with dates such as `Date(Long.MIN_VALUE)` or `Date(Long.MAX_VALUE)`. Instead, the `Calendar` protected constants should be used. **Motivation:** With the addition of the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#JULIAN_DAY:kotlin.Int` field, Julian day numbers must be restricted to a 32-bit `int`. This restricts the overall supported range. Furthermore, restricting the supported range simplifies the computations by removing special case code that was used to accommodate arithmetic overflow at millis near `Long.MIN_VALUE` and `Long.MAX_VALUE`.
- New fields are implemented: `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#JULIAN_DAY:kotlin.Int` defines single-field specification of the date. `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#MILLISECONDS_IN_DAY:kotlin.Int` defines a single-field specification of the wall time. `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#DOW_LOCAL:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#YEAR_WOY:kotlin.Int` implement localized day-of-week and week-of-year behavior.
- Subclasses can access protected millisecond constants defined in `Calendar`.
- New API has been added to support calendar-specific subclasses of `DateFormat`.
- Several subclasses have been implemented, representing various international calendar systems.

Subclass API

The original `Calendar` API was based on the experience of implementing a only a single subclass, `GregorianCalendar`. As a result, all of the subclassing kinks had not been worked out. The new subclassing API has been refined based on several implemented subclasses. This includes methods that must be overridden and methods for subclasses to call. Subclasses no longer have direct access to `fields` and `stamp`. Instead, they have new API to access these. Subclasses are able to allocate the `fields` array through a protected framework method; this allows subclasses to specify additional fields.

More functionality has been moved into the base class. The base class now contains much of the computational machinery to support the Gregorian calendar. This is based on two things: (1) Many calendars are based on the Gregorian calendar (such as the Buddhist and Japanese imperial calendars). (2) *All* calendars require basic Gregorian support in order to handle timezone computations.

Common computations have been moved into `Calendar`. Subclasses no longer compute the week related fields and the time related fields. These are commonly handled for all calendars by the base class.

**Subclass computation of time `=&gt;` fields**

The `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#ERA:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#YEAR:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#EXTENDED_YEAR:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#MONTH:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#DAY_OF_MONTH:kotlin.Int`, and `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#DAY_OF_YEAR:kotlin.Int` fields are computed by the subclass, based on the Julian day. All other fields are computed by `Calendar`.

- Subclasses should implement `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#handleComputeFields(kotlin.Int)` to compute the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#ERA:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#YEAR:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#EXTENDED_YEAR:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#MONTH:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#DAY_OF_MONTH:kotlin.Int`, and `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#DAY_OF_YEAR:kotlin.Int` fields, based on the value of the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#JULIAN_DAY:kotlin.Int` field. If there are calendar-specific fields not defined by `Calendar`, they must also be computed. These are the only fields that the subclass should compute. All other fields are computed by the base class, so time and week fields behave in a consistent way across all calendars. The default version of this method in `Calendar` implements a proleptic Gregorian calendar. Within this method, subclasses may call `getGregorianXxx()` to obtain the Gregorian calendar month, day of month, and extended year for the given date.

**Subclass computation of fields `=&gt;` time**

The interpretation of most field values is handled entirely by `Calendar`. `Calendar` determines which fields are set, which are not, which are set more recently, and so on. In addition, `Calendar` handles the computation of the time from the time fields and handles the week-related fields. The only thing the subclass must do is determine the extended year, based on the year fields, and then, given an extended year and a month, it must return a Julian day number.

- Subclasses should implement `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#handleGetExtendedYear()` to return the extended year for this calendar system, based on the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#YEAR:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#EXTENDED_YEAR:kotlin.Int`, and any fields that the calendar system uses that are larger than a year, such as `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#ERA:kotlin.Int`.
- Subclasses should implement `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#handleComputeMonthStart(kotlin.Int,%20kotlin.Int,%20kotlin.Boolean)` to return the Julian day number associated with a month and extended year. This is the Julian day number of the day before the first day of the month. The month number is zero-based. This computation should not depend on any field values.

**Other methods**

- Subclasses should implement `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#handleGetMonthLength(kotlin.Int,%20kotlin.Int)` to return the number of days in a given month of a given extended year. The month number, as always, is zero-based.
- Subclasses should implement `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#handleGetYearLength(kotlin.Int)` to return the number of days in the given extended year. This method is used by `computeWeekFields` to compute the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#WEEK_OF_YEAR:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#YEAR_WOY:kotlin.Int` fields.
- Subclasses should implement `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#handleGetLimit(kotlin.Int,%20kotlin.Int)` to return the protected values of a field, depending on the value of `limitType`. This method only needs to handle the fields `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#ERA:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#YEAR:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#MONTH:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#WEEK_OF_YEAR:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#WEEK_OF_MONTH:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#DAY_OF_MONTH:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#DAY_OF_YEAR:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#DAY_OF_WEEK_IN_MONTH:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#YEAR_WOY:kotlin.Int`, and `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#EXTENDED_YEAR:kotlin.Int`. Other fields are invariant (with respect to calendar system) and are handled by the base class.
- Optionally, subclasses may override #validateField to check any subclass-specific fields. If the field's value is out of range, the method should throw an `IllegalArgumentException`. The method may call `super.validateField(field)` to handle fields in a generic way, that is, to compare them to the range `getMinimum(field)`..`getMaximum(field)`.
- Optionally, subclasses may override `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#handleCreateFields()` to create an `int[]` array large enough to hold the calendar's fields. This is only necessary if the calendar defines additional fields beyond those defined by `Calendar`. The length of the result must be be between the base and maximum field counts.
- Optionally, subclasses may override #handleGetDateFormat to create a `DateFormat` appropriate to this calendar. This is only required if a calendar subclass redefines the use of a field (for example, changes the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#ERA:kotlin.Int` field from a symbolic field to a numeric one) or defines an additional field.
- Optionally, subclasses may override #roll and `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#add(kotlin.Int,%20kotlin.Int)` to handle fields that are discontinuous. For example, in the Hebrew calendar the month "Adar I" only occurs in leap years; in other years the calendar jumps from Shevat (month #4) to Adar (month #6). The `https://developer.android.com/reference/kotlin/android/icu/util/HebrewCalendar#add(kotlin.Int,%20kotlin.Int)` and android.icu.util.HebrewCalendar#roll methods take this into account, so that adding 1 month to Shevat gives the proper result (Adar) in a non-leap year. The protected utility method `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#pinField(kotlin.Int)` is often useful when implementing these two methods.

Normalized behavior

The behavior of certain fields has been made consistent across all calendar systems and implemented in `Calendar`.

- Time is normalized. Even though some calendar systems transition between days at sunset or at other times, all ICU4J calendars transition between days at *local zone midnight* . This allows ICU4J to centralize the time computations in `Calendar` and to maintain basic correspondences between calendar systems. Affected fields: `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#AM_PM:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#HOUR:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#HOUR_OF_DAY:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#MINUTE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#SECOND:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#MILLISECOND:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#ZONE_OFFSET:kotlin.Int`, and `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#DST_OFFSET:kotlin.Int`.
- DST behavior is normalized. Daylight savings time behavior is computed the same for all calendar systems, and depends on the value of several `GregorianCalendar` fields: the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#YEAR:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#MONTH:kotlin.Int`, and `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#DAY_OF_MONTH:kotlin.Int`. As a result, `Calendar` always computes these fields, even for non-Gregorian calendar systems. These fields are available to subclasses.
- Weeks are normalized. Although locales define the week differently, in terms of the day on which it starts, and the designation of week number one of a month or year, they all use a common mechanism. Furthermore, the day of the week has a simple and consistent definition throughout history. For example, although the Gregorian calendar introduced a discontinuity when first instituted, the day of week was not disrupted. For this reason, the fields `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#DAY_OF_WEEK:kotlin.Int`, `WEEK_OF_YEAR, WEEK_OF_MONTH`, `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#DAY_OF_WEEK_IN_MONTH:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#DOW_LOCAL:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#YEAR_WOY:kotlin.Int` are all computed in a consistent way in the base class, based on the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#EXTENDED_YEAR:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#DAY_OF_YEAR:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#MONTH:kotlin.Int`, and `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#DAY_OF_MONTH:kotlin.Int`, which are computed by the subclass.

Supported range

The allowable range of `Calendar` has been narrowed. `GregorianCalendar` used to attempt to support the range of dates with millisecond values from `Long.MIN_VALUE` to `Long.MAX_VALUE`. This introduced awkward constructions (hacks) which slowed down performance. It also introduced non-uniform behavior at the boundaries. The new `Calendar` protocol specifies the maximum range of supportable dates as those having Julian day numbers of `-0x7F000000` to `+0x7F000000`. This corresponds to years from \~5,800,000 BCE to \~5,800,000 CE. Programmers should use the protected constants in `Calendar` to specify an extremely early or extremely late date.

General notes

- Calendars implementations are *proleptic* . For example, even though the Gregorian calendar was not instituted until the 16th century, the `GregorianCalendar` class supports dates before the historical onset of the calendar by extending the calendar system backward in time. Similarly, the `HebrewCalendar` extends backward before the start of its epoch into zero and negative years. Subclasses do not throw exceptions because a date precedes the historical start of a calendar system. Instead, they implement `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#handleGetLimit(kotlin.Int,%20kotlin.Int)` to return appropriate limits on `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#YEAR:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#ERA:kotlin.Int`, etc. fields. Then, if the calendar is set to not be lenient, out-of-range field values will trigger an exception.
- Calendar system subclasses compute a *extended year* . This differs from the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#YEAR:kotlin.Int` field in that it ranges over all integer values, including zero and negative values, and it encapsulates the information of the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#YEAR:kotlin.Int` field and all larger fields. Thus, for the Gregorian calendar, the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#EXTENDED_YEAR:kotlin.Int` is computed as `ERA==AD ? YEAR : 1-YEAR`. Another example is the Mayan long count, which has years (`KUN`) and nested cycles of years (`KATUN` and `BAKTUN`). The Mayan `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#EXTENDED_YEAR:kotlin.Int` is computed as `TUN + 20 * (KATUN + 20 * BAKTUN)`. The `Calendar` base class uses the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#EXTENDED_YEAR:kotlin.Int` field to compute the week-related fields.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.WeekData` Simple, immutable struct-like class for access to the CLDR week data. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#AM:kotlin.Int` Value of the `AM_PM` field indicating the period of the day from midnight to just before noon. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#AM_PM:kotlin.Int` Field number for `get` and `set` indicating whether the `HOUR` is before or after noon. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#APRIL:kotlin.Int` Value of the `MONTH` field indicating the fourth month of the year. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#AUGUST:kotlin.Int` Value of the `MONTH` field indicating the eighth month of the year. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#DATE:kotlin.Int` Field number for `get` and `set` indicating the day of the month. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#DAY_OF_MONTH:kotlin.Int` Field number for `get` and `set` indicating the day of the month. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#DAY_OF_WEEK:kotlin.Int` Field number for `get` and `set` indicating the day of the week. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#DAY_OF_WEEK_IN_MONTH:kotlin.Int` Field number for `get` and `set` indicating the ordinal number of the day of the week within the current month. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#DAY_OF_YEAR:kotlin.Int` Field number for `get` and `set` indicating the day number within the current year. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#DECEMBER:kotlin.Int` Value of the `MONTH` field indicating the twelfth month of the year. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#DOW_LOCAL:kotlin.Int` **\[icu\]** Field number for `get()` and `set()` indicating the localized day of week. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#DST_OFFSET:kotlin.Int` Field number for `get` and `set` indicating the daylight savings offset in milliseconds. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#EPOCH_JULIAN_DAY:kotlin.Int` The Julian day of the epoch, that is, January 1, 1970 on the Gregorian calendar. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#ERA:kotlin.Int` Field number for `get` and `set` indicating the era, e. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#EXTENDED_YEAR:kotlin.Int` **\[icu\]** Field number for `get()` and `set()` indicating the extended year. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#FEBRUARY:kotlin.Int` Value of the `MONTH` field indicating the second month of the year. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#FRIDAY:kotlin.Int` Value of the `DAY_OF_WEEK` field indicating Friday. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#GREATEST_MINIMUM:kotlin.Int` Limit type for `getLimit()` and `handleGetLimit()` indicating the greatest minimum value that a field can take. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#HOUR:kotlin.Int` Field number for `get` and `set` indicating the hour of the morning or afternoon. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#HOUR_OF_DAY:kotlin.Int` Field number for `get` and `set` indicating the hour of the day. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#INTERNALLY_SET:kotlin.Int` Value of the time stamp `stamp[]` indicating that a field has been set via computations from the time or from other fields. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#IS_LEAP_MONTH:kotlin.Int` **\[icu\]** Field indicating whether or not the current month is a leap month. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#JANUARY:kotlin.Int` Value of the `MONTH` field indicating the first month of the year. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#JAN_1_1_JULIAN_DAY:kotlin.Int` The Julian day of the Gregorian epoch, that is, January 1, 1 on the Gregorian calendar. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#JULIAN_DAY:kotlin.Int` **\[icu\]** Field number for `get()` and `set()` indicating the modified Julian day number. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#JULY:kotlin.Int` Value of the `MONTH` field indicating the seventh month of the year. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#JUNE:kotlin.Int` Value of the `MONTH` field indicating the sixth month of the year. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#LEAST_MAXIMUM:kotlin.Int` Limit type for `getLimit()` and `handleGetLimit()` indicating the least maximum value that a field can take. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#MARCH:kotlin.Int` Value of the `MONTH` field indicating the third month of the year. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#MAXIMUM:kotlin.Int` Limit type for `getLimit()` and `handleGetLimit()` indicating the maximum value that a field can take (greatest maximum). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#MAX_FIELD_COUNT:kotlin.Int` The maximum number of fields possible. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#MAX_JULIAN:kotlin.Int` The maximum supported Julian day. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#MAX_MILLIS:kotlin.Long` The maximum supported epoch milliseconds. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#MAY:kotlin.Int` Value of the `MONTH` field indicating the fifth month of the year. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#MILLISECOND:kotlin.Int` Field number for `get` and `set` indicating the millisecond within the second. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#MILLISECONDS_IN_DAY:kotlin.Int` **\[icu\]** Field number for `get()` and `set()` indicating the milliseconds in the day. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#MINIMUM:kotlin.Int` Limit type for `getLimit()` and `handleGetLimit()` indicating the minimum value that a field can take (least minimum). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#MINIMUM_USER_STAMP:kotlin.Int` If the time stamp `stamp[]` has a value greater than or equal to `MINIMUM_USER_SET` then it has been set by the user via a call to `set()`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#MINUTE:kotlin.Int` Field number for `get` and `set` indicating the minute within the hour. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#MIN_JULIAN:kotlin.Int` The minimum supported Julian day. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#MIN_MILLIS:kotlin.Long` The minimum supported epoch milliseconds. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#MONDAY:kotlin.Int` Value of the `DAY_OF_WEEK` field indicating Monday. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#MONTH:kotlin.Int` Field number for `get` and `set` indicating the month. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#NOVEMBER:kotlin.Int` Value of the `MONTH` field indicating the eleventh month of the year. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#OCTOBER:kotlin.Int` Value of the `MONTH` field indicating the tenth month of the year. |
| --- | --- |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#ONE_DAY:kotlin.Long` The number of milliseconds in one day. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#ONE_HOUR:kotlin.Int` The number of milliseconds in one hour. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#ONE_MINUTE:kotlin.Int` The number of milliseconds in one minute. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#ONE_SECOND:kotlin.Int` The number of milliseconds in one second. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#ONE_WEEK:kotlin.Long` The number of milliseconds in one week. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#ORDINAL_MONTH:kotlin.Int` **\[icu\]** Field indicating the month. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#PM:kotlin.Int` Value of the `AM_PM` field indicating the period of the day from noon to just before midnight. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#RESOLVE_REMAP:kotlin.Int` Value to OR against resolve table field values for remapping. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#SATURDAY:kotlin.Int` Value of the `DAY_OF_WEEK` field indicating Saturday. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#SECOND:kotlin.Int` Field number for `get` and `set` indicating the second within the minute. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#SEPTEMBER:kotlin.Int` Value of the `MONTH` field indicating the ninth month of the year. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#SUNDAY:kotlin.Int` Value of the `DAY_OF_WEEK` field indicating Sunday. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#THURSDAY:kotlin.Int` Value of the `DAY_OF_WEEK` field indicating Thursday. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#TUESDAY:kotlin.Int` Value of the `DAY_OF_WEEK` field indicating Tuesday. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#UNDECIMBER:kotlin.Int` Value of the `MONTH` field indicating the thirteenth month of the year. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#UNSET:kotlin.Int` Value of the time stamp `stamp[]` indicating that a field has not been set since the last call to `clear()`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#WALLTIME_FIRST:kotlin.Int` **\[icu\]** Option used by `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#setRepeatedWallTimeOption(kotlin.Int)` and `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#setSkippedWallTimeOption(kotlin.Int)` specifying an ambiguous wall time to be interpreted as the earliest. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#WALLTIME_LAST:kotlin.Int` **\[icu\]** Option used by `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#setRepeatedWallTimeOption(kotlin.Int)` and `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#setSkippedWallTimeOption(kotlin.Int)` specifying an ambiguous wall time to be interpreted as the latest. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#WALLTIME_NEXT_VALID:kotlin.Int` **\[icu\]** Option used by `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#setSkippedWallTimeOption(kotlin.Int)` specifying an ambiguous wall time to be interpreted as the next valid wall time. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#WEDNESDAY:kotlin.Int` Value of the `DAY_OF_WEEK` field indicating Wednesday. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#WEEK_OF_MONTH:kotlin.Int` Field number for `get` and `set` indicating the week number within the current month. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#WEEK_OF_YEAR:kotlin.Int` Field number for `get` and `set` indicating the week number within the current year. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#YEAR:kotlin.Int` Field number for `get` and `set` indicating the year. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#YEAR_WOY:kotlin.Int` **\[icu\]** Field number for `get()` and `set()` indicating the extended year corresponding to the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#WEEK_OF_YEAR:kotlin.Int` field. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#ZONE_OFFSET:kotlin.Int` Field number for `get` and `set` indicating the raw offset from GMT in milliseconds. |

| Protected constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#Calendar()()` Constructs a Calendar with the default time zone and the default `FORMAT` locale. |
| `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#Calendar(android.icu.util.TimeZone,%20android.icu.util.ULocale)(zone: https://developer.android.com/reference/kotlin/android/icu/util/TimeZone!, locale: https://developer.android.com/reference/kotlin/android/icu/util/ULocale!)` Constructs a calendar with the specified time zone and locale. |
| `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#Calendar(android.icu.util.TimeZone,%20java.util.Locale)(zone: https://developer.android.com/reference/kotlin/android/icu/util/TimeZone!, aLocale: https://developer.android.com/reference/kotlin/java/util/Locale.html#!)` Constructs a calendar with the specified time zone and locale. |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#add(kotlin.Int,%20kotlin.Int)(field: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, amount: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Add a signed amount to a specified field, using this calendar's rules. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#after(kotlin.Any)(when: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!)` Compares the time field records. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#before(kotlin.Any)(when: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!)` Compares the time field records. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#clear()()` Clears the values of all the time fields. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#clear(kotlin.Int)(field: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Clears the value in the given time field. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#clone()()` Overrides Cloneable |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#compareTo(android.icu.util.Calendar)(other: https://developer.android.com/reference/kotlin/android/icu/util/Calendar#!)` Compares the times (in millis) represented by two `Calendar` objects. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Compares this calendar to the specified object. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#fieldDifference(java.util.Date,%20kotlin.Int)(when: https://developer.android.com/reference/kotlin/java/util/Date.html#!, field: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` **\[icu\]** Returns the difference between the given time and the time this calendar object is set to. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#get(kotlin.Int)(field: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the value for a given time field. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getActualMaximum(kotlin.Int)(field: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the maximum value that this field could have, given the current date. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getActualMinimum(kotlin.Int)(field: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the minimum value that this field could have, given the current date. |
| --- | --- |
| open static [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!\>! | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getAvailableLocales()()` Returns the list of locales for which Calendars are installed. |
| open [DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat.html#)! | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getDateTimeFormat(kotlin.Int,%20kotlin.Int,%20android.icu.util.ULocale)(dateStyle: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, timeStyle: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, loc: https://developer.android.com/reference/kotlin/android/icu/util/ULocale!)` **\[icu\]** Returns a `DateFormat` appropriate to this calendar. |
| open [DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat.html#)! | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getDateTimeFormat(kotlin.Int,%20kotlin.Int,%20java.util.Locale)(dateStyle: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, timeStyle: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, loc: https://developer.android.com/reference/kotlin/java/util/Locale.html#!)` **\[icu\]** Returns a `DateFormat` appropriate to this calendar. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getDisplayName(android.icu.util.ULocale)(loc: https://developer.android.com/reference/kotlin/android/icu/util/ULocale!)` Returns the name of this calendar in the language of the given locale. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getDisplayName(java.util.Locale)(loc: https://developer.android.com/reference/kotlin/java/util/Locale.html#!)` Returns the name of this calendar in the language of the given locale. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getFieldCount()()` **\[icu\]** Returns the number of fields defined by this calendar. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getFirstDayOfWeek()()` Returns what the first day of the week is, where 1 = `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#SUNDAY:kotlin.Int` and 7 = `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#SATURDAY:kotlin.Int`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getGreatestMinimum(kotlin.Int)(field: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the highest minimum value for the given field if varies. |
| open static [Calendar](https://developer.android.com/reference/kotlin/android/icu/util/Calendar#)! | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getInstance()()` Returns a calendar using the default time zone and locale. |
| --- | --- |
| open static [Calendar](https://developer.android.com/reference/kotlin/android/icu/util/Calendar#)! | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getInstance(android.icu.util.TimeZone)(zone: https://developer.android.com/reference/kotlin/android/icu/util/TimeZone!)` Returns a calendar using the specified time zone and default locale. |
| open static [Calendar](https://developer.android.com/reference/kotlin/android/icu/util/Calendar#)! | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getInstance(android.icu.util.TimeZone,%20android.icu.util.ULocale)(zone: https://developer.android.com/reference/kotlin/android/icu/util/TimeZone!, locale: https://developer.android.com/reference/kotlin/android/icu/util/ULocale!)` Returns a calendar with the specified time zone and locale. |
| open static [Calendar](https://developer.android.com/reference/kotlin/android/icu/util/Calendar#)! | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getInstance(android.icu.util.TimeZone,%20java.util.Locale)(zone: https://developer.android.com/reference/kotlin/android/icu/util/TimeZone!, aLocale: https://developer.android.com/reference/kotlin/java/util/Locale.html#!)` Returns a calendar with the specified time zone and locale. |
| --- | --- |
| open static [Calendar](https://developer.android.com/reference/kotlin/android/icu/util/Calendar#)! | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getInstance(android.icu.util.ULocale)(locale: https://developer.android.com/reference/kotlin/android/icu/util/ULocale!)` Returns a calendar using the default time zone and specified locale. |
| open static [Calendar](https://developer.android.com/reference/kotlin/android/icu/util/Calendar#)! | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getInstance(java.util.Locale)(aLocale: https://developer.android.com/reference/kotlin/java/util/Locale.html#!)` Returns a calendar using the default time zone and specified locale. |
| static [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getKeywordValuesForLocale(kotlin.String,%20android.icu.util.ULocale,%20kotlin.Boolean)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, locale: https://developer.android.com/reference/kotlin/android/icu/util/ULocale!, commonlyUsed: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` **\[icu\]** Given a key and a locale, returns an array of string values in a preferred order that would make a difference. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getLeastMaximum(kotlin.Int)(field: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the lowest maximum value for the given field if varies. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getMaximum(kotlin.Int)(field: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the maximum value for the given time field. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getMinimalDaysInFirstWeek()()` Returns what the minimal days required in the first week of the year are. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getMinimum(kotlin.Int)(field: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the minimum value for the given time field. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getRepeatedWallTimeOption()()` **\[icu\]**Gets the behavior for handling wall time repeating multiple times at negative time zone offset transitions. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getSkippedWallTimeOption()()` **\[icu\]**Gets the behavior for handling skipped wall time at positive time zone offset transitions. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getTemporalMonthCode()()` Gets The Temporal monthCode value corresponding to the month for the date. |
| [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)! | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getTime()()` Returns this Calendar's current time. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getTimeInMillis()()` Returns this Calendar's current time as a long. |
| --- | --- |
| open [TimeZone](https://developer.android.com/reference/kotlin/android/icu/util/TimeZone)! | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getTimeZone()()` Returns the time zone. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getType()()` **\[icu\]** Returns the calendar type name string for this Calendar object. |
| open [Calendar.WeekData](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.WeekData)! | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getWeekData()()` **\[icu\]** Return simple, immutable struct-like class for access to the week data in this calendar. |
| --- | --- |
| open static [Calendar.WeekData](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.WeekData)! | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getWeekDataForRegion(kotlin.String)(region: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` **\[icu\]** Return simple, immutable struct-like class for access to the CLDR week data. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#hashCode()()` Returns a hash code for this calendar. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#inTemporalLeapYear()()` **\[icu\]** Returns true if the date is in a leap year. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#isEquivalentTo(android.icu.util.Calendar)(other: https://developer.android.com/reference/kotlin/android/icu/util/Calendar#!)` **\[icu\]** Returns true if the given Calendar object is equivalent to this one. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#isLenient()()` Tell whether date/time interpretation is to be lenient. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#isSet(kotlin.Int)(field: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Determines if the given time field has a value set. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#isWeekend()()` **\[icu\]** Returns true if this Calendar's current date and time is in the weekend in this calendar system. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#isWeekend(java.util.Date)(date: https://developer.android.com/reference/kotlin/java/util/Date.html#!)` **\[icu\]** Returns true if the given date and time is in the weekend in this calendar system. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#roll(kotlin.Int,%20kotlin.Boolean)(field: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, up: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Rolls (up/down) a single unit of time on the given field. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#roll(kotlin.Int,%20kotlin.Int)(field: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, amount: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Rolls (up/down) a specified amount time on the given field. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#set(kotlin.Int,%20kotlin.Int)(field: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the time field with the given value. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#set(kotlin.Int,%20kotlin.Int,%20kotlin.Int)(year: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, month: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, date: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the values for the fields year, month, and date. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#set(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(year: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, month: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, date: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, hour: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, minute: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the values for the fields year, month, date, hour, and minute. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#set(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(year: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, month: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, date: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, hour: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, minute: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, second: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the values for the fields year, month, date, hour, minute, and second. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#setFirstDayOfWeek(kotlin.Int)(value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets what the first day of the week is, where 1 = `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#SUNDAY:kotlin.Int` and 7 = `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#SATURDAY:kotlin.Int`. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#setLenient(kotlin.Boolean)(lenient: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Specify whether or not date/time interpretation is to be lenient. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#setMinimalDaysInFirstWeek(kotlin.Int)(value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets what the minimal days required in the first week of the year are. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#setRepeatedWallTimeOption(kotlin.Int)(option: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` **\[icu\]**Sets the behavior for handling wall time repeating multiple times at negative time zone offset transitions. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#setSkippedWallTimeOption(kotlin.Int)(option: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` **\[icu\]**Sets the behavior for handling skipped wall time at positive time zone offset transitions. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#setTemporalMonthCode(kotlin.String)(temporalMonth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Sets The Temporal monthCode which is a string identifier that starts with the literal grapheme "M" followed by two graphemes representing the zero-padded month number of the current month in a normal (non-leap) year and suffixed by an optional literal grapheme "L" if this is a leap month in a lunisolar calendar. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#setTime(java.util.Date)(date: https://developer.android.com/reference/kotlin/java/util/Date.html#!)` Sets this Calendar's current time with the given Date. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#setTimeInMillis(kotlin.Long)(millis: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Sets this Calendar's current time from the given long value. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#setTimeZone(android.icu.util.TimeZone)(value: https://developer.android.com/reference/kotlin/android/icu/util/TimeZone!)` Sets the time zone with the given time zone value. |
| open [Calendar](https://developer.android.com/reference/kotlin/android/icu/util/Calendar#)! | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#setWeekData(android.icu.util.Calendar.WeekData)(wdata: https://developer.android.com/reference/kotlin/android/icu/util/Calendar.WeekData!)` **\[icu\]** Set data in this calendar based on the WeekData input. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#toString()()` Returns a string representation of this calendar. |

| Protected methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#complete()()` Fills in any unset fields in the time field list. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#computeFields()()` Converts the current millisecond time value `time` to field values in `fields[]`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#computeGregorianFields(kotlin.Int)(julianDay: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Compute the Gregorian calendar year, month, and day of month from the Julian day. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#computeGregorianMonthStart(kotlin.Int,%20kotlin.Int)(year: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, month: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Compute the Julian day of a month of the Gregorian calendar. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#computeJulianDay()()` Compute the Julian day number as specified by this calendar's fields. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#computeMillisInDay()()` Compute the milliseconds in the day from the fields. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#computeTime()()` Converts the current field values in `fields[]` to the millisecond time value `time`. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#computeZoneOffset(kotlin.Long,%20kotlin.Int)(millis: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, millisInDay: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` This method can assume EXTENDED_YEAR has been set. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#fieldName(kotlin.Int)(field: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns a string name for a field, for debugging and exceptions. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#floorDivide(kotlin.Int,%20kotlin.Int)(numerator: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, denominator: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Divide two integers, returning the floor of the quotient. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#floorDivide(kotlin.Int,%20kotlin.Int,%20kotlin.IntArray)(numerator: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, denominator: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, remainder: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!)` Divide two integers, returning the floor of the quotient, and the modulus remainder. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#floorDivide(kotlin.Long,%20kotlin.Int,%20kotlin.IntArray)(numerator: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, denominator: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, remainder: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!)` Divide two integers, returning the floor of the quotient, and the modulus remainder. |
| --- | --- |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#floorDivide(kotlin.Long,%20kotlin.Long)(numerator: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, denominator: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Divide two long integers, returning the floor of the quotient. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!\>!\>! | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getFieldResolutionTable()()` Returns the field resolution array for this calendar. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getGregorianDayOfMonth()()` Returns the day of month (1-based) on the Gregorian calendar as computed by `computeGregorianFields()`. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getGregorianDayOfYear()()` Returns the day of year (1-based) on the Gregorian calendar as computed by `computeGregorianFields()`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getGregorianMonth()()` Returns the month (0-based) on the Gregorian calendar as computed by `computeGregorianFields()`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getGregorianYear()()` Returns the extended year on the Gregorian calendar as computed by `computeGregorianFields()`. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getLimit(kotlin.Int,%20kotlin.Int)(field: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, limitType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns a limit for a field. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getStamp(kotlin.Int)(field: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the timestamp of a field. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#gregorianMonthLength(kotlin.Int,%20kotlin.Int)(y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, m: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the length of a month of the Gregorian calendar. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#gregorianPreviousMonthLength(kotlin.Int,%20kotlin.Int)(y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, m: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the length of a previous month of the Gregorian calendar. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#handleComputeFields(kotlin.Int)(julianDay: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Subclasses may override this method to compute several fields specific to each calendar system. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#handleComputeJulianDay(kotlin.Int)(bestField: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Subclasses may override this. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#handleComputeMonthStart(kotlin.Int,%20kotlin.Int,%20kotlin.Boolean)(eyear: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, month: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, useMonth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Returns the Julian day number of day before the first day of the given month in the given extended year. |
| open [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#handleCreateFields()()` Subclasses that use additional fields beyond those defined in `Calendar` should override this method to return an `int[]` array of the appropriate length. |
| open [DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat.html#)! | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#handleGetDateFormat(kotlin.String,%20android.icu.util.ULocale)(pattern: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, locale: https://developer.android.com/reference/kotlin/android/icu/util/ULocale!)` Creates a `DateFormat` appropriate to this calendar. |
| --- | --- |
| open [DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat.html#)! | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#handleGetDateFormat(kotlin.String,%20kotlin.String,%20java.util.Locale)(pattern: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, override: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, locale: https://developer.android.com/reference/kotlin/java/util/Locale.html#!)` Creates a `DateFormat` appropriate to this calendar. |
| open [DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat.html#)! | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#handleGetDateFormat(kotlin.String,%20java.util.Locale)(pattern: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, locale: https://developer.android.com/reference/kotlin/java/util/Locale.html#!)` Creates a `DateFormat` appropriate to this calendar. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#handleGetExtendedYear()()` Returns the extended year defined by the current fields. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#handleGetLimit(kotlin.Int,%20kotlin.Int)(field: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, limitType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Subclass API for defining limits of different types. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#handleGetMonthLength(kotlin.Int,%20kotlin.Int)(extendedYear: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, month: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the number of days in the given month of the given extended year of this calendar system. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#handleGetYearLength(kotlin.Int)(eyear: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the number of days in the given extended year of this calendar system. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#internalGet(kotlin.Int)(field: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the value for a given time field. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#internalGet(kotlin.Int,%20kotlin.Int)(field: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, defaultValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the value for a given time field, or return the given default value if the field is not set. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#internalGetTimeInMillis()()` Returns the current milliseconds without recomputing. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#internalSet(kotlin.Int,%20kotlin.Int)(field: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set a field to a value. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#isGregorianLeapYear(kotlin.Int)(year: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Determines if the given year is a leap year. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#julianDayToDayOfWeek(kotlin.Int)(julian: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the day of week, from SUNDAY to SATURDAY, given a Julian day. |
| --- | --- |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#julianDayToMillis(kotlin.Int)(julian: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Converts Julian day to time as milliseconds. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#millisToJulianDay(kotlin.Long)(millis: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Converts time as milliseconds to Julian day. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#newerField(kotlin.Int,%20kotlin.Int)(defaultField: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, alternateField: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the field that is newer, either defaultField, or alternateField. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#newestStamp(kotlin.Int,%20kotlin.Int,%20kotlin.Int)(first: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, last: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, bestStampSoFar: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the newest stamp of a given range of fields. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#pinField(kotlin.Int)(field: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Adjust the specified field so that it is within the allowable range for the date to which this calendar is set. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#prepareGetActual(kotlin.Int,%20kotlin.Boolean)(field: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, isMinimum: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Prepare this calendar for computing the actual minimum or maximum. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#resolveFields(kotlin.Array)(precedenceTable: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!>!>!)` Given a precedence table, return the newest field combination in the table, or -1 if none is found. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#validateField(kotlin.Int)(field: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Validate a single field of this calendar. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#validateField(kotlin.Int,%20kotlin.Int,%20kotlin.Int)(field: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, min: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, max: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Validate a single field of this calendar given its minimum and maximum allowed value. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#validateFields()()` Ensure that each field is within its valid range by calling `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#validateField(kotlin.Int)` on each field that has been set. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#weekNumber(kotlin.Int,%20kotlin.Int)(dayOfPeriod: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, dayOfWeek: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the week number of a day, within a period. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#weekNumber(kotlin.Int,%20kotlin.Int,%20kotlin.Int)(desiredDay: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, dayOfPeriod: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, dayOfWeek: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the week number of a day, within a period. |
| --- | --- |

| Properties ||
|---|---|
| static [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)! | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#MAX_DATE:java.util.Date` The maximum supported `Date`. |
| static [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)! | `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#MIN_DATE:java.util.Date` The minimum supported `Date`. |

## Constants

### AM

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AM: Int
```

Value of the `AM_PM` field indicating the period of the day from midnight to just before noon.

 Value: 0

### AM_PM

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AM_PM: Int
```

Field number for `get` and `set` indicating whether the `HOUR` is before or after noon. E.g., at 10:04:15.250 PM the `AM_PM` is `PM`.

 Value: 9

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#AM:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#PM:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#HOUR:kotlin.Int`

### APRIL

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val APRIL: Int
```

Value of the `MONTH` field indicating the fourth month of the year.

 Value: 3

### AUGUST

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AUGUST: Int
```

Value of the `MONTH` field indicating the eighth month of the year.

 Value: 7

### DATE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATE: Int
```

Field number for `get` and `set` indicating the day of the month. This is a synonym for `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#DAY_OF_MONTH:kotlin.Int`. The first day of the month has value 1.

 Value: 5

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#DAY_OF_MONTH:kotlin.Int`

### DAY_OF_MONTH

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DAY_OF_MONTH: Int
```

Field number for `get` and `set` indicating the day of the month. This is a synonym for `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#DATE:kotlin.Int`. The first day of the month has value 1.

 Value: 5

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#DATE:kotlin.Int`

### DAY_OF_WEEK

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DAY_OF_WEEK: Int
```

Field number for `get` and `set` indicating the day of the week. This field takes values `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#SUNDAY:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#MONDAY:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#TUESDAY:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#WEDNESDAY:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#THURSDAY:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#FRIDAY:kotlin.Int`, and `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#SATURDAY:kotlin.Int`.

 Value: 7

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#SUNDAY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#MONDAY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#TUESDAY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#WEDNESDAY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#THURSDAY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#FRIDAY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#SATURDAY:kotlin.Int`

### DAY_OF_WEEK_IN_MONTH

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DAY_OF_WEEK_IN_MONTH: Int
```

Field number for `get` and `set` indicating the ordinal number of the day of the week within the current month. Together with the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#DAY_OF_WEEK:kotlin.Int` field, this uniquely specifies a day within a month. Unlike `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#WEEK_OF_MONTH:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#WEEK_OF_YEAR:kotlin.Int`, this field's value does *not* depend on `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getFirstDayOfWeek()` or `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getMinimalDaysInFirstWeek()`. `DAY_OF_MONTH 1` through `7` always correspond to `DAY_OF_WEEK_IN_MONTH 1`; `8` through `15` correspond to `DAY_OF_WEEK_IN_MONTH 2`, and so on. `DAY_OF_WEEK_IN_MONTH 0` indicates the week before `DAY_OF_WEEK_IN_MONTH 1`. Negative values count back from the end of the month, so the last Sunday of a month is specified as `DAY_OF_WEEK = SUNDAY, DAY_OF_WEEK_IN_MONTH = -1`. Because negative values count backward they will usually be aligned differently within the month than positive values. For example, if a month has 31 days, `DAY_OF_WEEK_IN_MONTH -1` will overlap `DAY_OF_WEEK_IN_MONTH 5` and the end of `4`.

 Value: 8

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#DAY_OF_WEEK:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#WEEK_OF_MONTH:kotlin.Int`

### DAY_OF_YEAR

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DAY_OF_YEAR: Int
```

Field number for `get` and `set` indicating the day number within the current year. The first day of the year has value 1.

 Value: 6

### DECEMBER

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DECEMBER: Int
```

Value of the `MONTH` field indicating the twelfth month of the year.

 Value: 11

### DOW_LOCAL

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DOW_LOCAL: Int
```

**\[icu\]** Field number for `get()` and `set()` indicating the localized day of week. This will be a value from 1 to 7 inclusive, with 1 being the localized first day of the week.

 Value: 18

### DST_OFFSET

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DST_OFFSET: Int
```

Field number for `get` and `set` indicating the daylight savings offset in milliseconds.

 Value: 16

### EPOCH_JULIAN_DAY

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected static val EPOCH_JULIAN_DAY: Int
```

The Julian day of the epoch, that is, January 1, 1970 on the Gregorian calendar.

 Value: 2440588

### ERA

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERA: Int
```

Field number for `get` and `set` indicating the era, e.g., AD or BC in the Julian calendar. This is a calendar-specific value; see subclass documentation.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/GregorianCalendar#AD:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/icu/util/GregorianCalendar#BC:kotlin.Int`

### EXTENDED_YEAR

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTENDED_YEAR: Int
```

**\[icu\]** Field number for `get()` and `set()` indicating the extended year. This is a single number designating the year of this calendar system, encompassing all supra-year fields. For example, for the Julian calendar system, year numbers are positive, with an era of BCE or CE. An extended year value for the Julian calendar system assigns positive values to CE years and negative values to BCE years, with 1 BCE being year 0.

 Value: 19

### FEBRUARY

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEBRUARY: Int
```

Value of the `MONTH` field indicating the second month of the year.

 Value: 1

### FRIDAY

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FRIDAY: Int
```

Value of the `DAY_OF_WEEK` field indicating Friday.

 Value: 6

### GREATEST_MINIMUM

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected static val GREATEST_MINIMUM: Int
```

Limit type for `getLimit()` and `handleGetLimit()` indicating the greatest minimum value that a field can take.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getLimit(kotlin.Int,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#handleGetLimit(kotlin.Int,%20kotlin.Int)`

### HOUR

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HOUR: Int
```

Field number for `get` and `set` indicating the hour of the morning or afternoon. `HOUR` is used for the 12-hour clock. E.g., at 10:04:15.250 PM the `HOUR` is 10.

 Value: 10

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#AM_PM:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#HOUR_OF_DAY:kotlin.Int`

### HOUR_OF_DAY

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HOUR_OF_DAY: Int
```

Field number for `get` and `set` indicating the hour of the day. `HOUR_OF_DAY` is used for the 24-hour clock. E.g., at 10:04:15.250 PM the `HOUR_OF_DAY` is 22.

 Value: 11

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#HOUR:kotlin.Int`

### INTERNALLY_SET

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected static val INTERNALLY_SET: Int
```

Value of the time stamp `stamp[]` indicating that a field has been set via computations from the time or from other fields.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#UNSET:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#MINIMUM_USER_STAMP:kotlin.Int`

### IS_LEAP_MONTH

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val IS_LEAP_MONTH: Int
```

**\[icu\]** Field indicating whether or not the current month is a leap month. Should have a value of 0 for non-leap months, and 1 for leap months.

 Value: 22

### JANUARY

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val JANUARY: Int
```

Value of the `MONTH` field indicating the first month of the year.

 Value: 0

### JAN_1_1_JULIAN_DAY

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected static val JAN_1_1_JULIAN_DAY: Int
```

The Julian day of the Gregorian epoch, that is, January 1, 1 on the Gregorian calendar.

 Value: 1721426

### JULIAN_DAY

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val JULIAN_DAY: Int
```

**\[icu\]** Field number for `get()` and `set()` indicating the modified Julian day number. This is different from the conventional Julian day number in two regards. First, it demarcates days at local zone midnight, rather than noon GMT. Second, it is a local number; that is, it depends on the local time zone. It can be thought of as a single number that encompasses all the date-related fields.

 Value: 20

### JULY

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val JULY: Int
```

Value of the `MONTH` field indicating the seventh month of the year.

 Value: 6

### JUNE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val JUNE: Int
```

Value of the `MONTH` field indicating the sixth month of the year.

 Value: 5

### LEAST_MAXIMUM

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected static val LEAST_MAXIMUM: Int
```

Limit type for `getLimit()` and `handleGetLimit()` indicating the least maximum value that a field can take.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getLimit(kotlin.Int,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#handleGetLimit(kotlin.Int,%20kotlin.Int)`

### MARCH

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MARCH: Int
```

Value of the `MONTH` field indicating the third month of the year.

 Value: 2

### MAXIMUM

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected static val MAXIMUM: Int
```

Limit type for `getLimit()` and `handleGetLimit()` indicating the maximum value that a field can take (greatest maximum).

 Value: 3

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getLimit(kotlin.Int,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#handleGetLimit(kotlin.Int,%20kotlin.Int)`

### MAX_FIELD_COUNT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected static val MAX_FIELD_COUNT: Int
```

**Deprecated:** *ICU 58 The numeric value may change over time, see ICU ticket #12420.*

The maximum number of fields possible. Subclasses must not define more total fields than this number.

 Value: 32

### MAX_JULIAN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected static val MAX_JULIAN: Int
```

The maximum supported Julian day. This value is equivalent to `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#MAX_MILLIS:kotlin.Long` and `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#MAX_DATE:java.util.Date`.

 Value: 2130706432

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#JULIAN_DAY:kotlin.Int`

### MAX_MILLIS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected static val MAX_MILLIS: Long
```

The maximum supported epoch milliseconds. This value is equivalent to `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#MAX_JULIAN:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#MAX_DATE:java.util.Date`.

 Value: 183882168921600000L

### MAY

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MAY: Int
```

Value of the `MONTH` field indicating the fifth month of the year.

 Value: 4

### MILLISECOND

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MILLISECOND: Int
```

Field number for `get` and `set` indicating the millisecond within the second. E.g., at 10:04:15.250 PM the `MILLISECOND` is 250.

 Value: 14

### MILLISECONDS_IN_DAY

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MILLISECONDS_IN_DAY: Int
```

**\[icu\]** Field number for `get()` and `set()` indicating the milliseconds in the day. This ranges from 0 to 23:59:59.999 (regardless of DST). This field behaves *exactly* like a composite of all time-related fields, not including the zone fields. As such, it also reflects discontinuities of those fields on DST transition days. On a day of DST onset, it will jump forward. On a day of DST cessation, it will jump backward. This reflects the fact that is must be combined with the DST_OFFSET field to obtain a unique local time value.

 Value: 21

### MINIMUM

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected static val MINIMUM: Int
```

Limit type for `getLimit()` and `handleGetLimit()` indicating the minimum value that a field can take (least minimum).

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getLimit(kotlin.Int,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#handleGetLimit(kotlin.Int,%20kotlin.Int)`

### MINIMUM_USER_STAMP

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected static val MINIMUM_USER_STAMP: Int
```

If the time stamp `stamp[]` has a value greater than or equal to `MINIMUM_USER_SET` then it has been set by the user via a call to `set()`.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#UNSET:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#INTERNALLY_SET:kotlin.Int`

### MINUTE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MINUTE: Int
```

Field number for `get` and `set` indicating the minute within the hour. E.g., at 10:04:15.250 PM the `MINUTE` is 4.

 Value: 12

### MIN_JULIAN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected static val MIN_JULIAN: Int
```

The minimum supported Julian day. This value is equivalent to `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#MIN_MILLIS:kotlin.Long` and `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#MIN_DATE:java.util.Date`.

 Value: -2130706432

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#JULIAN_DAY:kotlin.Int`

### MIN_MILLIS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected static val MIN_MILLIS: Long
```

The minimum supported epoch milliseconds. This value is equivalent to `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#MIN_JULIAN:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#MIN_DATE:java.util.Date`.

 Value: -184303902528000000L

### MONDAY

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MONDAY: Int
```

Value of the `DAY_OF_WEEK` field indicating Monday.

 Value: 2

### MONTH

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MONTH: Int
```

Field number for `get` and `set` indicating the month. This is a calendar-specific value. The first month of the year is `JANUARY`; the last depends on the number of months in a year.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#JANUARY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#FEBRUARY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#MARCH:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#APRIL:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#MAY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#JUNE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#JULY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#AUGUST:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#SEPTEMBER:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#OCTOBER:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#NOVEMBER:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#DECEMBER:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#UNDECIMBER:kotlin.Int`

### NOVEMBER

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NOVEMBER: Int
```

Value of the `MONTH` field indicating the eleventh month of the year.

 Value: 10

### OCTOBER

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OCTOBER: Int
```

Value of the `MONTH` field indicating the tenth month of the year.

 Value: 9

### ONE_DAY

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected static val ONE_DAY: Long
```

The number of milliseconds in one day. Although ONE_DAY and ONE_WEEK can fit into ints, they must be longs in order to prevent arithmetic overflow when performing (bug 4173516).

 Value: 86400000L

### ONE_HOUR

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected static val ONE_HOUR: Int
```

The number of milliseconds in one hour.

 Value: 3600000

### ONE_MINUTE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected static val ONE_MINUTE: Int
```

The number of milliseconds in one minute.

 Value: 60000

### ONE_SECOND

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected static val ONE_SECOND: Int
```

The number of milliseconds in one second.

 Value: 1000

### ONE_WEEK

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected static val ONE_WEEK: Long
```

The number of milliseconds in one week. Although ONE_DAY and ONE_WEEK can fit into ints, they must be longs in order to prevent arithmetic overflow when performing (bug 4173516).

 Value: 604800000L

### ORDINAL_MONTH

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ORDINAL_MONTH: Int
```

**\[icu\]** Field indicating the month. This is a calendar-specific value. Differ from MONTH, this value is continuous and unique within a year and range from 0 to 11 or 0 to 12 depending on how many months in a year, the calendar system has leap month or not, and in leap year or not. It is the ordinal position of that month in the corresponding year of the calendar. For Chinese, Dangi, and Hebrew calendar, the range is 0 to 11 in non-leap years and 0 to 12 in leap years. For Coptic and Ethiopian calendar, the range is always 0 to 12. For other calendars supported by ICU now, the range is 0 to 11. When the number of months in a year of the identified calendar is variable, a different ORDINAL_MONTH value can be used for dates that are part of the same named month in different years. For example, in the Hebrew calendar, "1 Nisan 5781" is associated with ORDINAL_MONTH value 6 while "1 Nisan 5782" is associated with ORDINAL_MONTH value 7 because 5782 is a leap year and Nisan follows the insertion of Adar I. In Chinese calendar, "Year 4664 Month 6 Day 2" is associated with ORDINAL_MONTH value 5 while "Year 4665 Month 6 Day 2" is associated with ORDINAL_MONTH value 6 because 4665 is a leap year and there is an extra "Leap Month 5" which associated with ORDINAL_MONTH value 5 before "Month 6" of year 4664.

 Value: 23

### PM

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PM: Int
```

Value of the `AM_PM` field indicating the period of the day from noon to just before midnight.

 Value: 1

### RESOLVE_REMAP

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected static val RESOLVE_REMAP: Int
```

Value to OR against resolve table field values for remapping.

 Value: 32

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#resolveFields(kotlin.Array)`

### SATURDAY

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SATURDAY: Int
```

Value of the `DAY_OF_WEEK` field indicating Saturday.

 Value: 7

### SECOND

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SECOND: Int
```

Field number for `get` and `set` indicating the second within the minute. E.g., at 10:04:15.250 PM the `SECOND` is 15.

 Value: 13

### SEPTEMBER

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SEPTEMBER: Int
```

Value of the `MONTH` field indicating the ninth month of the year.

 Value: 8

### SUNDAY

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SUNDAY: Int
```

Value of the `DAY_OF_WEEK` field indicating Sunday.

 Value: 1

### THURSDAY

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val THURSDAY: Int
```

Value of the `DAY_OF_WEEK` field indicating Thursday.

 Value: 5

### TUESDAY

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TUESDAY: Int
```

Value of the `DAY_OF_WEEK` field indicating Tuesday.

 Value: 3

### UNDECIMBER

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UNDECIMBER: Int
```

Value of the `MONTH` field indicating the thirteenth month of the year. Although `https://developer.android.com/reference/kotlin/android/icu/util/GregorianCalendar` does not use this value, lunar calendars do.

 Value: 12

### UNSET

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected static val UNSET: Int
```

Value of the time stamp `stamp[]` indicating that a field has not been set since the last call to `clear()`.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#INTERNALLY_SET:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#MINIMUM_USER_STAMP:kotlin.Int`

### WALLTIME_FIRST

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WALLTIME_FIRST: Int
```

**\[icu\]** Option used by `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#setRepeatedWallTimeOption(kotlin.Int)` and `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#setSkippedWallTimeOption(kotlin.Int)` specifying an ambiguous wall time to be interpreted as the earliest.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#setRepeatedWallTimeOption(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getRepeatedWallTimeOption()`
- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#setSkippedWallTimeOption(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getSkippedWallTimeOption()`

### WALLTIME_LAST

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WALLTIME_LAST: Int
```

**\[icu\]** Option used by `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#setRepeatedWallTimeOption(kotlin.Int)` and `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#setSkippedWallTimeOption(kotlin.Int)` specifying an ambiguous wall time to be interpreted as the latest.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#setRepeatedWallTimeOption(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getRepeatedWallTimeOption()`
- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#setSkippedWallTimeOption(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getSkippedWallTimeOption()`

### WALLTIME_NEXT_VALID

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WALLTIME_NEXT_VALID: Int
```

**\[icu\]** Option used by `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#setSkippedWallTimeOption(kotlin.Int)` specifying an ambiguous wall time to be interpreted as the next valid wall time.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#setSkippedWallTimeOption(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getSkippedWallTimeOption()`

### WEDNESDAY

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WEDNESDAY: Int
```

Value of the `DAY_OF_WEEK` field indicating Wednesday.

 Value: 4

### WEEK_OF_MONTH

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WEEK_OF_MONTH: Int
```

Field number for `get` and `set` indicating the week number within the current month. The first week of the month, as defined by `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getFirstDayOfWeek()` and `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getMinimalDaysInFirstWeek()`, has value 1. Subclasses define the value of `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#WEEK_OF_MONTH:kotlin.Int` for days before the first week of the month.

 Value: 4

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getFirstDayOfWeek()`
- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getMinimalDaysInFirstWeek()`

### WEEK_OF_YEAR

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WEEK_OF_YEAR: Int
```

Field number for `get` and `set` indicating the week number within the current year. The first week of the year, as defined by `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getFirstDayOfWeek()` and `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getMinimalDaysInFirstWeek()`, has value 1. Subclasses define the value of `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#WEEK_OF_YEAR:kotlin.Int` for days before the first week of the year.

 Value: 3

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getFirstDayOfWeek()`
- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getMinimalDaysInFirstWeek()`

### YEAR

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val YEAR: Int
```

Field number for `get` and `set` indicating the year. This is a calendar-specific value; see subclass documentation.

 Value: 1

### YEAR_WOY

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val YEAR_WOY: Int
```

**\[icu\]** Field number for `get()` and `set()` indicating the extended year corresponding to the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#WEEK_OF_YEAR:kotlin.Int` field. This may be one greater or less than the value of `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#EXTENDED_YEAR:kotlin.Int`.

 Value: 17

### ZONE_OFFSET

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ZONE_OFFSET: Int
```

Field number for `get` and `set` indicating the raw offset from GMT in milliseconds.

 Value: 15

## Protected constructors

### Calendar

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected Calendar()
```

Constructs a Calendar with the default time zone and the default `FORMAT` locale.
**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/TimeZone#getDefault()`
- `https://developer.android.com/reference/kotlin/android/icu/util/ULocale.Category`

### Calendar

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected Calendar(
    zone: TimeZone!, 
    locale: ULocale!)
```

Constructs a calendar with the specified time zone and locale.

| Parameters ||
|---|---|
| `zone` | [TimeZone](https://developer.android.com/reference/kotlin/android/icu/util/TimeZone)!: the time zone to use |
| `locale` | [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale)!: the ulocale for the week data |

### Calendar

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected Calendar(
    zone: TimeZone!, 
    aLocale: Locale!)
```

Constructs a calendar with the specified time zone and locale.

| Parameters ||
|---|---|
| `zone` | [TimeZone](https://developer.android.com/reference/kotlin/android/icu/util/TimeZone)!: the time zone to use |
| `aLocale` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!: the locale for the week data |

## Public methods

### add

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun add(
    field: Int, 
    amount: Int
): Unit
```

Add a signed amount to a specified field, using this calendar's rules. For example, to add three days to the current date, you can call `add(Calendar.DATE, 3)`.

When adding to certain fields, the values of other fields may conflict and need to be changed. For example, when adding one to the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#MONTH:kotlin.Int` field for the Gregorian date 1/31/96, the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#DAY_OF_MONTH:kotlin.Int` field must be adjusted so that the result is 2/29/96 rather than the invalid 2/31/96.

Adding a positive value always means moving forward in time, so for the Gregorian calendar, starting with 100 BC and adding +1 to year results in 99 BC (even though this actually reduces the numeric value of the field itself).

**\[icu\] Note:** The ICU implementation of this method is able to add to all fields except for `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#ERA:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#DST_OFFSET:kotlin.Int`, and `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#ZONE_OFFSET:kotlin.Int`. Subclasses may, of course, add support for additional fields in their overrides of `add`.

**Note:** You should always use `roll` and `add` rather than attempting to perform arithmetic operations directly on the fields of a `Calendar`. It is quite possible for `Calendar` subclasses to have fields with non-linear behavior, for example missing months or days during non-leap years. The subclasses' `add` and `roll` methods will take this into account, while simple arithmetic manipulations may give invalid results.

**Subclassing:** 
This implementation of `add` assumes that the behavior of the field is continuous between its minimum and maximum, which are found by calling `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getActualMinimum(kotlin.Int)` and `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getActualMaximum(kotlin.Int)`. For such fields, simple arithmetic operations are sufficient to perform the add.

Subclasses that have fields for which this assumption of continuity breaks down must override `add` to handle those fields specially. For example, in the Hebrew calendar the month "Adar I" only occurs in leap years; in other years the calendar jumps from Shevat (month #4) to Adar (month #6). The `https://developer.android.com/reference/kotlin/android/icu/util/HebrewCalendar#add(kotlin.Int,%20kotlin.Int)` method takes this into account, so that adding one month to a date in Shevat gives the proper result (Adar) in a non-leap year.

<br />

| Parameters ||
|---|---|
| `field` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the time field. |
| `amount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the amount to add to the field. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the field is invalid or refers to a field that cannot be handled by this method. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#roll(kotlin.Int,%20kotlin.Int)`

### after

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun after(when: Any!): Boolean
```

Compares the time field records. Equivalent to comparing result of conversion to UTC.

| Parameters ||
|---|---|
| `when` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: the Calendar to be compared with this Calendar. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the current time of this Calendar is after the time of Calendar when; false otherwise. |

### before

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun before(when: Any!): Boolean
```

Compares the time field records. Equivalent to comparing result of conversion to UTC.

| Parameters ||
|---|---|
| `when` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: the Calendar to be compared with this Calendar. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the current time of this Calendar is before the time of Calendar when; false otherwise. |

### clear

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun clear(): Unit
```

Clears the values of all the time fields.

### clear

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun clear(field: Int): Unit
```

Clears the value in the given time field.

| Parameters ||
|---|---|
| `field` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the time field to be cleared. |

### clone

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clone(): Any
```

Overrides Cloneable

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html` | a clone of this instance. |

| Exceptions ||
|---|---|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the `Cloneable` interface. Subclasses that override the `clone` method can also throw this exception to indicate that an instance cannot be cloned. |

### compareTo

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun compareTo(other: Calendar!): Int
```

Compares the times (in millis) represented by two `Calendar` objects.

| Parameters ||
|---|---|
| `o` | the object to be compared. |
| `that` | the `Calendar` to compare to this. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `0` if the time represented by this `Calendar` is equal to the time represented by that `Calendar`, a value less than `0` if the time represented by this is before the time represented by that, and a value greater than `0` if the time represented by this is after the time represented by that. |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the specified object's type prevents it from being compared to this object. |
| `java.lang.NullPointerException` | if that `Calendar` is null. |
| `java.lang.IllegalArgumentException` | if the time of that `Calendar` can't be obtained because of invalid calendar values. |
| --- | --- |

### equals

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun equals(other: Any?): Boolean
```

Compares this calendar to the specified object. The result is `true` if and only if the argument is not `null` and is a `Calendar` object that represents the same calendar as this object.

| Parameters ||
|---|---|
| `obj` | the object to compare with. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the objects are the same; `false` otherwise. |

### fieldDifference

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun fieldDifference(
    when: Date!, 
    field: Int
): Int
```

**\[icu\]** Returns the difference between the given time and the time this calendar object is set to. If this calendar is set *before* the given time, the returned value will be positive. If this calendar is set *after* the given time, the returned value will be negative. The `field` parameter specifies the units of the return value. For example, if `fieldDifference(when, Calendar.MONTH)` returns 3, then this calendar is set to 3 months before , and possibly some additional time less than one month.

As a side effect of this call, this calendar is advanced toward `when` by the given amount. That is, calling this method has the side effect of calling `add(field, n)`, where `n` is the return value.

Usage: To use this method, call it first with the largest field of interest, then with progressively smaller fields. For example:

```kotlin
int y = cal.fieldDifference(when, Calendar.YEAR);
  int m = cal.fieldDifference(when, Calendar.MONTH);
  int d = cal.fieldDifference(when, Calendar.DATE);
```
computes the difference between `cal` and `when` in years, months, and days.

Note: `fieldDifference()` is *asymmetrical*. That is, in the following code:

```kotlin
cal.setTime(date1);
  int m1 = cal.fieldDifference(date2, Calendar.MONTH);
  int d1 = cal.fieldDifference(date2, Calendar.DATE);
  cal.setTime(date2);
  int m2 = cal.fieldDifference(date1, Calendar.MONTH);
  int d2 = cal.fieldDifference(date1, Calendar.DATE);
```
one might expect that `m1 == -m2 && d1 == -d2`. However, this is not generally the case, because of irregularities in the underlying calendar system (e.g., the Gregorian calendar has a varying number of days per month).

| Parameters ||
|---|---|
| `when` | [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)!: the date to compare this calendar's time to |
| `field` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the field in which to compute the result |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the difference, either positive or negative, between this calendar's time and `when`, in terms of `field`. |

### get

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun get(field: Int): Int
```

Returns the value for a given time field.

| Parameters ||
|---|---|
| `field` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the given time field. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the value for the given time field. |

### getActualMaximum

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getActualMaximum(field: Int): Int
```

Returns the maximum value that this field could have, given the current date. For example, with the Gregorian date February 3, 1997 and the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#DAY_OF_MONTH:kotlin.Int` field, the actual maximum is 28; for February 3, 1996 it is 29.

The actual maximum computation ignores smaller fields and the current value of like-sized fields. For example, the actual maximum of the DAY_OF_YEAR or MONTH depends only on the year and supra-year fields. The actual maximum of the DAY_OF_MONTH depends, in addition, on the MONTH field and any other fields at that granularity (such as IS_LEAP_MONTH). The DAY_OF_WEEK_IN_MONTH field does not depend on the current DAY_OF_WEEK; it returns the maximum for any day of week in the current month. Likewise for the WEEK_OF_MONTH and WEEK_OF_YEAR fields.

| Parameters ||
|---|---|
| `field` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the field whose maximum is desired |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the maximum of the given field for the current date of this calendar |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getMaximum(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getLeastMaximum(kotlin.Int)`

### getActualMinimum

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getActualMinimum(field: Int): Int
```

Returns the minimum value that this field could have, given the current date. For most fields, this is the same as `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getMinimum(kotlin.Int)` and `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getGreatestMinimum(kotlin.Int)`. However, some fields, especially those related to week number, are more complicated.

For example, assume `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getMinimalDaysInFirstWeek()` returns 4 and `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getFirstDayOfWeek()` returns SUNDAY. If the first day of the month is Sunday, Monday, Tuesday, or Wednesday there will be four or more days in the first week, so it will be week number 1, and `getActualMinimum(WEEK_OF_MONTH)` will return 1. However, if the first of the month is a Thursday, Friday, or Saturday, there are *not* four days in that week, so it is week number 0, and `getActualMinimum(WEEK_OF_MONTH)` will return 0.

<br />

| Parameters ||
|---|---|
| `field` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the field whose actual minimum value is desired. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the minimum of the given field for the current date of this calendar |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getMinimum(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getGreatestMinimum(kotlin.Int)`

### getAvailableLocales

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getAvailableLocales(): Array<Locale!>!
```

Returns the list of locales for which Calendars are installed.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/util/Locale.html#!>!` | the list of locales for which Calendars are installed. |

### getDateTimeFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDateTimeFormat(
    dateStyle: Int, 
    timeStyle: Int, 
    loc: ULocale!
): DateFormat!
```

**\[icu\]** Returns a `DateFormat` appropriate to this calendar. Subclasses wishing to specialize this behavior should override #handleGetDateFormat.

### getDateTimeFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDateTimeFormat(
    dateStyle: Int, 
    timeStyle: Int, 
    loc: Locale!
): DateFormat!
```

**\[icu\]** Returns a `DateFormat` appropriate to this calendar. Subclasses wishing to specialize this behavior should override #handleGetDateFormat.

### getDisplayName

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDisplayName(loc: ULocale!): String!
```

Returns the name of this calendar in the language of the given locale.

### getDisplayName

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDisplayName(loc: Locale!): String!
```

Returns the name of this calendar in the language of the given locale.

### getFieldCount

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getFieldCount(): Int
```

**\[icu\]** Returns the number of fields defined by this calendar. Valid field arguments to `set()` and `get()` are `0..getFieldCount()-1`.

### getFirstDayOfWeek

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getFirstDayOfWeek(): Int
```

Returns what the first day of the week is, where 1 = `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#SUNDAY:kotlin.Int` and 7 = `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#SATURDAY:kotlin.Int`. e.g., Sunday in US, Monday in France

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the first day of the week, where 1 = `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#SUNDAY:kotlin.Int` and 7 = `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#SATURDAY:kotlin.Int`. |

### getGreatestMinimum

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getGreatestMinimum(field: Int): Int
```

Returns the highest minimum value for the given field if varies. Otherwise same as getMinimum(). For Gregorian, no difference.

| Parameters ||
|---|---|
| `field` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the given time field. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the highest minimum value for the given time field. |

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getInstance(): Calendar!
```

Returns a calendar using the default time zone and locale.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#!` | a Calendar. |

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getInstance(zone: TimeZone!): Calendar!
```

Returns a calendar using the specified time zone and default locale.

| Parameters ||
|---|---|
| `zone` | [TimeZone](https://developer.android.com/reference/kotlin/android/icu/util/TimeZone)!: the time zone to use |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#!` | a Calendar. |

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getInstance(
    zone: TimeZone!, 
    locale: ULocale!
): Calendar!
```

Returns a calendar with the specified time zone and locale.

| Parameters ||
|---|---|
| `zone` | [TimeZone](https://developer.android.com/reference/kotlin/android/icu/util/TimeZone)!: the time zone to use |
| `locale` | [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale)!: the ulocale for the week data |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#!` | a Calendar. |

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getInstance(
    zone: TimeZone!, 
    aLocale: Locale!
): Calendar!
```

Returns a calendar with the specified time zone and locale.

| Parameters ||
|---|---|
| `zone` | [TimeZone](https://developer.android.com/reference/kotlin/android/icu/util/TimeZone)!: the time zone to use |
| `aLocale` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!: the locale for the week data |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#!` | a Calendar. |

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getInstance(locale: ULocale!): Calendar!
```

Returns a calendar using the default time zone and specified locale.

| Parameters ||
|---|---|
| `locale` | [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale)!: the ulocale for the week data |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#!` | a Calendar. |

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getInstance(aLocale: Locale!): Calendar!
```

Returns a calendar using the default time zone and specified locale.

| Parameters ||
|---|---|
| `aLocale` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!: the locale for the week data |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#!` | a Calendar. |

### getKeywordValuesForLocale

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getKeywordValuesForLocale(
    key: String!, 
    locale: ULocale!, 
    commonlyUsed: Boolean
): Array<String!>!
```

**\[icu\]** Given a key and a locale, returns an array of string values in a preferred order that would make a difference. These are all and only those values where the open (creation) of the service with the locale formed from the input locale plus input keyword and that value has different behavior than creation with the input locale alone.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: one of the keys supported by this service. For now, only "calendar" is supported. |
| `locale` | [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale)!: the locale |
| `commonlyUsed` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): if set to true it will return only commonly used values with the given locale in preferred order. Otherwise, it will return all the available values for the locale. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | an array of string values for the given key and the locale. |

### getLeastMaximum

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getLeastMaximum(field: Int): Int
```

Returns the lowest maximum value for the given field if varies. Otherwise same as getMaximum(). e.g., for Gregorian DAY_OF_MONTH, 28.

| Parameters ||
|---|---|
| `field` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the given time field. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the lowest maximum value for the given time field. |

### getMaximum

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMaximum(field: Int): Int
```

Returns the maximum value for the given time field. e.g. for Gregorian DAY_OF_MONTH, 31.

| Parameters ||
|---|---|
| `field` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the given time field. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the maximum value for the given time field. |

### getMinimalDaysInFirstWeek

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMinimalDaysInFirstWeek(): Int
```

Returns what the minimal days required in the first week of the year are. That is, if the first week is defined as one that contains the first day of the first month of a year, getMinimalDaysInFirstWeek returns 1. If the minimal days required must be a full week, getMinimalDaysInFirstWeek returns 7.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the minimal days required in the first week of the year. |

### getMinimum

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMinimum(field: Int): Int
```

Returns the minimum value for the given time field. e.g., for Gregorian DAY_OF_MONTH, 1.

| Parameters ||
|---|---|
| `field` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the given time field. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the minimum value for the given time field. |

### getRepeatedWallTimeOption

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getRepeatedWallTimeOption(): Int
```

**\[icu\]**Gets the behavior for handling wall time repeating multiple times at negative time zone offset transitions.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the behavior for handling repeating wall time, either `WALLTIME_FIRST` or `WALLTIME_LAST`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#setRepeatedWallTimeOption(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#WALLTIME_FIRST:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#WALLTIME_LAST:kotlin.Int`

### getSkippedWallTimeOption

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSkippedWallTimeOption(): Int
```

**\[icu\]**Gets the behavior for handling skipped wall time at positive time zone offset transitions.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the behavior for handling skipped wall time, one of `WALLTIME_FIRST`, `WALLTIME_LAST` and `WALLTIME_NEXT_VALID`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#setSkippedWallTimeOption(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#WALLTIME_FIRST:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#WALLTIME_LAST:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#WALLTIME_NEXT_VALID:kotlin.Int`

### getTemporalMonthCode

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTemporalMonthCode(): String!
```

Gets The Temporal monthCode value corresponding to the month for the date. The value is a string identifier that starts with the literal grapheme "M" followed by two graphemes representing the zero-padded month number of the current month in a normal (non-leap) year and suffixed by an optional literal grapheme "L" if this is a leap month in a lunisolar calendar. The 25 possible values are "M01" .. "M13" and "M01L" .. "M12L". For the Hebrew calendar, the values are "M01" .. "M12" for non-leap year, and "M01" .. "M05", "M05L", "M06" .. "M12" for leap year. For the Chinese calendar, the values are "M01" .. "M12" for non-leap year and in leap year with another monthCode in "M01L" .. "M12L". For Coptic and Ethiopian calendar, the Temporal monthCode values for any years are "M01" to "M13".

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | One of 25 possible strings in {"M01".."M13", "M01L".."M12L"}. |

### getTime

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTime(): Date!
```

Returns this Calendar's current time.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Date.html#!` | the current time. |

### getTimeInMillis

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTimeInMillis(): Long
```

Returns this Calendar's current time as a long.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the current time as UTC milliseconds from the epoch. |

### getTimeZone

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTimeZone(): TimeZone!
```

Returns the time zone.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/util/TimeZone!` | the time zone object associated with this calendar. |

### getType

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getType(): String!
```

**\[icu\]** Returns the calendar type name string for this Calendar object. The returned string is the legacy ICU calendar attribute value, for example, "gregorian" or "japanese".

See type="old type name" for the calendar attribute of locale IDs at http://www.unicode.org/reports/tr35/#Key_Type_Definitions

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | legacy calendar type name string |

### getWeekData

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getWeekData(): Calendar.WeekData!
```

**\[icu\]** Return simple, immutable struct-like class for access to the week data in this calendar.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.WeekData!` | the WeekData for this calendar. |

### getWeekDataForRegion

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getWeekDataForRegion(region: String!): Calendar.WeekData!
```

**\[icu\]** Return simple, immutable struct-like class for access to the CLDR week data.

| Parameters ||
|---|---|
| `region` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The input region. The results are undefined if the region code is not valid. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/util/Calendar.WeekData!` | the WeekData for the input region. It is never null. |

### hashCode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hashCode(): Int
```

Returns a hash code for this calendar.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

### inTemporalLeapYear

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun inTemporalLeapYear(): Boolean
```

**\[icu\]** Returns true if the date is in a leap year. Recalculate the current time field values if the time value has been changed by a call to \* setTime(). This method is semantically const, but may alter the object in memory. A "leap year" is a year that contains more days than other years (for solar or lunar calendars) or more months than other years (for lunisolar calendars like Hebrew or Chinese), as defined in the ECMAScript Temporal proposal.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the date in the fields is in a Temporal proposal defined leap year. False otherwise. |

### isEquivalentTo

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isEquivalentTo(other: Calendar!): Boolean
```

**\[icu\]** Returns true if the given Calendar object is equivalent to this one. An equivalent Calendar will behave exactly as this one does, but it may be set to a different time. By contrast, for the equals() method to return true, the other Calendar must be set to the same time.

| Parameters ||
|---|---|
| `other` | [Calendar](https://developer.android.com/reference/kotlin/android/icu/util/Calendar#)!: the Calendar to be compared with this Calendar |

### isLenient

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isLenient(): Boolean
```

Tell whether date/time interpretation is to be lenient.

### isSet

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isSet(field: Int): Boolean
```

Determines if the given time field has a value set.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the given time field has a value set; false otherwise. |

### isWeekend

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isWeekend(): Boolean
```

**\[icu\]** Returns true if this Calendar's current date and time is in the weekend in this calendar system.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the given date and time is part of the weekend |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#isWeekend(java.util.Date)`

### isWeekend

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isWeekend(date: Date!): Boolean
```

**\[icu\]** Returns true if the given date and time is in the weekend in this calendar system. Equivalent to calling setTime() followed by isWeekend(). Note: This method changes the time this calendar is set to.

| Parameters ||
|---|---|
| `date` | [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)!: the date and time |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the given date and time is part of the weekend |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#isWeekend()`

### roll

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun roll(
    field: Int, 
    up: Boolean
): Unit
```

Rolls (up/down) a single unit of time on the given field. If the field is rolled past its maximum allowable value, it will "wrap" back to its minimum and continue rolling. For example, to roll the current date up by one day, you can call:

``roll(`https://developer.android.com/reference/kotlin/android/icu/util/Calendar#DATE:kotlin.Int`, true)``

When rolling on the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#YEAR:kotlin.Int` field, it will roll the year value in the range between 1 and the value returned by calling `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getMaximum(kotlin.Int)`(`https://developer.android.com/reference/kotlin/android/icu/util/Calendar#YEAR:kotlin.Int`).

When rolling on certain fields, the values of other fields may conflict and need to be changed. For example, when rolling the `MONTH` field for the Gregorian date 1/31/96 upward, the `DAY_OF_MONTH` field must be adjusted so that the result is 2/29/96 rather than the invalid 2/31/96.

Rolling up always means rolling forward in time (unless the limit of the field is reached, in which case it may pin or wrap), so for the Gregorian calendar, starting with 100 BC and rolling the year up results in 99 BC. When eras have a definite beginning and end (as in the Chinese calendar, or as in most eras in the Japanese calendar) then rolling the year past either limit of the era will cause the year to wrap around. When eras only have a limit at one end, then attempting to roll the year past that limit will result in pinning the year at that limit. Note that for most calendars in which era 0 years move forward in time (such as Buddhist, Hebrew, or Islamic), it is possible for add or roll to result in negative years for era 0 (that is the only way to represent years before the calendar epoch in such calendars).

**Note:** Calling `roll(field, true)` N times is *not* necessarily equivalent to calling `roll(field, N)`. For example, imagine that you start with the date Gregorian date January 31, 1995. If you call `roll(Calendar.MONTH, 2)`, the result will be March 31, 1995. But if you call `roll(Calendar.MONTH, true)`, the result will be February 28, 1995. Calling it one more time will give March 28, 1995, which is usually not the desired result.

**Note:** You should always use `roll` and `add` rather than attempting to perform arithmetic operations directly on the fields of a `Calendar`. It is quite possible for `Calendar` subclasses to have fields with non-linear behavior, for example missing months or days during non-leap years. The subclasses' `add` and `roll` methods will take this into account, while simple arithmetic manipulations may give invalid results.

<br />

| Parameters ||
|---|---|
| `field` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the calendar field to roll. |
| `up` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): indicates if the value of the specified time field is to be rolled up or rolled down. Use `true` if rolling up, `false` otherwise. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the field is invalid or refers to a field that cannot be handled by this method. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#roll(kotlin.Int,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#add(kotlin.Int,%20kotlin.Int)`

### roll

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun roll(
    field: Int, 
    amount: Int
): Unit
```

Rolls (up/down) a specified amount time on the given field. For example, to roll the current date up by three days, you can call `roll(Calendar.DATE, 3)`. If the field is rolled past its maximum allowable value, it will "wrap" back to its minimum and continue rolling. For example, calling `roll(Calendar.DATE, 10)` on a Gregorian calendar set to 4/25/96 will result in the date 4/5/96.

When rolling on certain fields, the values of other fields may conflict and need to be changed. For example, when rolling the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#MONTH:kotlin.Int` field for the Gregorian date 1/31/96 by +1, the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#DAY_OF_MONTH:kotlin.Int` field must be adjusted so that the result is 2/29/96 rather than the invalid 2/31/96.

Rolling by a positive value always means rolling forward in time (unless the limit of the field is reached, in which case it may pin or wrap), so for the Gregorian calendar, starting with 100 BC and rolling the year by + 1 results in 99 BC. When eras have a definite beginning and end (as in the Chinese calendar, or as in most eras in the Japanese calendar) then rolling the year past either limit of the era will cause the year to wrap around. When eras only have a limit at one end, then attempting to roll the year past that limit will result in pinning the year at that limit. Note that for most calendars in which era 0 years move forward in time (such as Buddhist, Hebrew, or Islamic), it is possible for add or roll to result in negative years for era 0 (that is the only way to represent years before the calendar epoch in such calendars).

**\[icu\] Note:** the ICU implementation of this method is able to roll all fields except for `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#ERA:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#DST_OFFSET:kotlin.Int`, and `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#ZONE_OFFSET:kotlin.Int`. Subclasses may, of course, add support for additional fields in their overrides of `roll`.

**Note:** You should always use `roll` and `add` rather than attempting to perform arithmetic operations directly on the fields of a `Calendar`. It is quite possible for `Calendar` subclasses to have fields with non-linear behavior, for example missing months or days during non-leap years. The subclasses' `add` and `roll` methods will take this into account, while simple arithmetic manipulations may give invalid results.

**Subclassing:** 
This implementation of `roll` assumes that the behavior of the field is continuous between its minimum and maximum, which are found by calling `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getActualMinimum(kotlin.Int)` and `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getActualMaximum(kotlin.Int)`. For most such fields, simple addition, subtraction, and modulus operations are sufficient to perform the roll. For week-related fields, the results of `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getFirstDayOfWeek()` and `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getMinimalDaysInFirstWeek()` are also necessary. Subclasses can override these two methods if their values differ from the defaults.

Subclasses that have fields for which the assumption of continuity breaks down must override `roll` to handle those fields specially. For example, in the Hebrew calendar the month "Adar I" only occurs in leap years; in other years the calendar jumps from Shevat (month #4) to Adar (month #6). The android.icu.util.HebrewCalendar#roll method takes this into account, so that rolling the month of Shevat by one gives the proper result (Adar) in a non-leap year.

<br />

| Parameters ||
|---|---|
| `field` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the calendar field to roll. |
| `amount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the amount by which the field should be rolled. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the field is invalid or refers to a field that cannot be handled by this method. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#roll(kotlin.Int,%20kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#add(kotlin.Int,%20kotlin.Int)`

### set

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun set(
    field: Int, 
    value: Int
): Unit
```

Sets the time field with the given value.

| Parameters ||
|---|---|
| `field` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the given time field. |
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the value to be set for the given time field. |

### set

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun set(
    year: Int, 
    month: Int, 
    date: Int
): Unit
```

Sets the values for the fields year, month, and date. Previous values of other fields are retained. If this is not desired, call `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#clear()` first.

| Parameters ||
|---|---|
| `year` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the value used to set the YEAR time field. |
| `month` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the value used to set the MONTH time field. Month value is 0-based. e.g., 0 for January. |
| `date` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the value used to set the DATE time field. |
| --- | --- |

### set

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun set(
    year: Int, 
    month: Int, 
    date: Int, 
    hour: Int, 
    minute: Int
): Unit
```

Sets the values for the fields year, month, date, hour, and minute. Previous values of other fields are retained. If this is not desired, call `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#clear()` first.

| Parameters ||
|---|---|
| `year` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the value used to set the YEAR time field. |
| `month` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the value used to set the MONTH time field. Month value is 0-based. e.g., 0 for January. |
| `date` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the value used to set the DATE time field. |
| --- | --- |
| `hour` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the value used to set the HOUR_OF_DAY time field. |
| `minute` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the value used to set the MINUTE time field. |

### set

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun set(
    year: Int, 
    month: Int, 
    date: Int, 
    hour: Int, 
    minute: Int, 
    second: Int
): Unit
```

Sets the values for the fields year, month, date, hour, minute, and second. Previous values of other fields are retained. If this is not desired, call #clear first.

| Parameters ||
|---|---|
| `year` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the value used to set the YEAR time field. |
| `month` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the value used to set the MONTH time field. Month value is 0-based. e.g., 0 for January. |
| `date` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the value used to set the DATE time field. |
| --- | --- |
| `hour` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the value used to set the HOUR_OF_DAY time field. |
| `minute` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the value used to set the MINUTE time field. |
| `second` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the value used to set the SECOND time field. |
| --- | --- |

### setFirstDayOfWeek

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setFirstDayOfWeek(value: Int): Unit
```

Sets what the first day of the week is, where 1 = `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#SUNDAY:kotlin.Int` and 7 = `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#SATURDAY:kotlin.Int`.

| Parameters ||
|---|---|
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the given first day of the week, where 1 = `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#SUNDAY:kotlin.Int` and 7 = `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#SATURDAY:kotlin.Int`. |

### setLenient

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setLenient(lenient: Boolean): Unit
```

Specify whether or not date/time interpretation is to be lenient. With lenient interpretation, a date such as "February 942, 1996" will be treated as being equivalent to the 941st day after February 1, 1996. With strict interpretation, such dates will cause an exception to be thrown.
**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat.html#setLenient(kotlin.Boolean)`

### setMinimalDaysInFirstWeek

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setMinimalDaysInFirstWeek(value: Int): Unit
```

Sets what the minimal days required in the first week of the year are. For example, if the first week is defined as one that contains the first day of the first month of a year, call the method with value 1. If it must be a full week, use value 7.

| Parameters ||
|---|---|
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the given minimal days required in the first week of the year. |

### setRepeatedWallTimeOption

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setRepeatedWallTimeOption(option: Int): Unit
```

**\[icu\]** Sets the behavior for handling wall time repeating multiple times at negative time zone offset transitions. For example, 1:30 AM on November 6, 2011 in US Eastern time (America/New_York) occurs twice; 1:30 AM EDT, then 1:30 AM EST one hour later. When `WALLTIME_FIRST` is used, the wall time 1:30AM in this example will be interpreted as 1:30 AM EDT (first occurrence). When `WALLTIME_LAST` is used, it will be interpreted as 1:30 AM EST (last occurrence). The default value is `WALLTIME_LAST`.

| Parameters ||
|---|---|
| `option` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the behavior for handling repeating wall time, either `WALLTIME_FIRST` or `WALLTIME_LAST`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | when `option` is neither `WALLTIME_FIRST` nor `WALLTIME_LAST`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getRepeatedWallTimeOption()`
- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#WALLTIME_FIRST:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#WALLTIME_LAST:kotlin.Int`

### setSkippedWallTimeOption

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setSkippedWallTimeOption(option: Int): Unit
```

**\[icu\]** Sets the behavior for handling skipped wall time at positive time zone offset transitions. For example, 2:30 AM on March 13, 2011 in US Eastern time (America/New_York) does not exist because the wall time jump from 1:59 AM EST to 3:00 AM EDT. When `WALLTIME_FIRST` is used, 2:30 AM is interpreted as 30 minutes before 3:00 AM EDT, therefore, it will be resolved as 1:30 AM EST. When `WALLTIME_LAST` is used, 2:30 AM is interpreted as 31 minutes after 1:59 AM EST, therefore, it will be resolved as 3:30 AM EDT. When `WALLTIME_NEXT_VALID` is used, 2:30 AM will be resolved as next valid wall time, that is 3:00 AM EDT. The default value is `WALLTIME_LAST`.

**Note:** This option is effective only when this calendar is `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#isLenient()`. When the calendar is strict, such non-existing wall time will cause an exception.

| Parameters ||
|---|---|
| `option` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the behavior for handling skipped wall time at positive time zone offset transitions, one of `WALLTIME_FIRST`, `WALLTIME_LAST` and `WALLTIME_NEXT_VALID`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | when `option` is not any of `WALLTIME_FIRST`, `WALLTIME_LAST` and `WALLTIME_NEXT_VALID`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getSkippedWallTimeOption()`
- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#WALLTIME_FIRST:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#WALLTIME_LAST:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#WALLTIME_NEXT_VALID:kotlin.Int`

### setTemporalMonthCode

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTemporalMonthCode(temporalMonth: String!): Unit
```

Sets The Temporal monthCode which is a string identifier that starts with the literal grapheme "M" followed by two graphemes representing the zero-padded month number of the current month in a normal (non-leap) year and suffixed by an optional literal grapheme "L" if this is a leap month in a lunisolar calendar. The 25 possible values are "M01" .. "M13" and "M01L" .. "M12L". For Hebrew calendar, the values are "M01" .. "M12" for non-leap years, and "M01" .. "M05", "M05L", "M06" .. "M12" for leap year. For the Chinese calendar, the values are "M01" .. "M12" for non-leap year and in leap year with another monthCode in "M01L" .. "M12L". For Coptic and Ethiopian calendar, the Temporal monthCode values for any years are "M01" to "M13".

| Parameters ||
|---|---|
| `temporalMonth` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: One of 25 possible strings in {"M01".. "M12", "M13", "M01L", "M12L"}. |

### setTime

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setTime(date: Date!): Unit
```

Sets this Calendar's current time with the given Date.

Note: Calling `setTime` with `Date(Long.MAX_VALUE)` or `Date(Long.MIN_VALUE)` may yield incorrect field values from `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#get(kotlin.Int)`.

| Parameters ||
|---|---|
| `date` | [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)!: the given Date. |

### setTimeInMillis

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTimeInMillis(millis: Long): Unit
```

Sets this Calendar's current time from the given long value. An IllegalIcuArgumentException is thrown when millis is outside the range permitted by a Calendar object when in strict mode. When in lenient mode the out of range values are pinned to their respective min/max.

| Parameters ||
|---|---|
| `millis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the new time in UTC milliseconds from the epoch. |

### setTimeZone

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTimeZone(value: TimeZone!): Unit
```

Sets the time zone with the given time zone value.

| Parameters ||
|---|---|
| `value` | [TimeZone](https://developer.android.com/reference/kotlin/android/icu/util/TimeZone)!: the given time zone. |

### setWeekData

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setWeekData(wdata: Calendar.WeekData!): Calendar!
```

**\[icu\]** Set data in this calendar based on the WeekData input.

| Parameters ||
|---|---|
| `wdata` | [Calendar.WeekData](https://developer.android.com/reference/kotlin/android/icu/util/Calendar.WeekData)!: The week data to use |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#!` | this, for chaining |

### toString

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Returns a string representation of this calendar. This method is intended to be used only for debugging purposes, and the format of the returned string may vary between implementations. The returned string may be empty but may not be `null`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of this calendar. |

## Protected methods

### complete

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun complete(): Unit
```

Fills in any unset fields in the time field list.

### computeFields

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun computeFields(): Unit
```

Converts the current millisecond time value `time` to field values in `fields[]`. This synchronizes the time field values with a new time that is set for the calendar. The time is *not* recomputed first; to recompute the time, then the fields, call the `complete` method.
**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#complete()`

### computeGregorianFields

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected fun computeGregorianFields(julianDay: Int): Unit
```

Compute the Gregorian calendar year, month, and day of month from the Julian day. These values are not stored in fields, but in member variables gregorianXxx. They are used for time zone computations and by subclasses that are Gregorian derivatives. Subclasses may call this method to perform a Gregorian calendar millis-\>fields computation. To perform a Gregorian calendar fields-\>millis computation, call computeGregorianMonthStart().
**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#computeGregorianMonthStart(kotlin.Int,%20kotlin.Int)`

### computeGregorianMonthStart

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun computeGregorianMonthStart(
    year: Int, 
    month: Int
): Int
```

Compute the Julian day of a month of the Gregorian calendar. Subclasses may call this method to perform a Gregorian calendar fields-\>millis computation. To perform a Gregorian calendar millis-\>fields computation, call computeGregorianFields().

| Parameters ||
|---|---|
| `year` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): extended Gregorian year |
| `month` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): zero-based Gregorian month |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the Julian day number of the day before the first day of the given month in the given extended year |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#computeGregorianFields(kotlin.Int)`

### computeJulianDay

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun computeJulianDay(): Int
```

Compute the Julian day number as specified by this calendar's fields.

### computeMillisInDay

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun computeMillisInDay(): Int
```

**Deprecated:** *ICU 60*

Compute the milliseconds in the day from the fields. This is a value from 0 to 23:59:59.999 inclusive, unless fields are out of range, in which case it can be an arbitrary value. This value reflects local zone wall time.

### computeTime

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun computeTime(): Unit
```

Converts the current field values in `fields[]` to the millisecond time value `time`.

### computeZoneOffset

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun computeZoneOffset(
    millis: Long, 
    millisInDay: Int
): Int
```

**Deprecated:** *ICU 60*

This method can assume EXTENDED_YEAR has been set.

| Parameters ||
|---|---|
| `millis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): milliseconds of the date fields (local midnight millis) |
| `millisInDay` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): milliseconds of the time fields; may be out or range. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | total zone offset (raw + DST) for the given moment |

### fieldName

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun fieldName(field: Int): String!
```

Returns a string name for a field, for debugging and exceptions.

### floorDivide

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected static fun floorDivide(
    numerator: Int, 
    denominator: Int
): Int
```

Divide two integers, returning the floor of the quotient.

Unlike the built-in division, this is mathematically well-behaved. E.g., `-1/4` =\> 0 but `floorDivide(-1,4)` =\> -1.

| Parameters ||
|---|---|
| `numerator` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the numerator |
| `denominator` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): a divisor which must be \> 0 |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the floor of the quotient. |

### floorDivide

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected static fun floorDivide(
    numerator: Int, 
    denominator: Int, 
    remainder: IntArray!
): Int
```

Divide two integers, returning the floor of the quotient, and the modulus remainder.

Unlike the built-in division, this is mathematically well-behaved. E.g., `-1/4` =\> 0 and `-1%4` =\> -1, but `floorDivide(-1,4)` =\> -1 with `remainder[0]` =\> 3.

| Parameters ||
|---|---|
| `numerator` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the numerator |
| `denominator` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): a divisor which must be \> 0 |
| `remainder` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!: an array of at least one element in which the value `numerator mod denominator` is returned. Unlike `numerator % denominator`, this will always be non-negative. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the floor of the quotient. |

### floorDivide

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected static fun floorDivide(
    numerator: Long, 
    denominator: Int, 
    remainder: IntArray!
): Int
```

Divide two integers, returning the floor of the quotient, and the modulus remainder.

Unlike the built-in division, this is mathematically well-behaved. E.g., `-1/4` =\> 0 and `-1%4` =\> -1, but `floorDivide(-1,4)` =\> -1 with `remainder[0]` =\> 3.

| Parameters ||
|---|---|
| `numerator` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the numerator |
| `denominator` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): a divisor which must be \> 0 |
| `remainder` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!: an array of at least one element in which the value `numerator mod denominator` is returned. Unlike `numerator % denominator`, this will always be non-negative. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the floor of the quotient. |

### floorDivide

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected static fun floorDivide(
    numerator: Long, 
    denominator: Long
): Long
```

Divide two long integers, returning the floor of the quotient.

Unlike the built-in division, this is mathematically well-behaved. E.g., `-1/4` =\> 0 but `floorDivide(-1,4)` =\> -1.

| Parameters ||
|---|---|
| `numerator` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the numerator |
| `denominator` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): a divisor which must be \> 0 |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the floor of the quotient. |

### getFieldResolutionTable

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun getFieldResolutionTable(): Array<Array<IntArray!>!>!
```

Returns the field resolution array for this calendar. Calendars that define additional fields or change the semantics of existing fields should override this method to adjust the field resolution semantics accordingly. Other subclasses should not override this method.
**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#resolveFields(kotlin.Array)`

### getGregorianDayOfMonth

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected fun getGregorianDayOfMonth(): Int
```

Returns the day of month (1-based) on the Gregorian calendar as computed by `computeGregorianFields()`.
**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#computeGregorianFields(kotlin.Int)`

### getGregorianDayOfYear

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected fun getGregorianDayOfYear(): Int
```

Returns the day of year (1-based) on the Gregorian calendar as computed by `computeGregorianFields()`.
**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#computeGregorianFields(kotlin.Int)`

### getGregorianMonth

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected fun getGregorianMonth(): Int
```

Returns the month (0-based) on the Gregorian calendar as computed by `computeGregorianFields()`.
**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#computeGregorianFields(kotlin.Int)`

### getGregorianYear

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected fun getGregorianYear(): Int
```

Returns the extended year on the Gregorian calendar as computed by `computeGregorianFields()`.
**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#computeGregorianFields(kotlin.Int)`

### getLimit

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun getLimit(
    field: Int, 
    limitType: Int
): Int
```

Returns a limit for a field.

| Parameters ||
|---|---|
| `field` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the field, from 0..`getFieldCount()-1` |
| `limitType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the type specifier for the limit |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#MINIMUM:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#GREATEST_MINIMUM:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#LEAST_MAXIMUM:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#MAXIMUM:kotlin.Int`

### getStamp

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected fun getStamp(field: Int): Int
```

Returns the timestamp of a field.

### gregorianMonthLength

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected static fun gregorianMonthLength(
    y: Int, 
    m: Int
): Int
```

Returns the length of a month of the Gregorian calendar.

| Parameters ||
|---|---|
| `y` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the extended year |
| `m` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the 0-based month number |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the number of days in the given month |

### gregorianPreviousMonthLength

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected static fun gregorianPreviousMonthLength(
    y: Int, 
    m: Int
): Int
```

Returns the length of a previous month of the Gregorian calendar.

| Parameters ||
|---|---|
| `y` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the extended year |
| `m` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the 0-based month number |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the number of days in the month previous to the given month |

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

The default implementation in `Calendar` implements a pure proleptic Gregorian calendar.

### handleComputeJulianDay

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun handleComputeJulianDay(bestField: Int): Int
```

Subclasses may override this. This method calls handleGetMonthLength() to obtain the calendar-specific month length.

### handleComputeMonthStart

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected abstract fun handleComputeMonthStart(
    eyear: Int, 
    month: Int, 
    useMonth: Boolean
): Int
```

Returns the Julian day number of day before the first day of the given month in the given extended year. Subclasses should override this method to implement their calendar system.

| Parameters ||
|---|---|
| `eyear` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the extended year |
| `month` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the zero-based month, or 0 if useMonth is false |
| `useMonth` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): if false, compute the day before the first day of the given year, otherwise, compute the day before the first day of the given month |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the Julian day number of the day before the first day of the given month and year |

### handleCreateFields

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun handleCreateFields(): IntArray!
```

Subclasses that use additional fields beyond those defined in `Calendar` should override this method to return an `int[]` array of the appropriate length. The length must be at least `BASE_FIELD_COUNT` and no more than `MAX_FIELD_COUNT`.

### handleGetDateFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun handleGetDateFormat(
    pattern: String!, 
    locale: ULocale!
): DateFormat!
```

Creates a `DateFormat` appropriate to this calendar. This is a framework method for subclasses to override. This method is responsible for creating the calendar-specific DateFormat and DateFormatSymbols objects as needed.

| Parameters ||
|---|---|
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the pattern, specific to the `DateFormat` subclass |
| `locale` | [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale)!: the locale for which the symbols should be drawn |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat.html#!` | a `DateFormat` appropriate to this calendar |

### handleGetDateFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun handleGetDateFormat(
    pattern: String!, 
    override: String!, 
    locale: Locale!
): DateFormat!
```

Creates a `DateFormat` appropriate to this calendar. This is a framework method for subclasses to override. This method is responsible for creating the calendar-specific DateFormat and DateFormatSymbols objects as needed.

| Parameters ||
|---|---|
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the pattern, specific to the `DateFormat` subclass |
| `override` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The override string. A numbering system override string can take one of the following forms: 1). If just a numbering system name is specified, it applies to all numeric fields in the date format pattern. 2). To specify an alternate numbering system on a field by field basis, use the field letters from the pattern followed by an = sign, followed by the numbering system name. For example, to specify that just the year be formatted using Hebrew digits, use the override "y=hebr". Multiple overrides can be specified in a single string by separating them with a semi-colon. For example, the override string "m=thai;y=deva" would format using Thai digits for the month and Devanagari digits for the year. |
| `locale` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!: the locale for which the symbols should be drawn |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat.html#!` | a `DateFormat` appropriate to this calendar |

### handleGetDateFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun handleGetDateFormat(
    pattern: String!, 
    locale: Locale!
): DateFormat!
```

Creates a `DateFormat` appropriate to this calendar. This is a framework method for subclasses to override. This method is responsible for creating the calendar-specific DateFormat and DateFormatSymbols objects as needed.

| Parameters ||
|---|---|
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the pattern, specific to the `DateFormat` subclass |
| `locale` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!: the locale for which the symbols should be drawn |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/DateFormat.html#!` | a `DateFormat` appropriate to this calendar |

### handleGetExtendedYear

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected abstract fun handleGetExtendedYear(): Int
```

Returns the extended year defined by the current fields. This will use the EXTENDED_YEAR field or the YEAR and supra-year fields (such as ERA) specific to the calendar system, depending on which set of fields is newer.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the extended year |

### handleGetLimit

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected abstract fun handleGetLimit(
    field: Int, 
    limitType: Int
): Int
```

Subclass API for defining limits of different types. Subclasses must implement this method to return limits for the following fields:

```kotlin
ERA
  YEAR
  MONTH
  WEEK_OF_YEAR
  WEEK_OF_MONTH
  DAY_OF_MONTH
  DAY_OF_YEAR
  DAY_OF_WEEK_IN_MONTH
  YEAR_WOY
  EXTENDED_YEAR
```

<br />

| Parameters ||
|---|---|
| `field` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): one of the above field numbers |
| `limitType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): one of `MINIMUM`, `GREATEST_MINIMUM`, `LEAST_MAXIMUM`, or `MAXIMUM` |

### handleGetMonthLength

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun handleGetMonthLength(
    extendedYear: Int, 
    month: Int
): Int
```

Returns the number of days in the given month of the given extended year of this calendar system. Subclasses should override this method if they can provide a more correct or more efficient implementation than the default implementation in Calendar.

### handleGetYearLength

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun handleGetYearLength(eyear: Int): Int
```

Returns the number of days in the given extended year of this calendar system. Subclasses should override this method if they can provide a more correct or more efficient implementation than the default implementation in Calendar.

### internalGet

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected fun internalGet(field: Int): Int
```

Returns the value for a given time field. This is an internal method for subclasses that does *not* trigger any calculations.

| Parameters ||
|---|---|
| `field` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the given time field. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the value for the given time field. |

### internalGet

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected fun internalGet(
    field: Int, 
    defaultValue: Int
): Int
```

Returns the value for a given time field, or return the given default value if the field is not set. This is an internal method for subclasses that does *not* trigger any calculations.

| Parameters ||
|---|---|
| `field` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the given time field. |
| `defaultValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): value to return if field is not set |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the value for the given time field of defaultValue if the field is unset |

### internalGetTimeInMillis

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected fun internalGetTimeInMillis(): Long
```

Returns the current milliseconds without recomputing.

### internalSet

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected fun internalSet(
    field: Int, 
    value: Int
): Unit
```

Set a field to a value. Subclasses should use this method when computing fields. It sets the time stamp in the `stamp[]` array to `INTERNALLY_SET`. If a field that may not be set by subclasses is passed in, an `IllegalArgumentException` is thrown. This prevents subclasses from modifying fields that are intended to be calendar-system invariant.

### isGregorianLeapYear

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected static fun isGregorianLeapYear(year: Int): Boolean
```

Determines if the given year is a leap year. Returns true if the given year is a leap year.

| Parameters ||
|---|---|
| `year` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the given year. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the given year is a leap year; false otherwise. |

### julianDayToDayOfWeek

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected static fun julianDayToDayOfWeek(julian: Int): Int
```

Returns the day of week, from SUNDAY to SATURDAY, given a Julian day.

### julianDayToMillis

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected static fun julianDayToMillis(julian: Int): Long
```

Converts Julian day to time as milliseconds.

| Parameters ||
|---|---|
| `julian` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the given Julian day number. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | time as milliseconds. |

### millisToJulianDay

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected static fun millisToJulianDay(millis: Long): Int
```

Converts time as milliseconds to Julian day.

| Parameters ||
|---|---|
| `millis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the given milliseconds. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the Julian day number. |

### newerField

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun newerField(
    defaultField: Int, 
    alternateField: Int
): Int
```

Returns the field that is newer, either defaultField, or alternateField. If neither is newer or neither is set, return defaultField.

### newestStamp

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun newestStamp(
    first: Int, 
    last: Int, 
    bestStampSoFar: Int
): Int
```

Returns the newest stamp of a given range of fields.

### pinField

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun pinField(field: Int): Unit
```

Adjust the specified field so that it is within the allowable range for the date to which this calendar is set. For example, in a Gregorian calendar pinning the `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#DAY_OF_MONTH:kotlin.Int` field for a calendar set to April 31 would cause it to be set to April 30.

**Subclassing:** 
This utility method is intended for use by subclasses that need to implement their own overrides of #roll and `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#add(kotlin.Int,%20kotlin.Int)`.

**Note:** `pinField` is implemented in terms of `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getActualMinimum(kotlin.Int)` and `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getActualMaximum(kotlin.Int)`. If either of those methods uses a slow, iterative algorithm for a particular field, it would be unwise to attempt to call `pinField` for that field. If you really do need to do so, you should override this method to do something more efficient for that field.

<br />

| Parameters ||
|---|---|
| `field` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The calendar field whose value should be pinned. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getActualMinimum(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getActualMaximum(kotlin.Int)`

### prepareGetActual

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun prepareGetActual(
    field: Int, 
    isMinimum: Boolean
): Unit
```

Prepare this calendar for computing the actual minimum or maximum. This method modifies this calendar's fields; it is called on a temporary calendar.

Rationale: The semantics of getActualXxx() is to return the maximum or minimum value that the given field can take, taking into account other relevant fields. In general these other fields are larger fields. For example, when computing the actual maximum DAY_OF_MONTH, the current value of DAY_OF_MONTH itself is ignored, as is the value of any field smaller.

The time fields all have fixed minima and maxima, so we don't need to worry about them. This also lets us set the MILLISECONDS_IN_DAY to zero to erase any effects the time fields might have when computing date fields.

DAY_OF_WEEK is adjusted specially for the WEEK_OF_MONTH and WEEK_OF_YEAR fields to ensure that they are computed correctly.

### resolveFields

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun resolveFields(precedenceTable: Array<Array<IntArray!>!>!): Int
```

Given a precedence table, return the newest field combination in the table, or -1 if none is found.

The precedence table is a 3-dimensional array of integers. It may be thought of as an array of groups. Each group is an array of lines. Each line is an array of field numbers. Within a line, if all fields are set, then the time stamp of the line is taken to be the stamp of the most recently set field. If any field of a line is unset, then the line fails to match. Within a group, the line with the newest time stamp is selected. The first field of the line is returned to indicate which line matched.

In some cases, it may be desirable to map a line to field that whose stamp is NOT examined. For example, if the best field is DAY_OF_WEEK then the DAY_OF_WEEK_IN_MONTH algorithm may be used. In order to do this, insert the value `REMAP_RESOLVE | F` at the start of the line, where `F` is the desired return field value. This field will NOT be examined; it only determines the return value if the other fields in the line are the newest.
| --- | --- |

If all lines of a group contain at least one unset field, then no line will match, and the group as a whole will fail to match. In that case, the next group will be processed. If all groups fail to match, then -1 is returned.

### validateField

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun validateField(field: Int): Unit
```

Validate a single field of this calendar. Subclasses should override this method to validate any calendar-specific fields. Generic fields can be handled by `Calendar.validateField()`.
**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#validateField(kotlin.Int,%20kotlin.Int,%20kotlin.Int)`

### validateField

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected fun validateField(
    field: Int, 
    min: Int, 
    max: Int
): Unit
```

Validate a single field of this calendar given its minimum and maximum allowed value. If the field is out of range, throw a descriptive `IllegalArgumentException`. Subclasses may use this method in their implementation of `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#validateField(kotlin.Int)`.

### validateFields

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun validateFields(): Unit
```

Ensure that each field is within its valid range by calling `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#validateField(kotlin.Int)` on each field that has been set. This method should only be called if this calendar is not lenient.
**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#isLenient()`
- `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#validateField(kotlin.Int)`

### weekNumber

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected fun weekNumber(
    dayOfPeriod: Int, 
    dayOfWeek: Int
): Int
```

Returns the week number of a day, within a period. This may be the week number in a year, or the week number in a month. Usually this will be a value \>= 1, but if some initial days of the period are excluded from week 1, because `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getMinimalDaysInFirstWeek()` is \> 1, then the week number will be zero for those initial days. This method requires the day of week for the given date in order to determine the result.

**Subclassing:** 
This method is intended for use by subclasses in implementing their `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#computeTime()` and/or `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#computeFields()` methods. It is often useful in `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getActualMinimum(kotlin.Int)` and `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getActualMaximum(kotlin.Int)` as well.

<br />

| Parameters ||
|---|---|
| `dayOfPeriod` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#DAY_OF_YEAR:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#DAY_OF_MONTH:kotlin.Int` whose week number is desired. Should be 1 for the first day of the period. |
| `dayOfWeek` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#DAY_OF_WEEK:kotlin.Int` for the day corresponding to the `dayOfPeriod` parameter. 1-based with 1=Sunday. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The week number (one-based), or zero if the day falls before the first week because `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getMinimalDaysInFirstWeek()` is more than one. |

### weekNumber

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun weekNumber(
    desiredDay: Int, 
    dayOfPeriod: Int, 
    dayOfWeek: Int
): Int
```

Returns the week number of a day, within a period. This may be the week number in a year or the week number in a month. Usually this will be a value \>= 1, but if some initial days of the period are excluded from week 1, because `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getMinimalDaysInFirstWeek()` is \> 1, then the week number will be zero for those initial days. This method requires the day number and day of week for some known date in the period in order to determine the day of week on the desired day.

**Subclassing:** 
This method is intended for use by subclasses in implementing their `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#computeTime()` and/or `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#computeFields()` methods. It is often useful in `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getActualMinimum(kotlin.Int)` and `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getActualMaximum(kotlin.Int)` as well.

This variant is handy for computing the week number of some other day of a period (often the first or last day of the period) when its day of the week is not known but the day number and day of week for some other day in the period (e.g. the current date) *is* known.

<br />

| Parameters ||
|---|---|
| `desiredDay` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#DAY_OF_YEAR:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#DAY_OF_MONTH:kotlin.Int` whose week number is desired. Should be 1 for the first day of the period. |
| `dayOfPeriod` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#DAY_OF_YEAR:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#DAY_OF_MONTH:kotlin.Int` for a day in the period whose `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#DAY_OF_WEEK:kotlin.Int` is specified by the `dayOfWeek` parameter. Should be 1 for first day of period. |
| `dayOfWeek` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#DAY_OF_WEEK:kotlin.Int` for the day corresponding to the `dayOfPeriod` parameter. 1-based with 1=Sunday. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The week number (one-based), or zero if the day falls before the first week because `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#getMinimalDaysInFirstWeek()` is more than one. |

## Properties

### MAX_DATE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected static val MAX_DATE: Date!
```

The maximum supported `Date`. This value is equivalent to `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#MAX_JULIAN:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#MAX_MILLIS:kotlin.Long`.

### MIN_DATE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected static val MIN_DATE: Date!
```

The minimum supported `Date`. This value is equivalent to `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#MIN_JULIAN:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/icu/util/Calendar#MIN_MILLIS:kotlin.Long`.
