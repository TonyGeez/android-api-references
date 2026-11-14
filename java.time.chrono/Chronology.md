Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Chronology

```
interface Chronology : Comparable<Chronology!>
```

| [java.time.chrono.Chronology](https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#) |

Known Direct Subclasses [AbstractChronology](https://developer.android.com/reference/kotlin/java/time/chrono/AbstractChronology) [AbstractChronology](https://developer.android.com/reference/kotlin/java/time/chrono/AbstractChronology) An abstract implementation of a calendar system, used to organize and identify dates.
Known Indirect Subclasses [HijrahChronology](https://developer.android.com/reference/kotlin/java/time/chrono/HijrahChronology), [IsoChronology](https://developer.android.com/reference/kotlin/java/time/chrono/IsoChronology), [JapaneseChronology](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseChronology), [MinguoChronology](https://developer.android.com/reference/kotlin/java/time/chrono/MinguoChronology), [ThaiBuddhistChronology](https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistChronology) [HijrahChronology](https://developer.android.com/reference/kotlin/java/time/chrono/HijrahChronology) The Hijrah calendar is a lunar calendar supporting Islamic calendars.
[IsoChronology](https://developer.android.com/reference/kotlin/java/time/chrono/IsoChronology) The ISO calendar system.
[JapaneseChronology](https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseChronology) The Japanese Imperial calendar system.
[MinguoChronology](https://developer.android.com/reference/kotlin/java/time/chrono/MinguoChronology) The Minguo calendar system.
[ThaiBuddhistChronology](https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistChronology) The Thai Buddhist calendar system.

A calendar system, used to organize and identify dates.

The main date and time API is built on the ISO calendar system. The chronology operates behind the scenes to represent the general concept of a calendar system. For example, the Japanese, Minguo, Thai Buddhist and others.

Most other calendar systems also operate on the shared concepts of year, month and day, linked to the cycles of the Earth around the Sun, and the Moon around the Earth. These shared concepts are defined by `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#` and are available for use by any `Chronology` implementation:

```kotlin
LocalDate isoDate = ...
    ThaiBuddhistDate thaiDate = ...
    int isoYear = isoDate.get(ChronoField.YEAR);
    int thaiYear = thaiDate.get(ChronoField.YEAR);
  
```
As shown, although the date objects are in different calendar systems, represented by different `Chronology` instances, both can be queried using the same constant on `ChronoField`. For a full discussion of the implications of this, see `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate`. In general, the advice is to use the known ISO-based `LocalDate`, rather than `ChronoLocalDate`.

While a `Chronology` object typically uses `ChronoField` and is based on an era, year-of-era, month-of-year, day-of-month model of a date, this is not required. A `Chronology` instance may represent a totally different kind of calendar system, such as the Mayan.

In practical terms, the `Chronology` instance also acts as a factory. The `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#of(kotlin.String)` method allows an instance to be looked up by identifier, while the `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#ofLocale(java.util.Locale)` method allows lookup by locale.

The `Chronology` instance provides a set of methods to create `ChronoLocalDate` instances. The date classes are used to manipulate specific dates.

- `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#dateNow()`
- `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#dateNow(java.time.Clock)`
- `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#dateNow(java.time.ZoneId)`
- `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#date(kotlin.Int,%20kotlin.Int,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#date(java.time.chrono.Era,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#dateYearDay(kotlin.Int,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#dateYearDay(java.time.chrono.Era,%20kotlin.Int,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#date(java.time.temporal.TemporalAccessor)`

## Adding New Calendars

The set of available chronologies can be extended by applications. Adding a new calendar system requires the writing of an implementation of `Chronology`, `ChronoLocalDate` and `Era`. The majority of the logic specific to the calendar system will be in the `ChronoLocalDate` implementation. The `Chronology` implementation acts as a factory.

To permit the discovery of additional chronologies, the `https://developer.android.com/reference/kotlin/java/util/ServiceLoader.html#` is used. A file must be added to the `META-INF/services` directory with the name 'java.time.chrono.Chronology' listing the implementation classes. See the ServiceLoader for more details on service loading. For lookup by id or calendarType, the system provided calendars are found first followed by application provided calendars.

Each chronology must define a chronology ID that is unique within the system. If the chronology represents a calendar system defined by the CLDR specification then the calendar type is the concatenation of the CLDR type and, if applicable, the CLDR variant.

## Summary

| Public methods ||
|---|---|
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#compareTo(java.time.chrono.Chronology)(other: https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#!)` Compares this chronology to another chronology. |
| abstract [ChronoLocalDate](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate)! | `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#date(kotlin.Int,%20kotlin.Int,%20kotlin.Int)(prolepticYear: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, month: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, dayOfMonth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Obtains a local date in this chronology from the proleptic-year, month-of-year and day-of-month fields. |
| open [ChronoLocalDate](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate)! | `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#date(java.time.chrono.Era,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(era: https://developer.android.com/reference/kotlin/java/time/chrono/Era!, yearOfEra: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, month: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, dayOfMonth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Obtains a local date in this chronology from the era, year-of-era, month-of-year and day-of-month fields. |
| abstract [ChronoLocalDate](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate)! | `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#date(java.time.temporal.TemporalAccessor)(temporal: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor.html#!)` Obtains a local date in this chronology from another temporal object. |
| abstract [ChronoLocalDate](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate)! | `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#dateEpochDay(kotlin.Long)(epochDay: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Obtains a local date in this chronology from the epoch-day. |
| open [ChronoLocalDate](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate)! | `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#dateNow()()` Obtains the current local date in this chronology from the system clock in the default time-zone. |
| open [ChronoLocalDate](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate)! | `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#dateNow(java.time.Clock)(clock: https://developer.android.com/reference/kotlin/java/time/Clock.html#!)` Obtains the current local date in this chronology from the specified clock. |
| open [ChronoLocalDate](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate)! | `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#dateNow(java.time.ZoneId)(zone: https://developer.android.com/reference/kotlin/java/time/ZoneId.html#!)` Obtains the current local date in this chronology from the system clock in the specified time-zone. |
| abstract [ChronoLocalDate](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate)! | `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#dateYearDay(kotlin.Int,%20kotlin.Int)(prolepticYear: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, dayOfYear: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Obtains a local date in this chronology from the proleptic-year and day-of-year fields. |
| open [ChronoLocalDate](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate)! | `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#dateYearDay(java.time.chrono.Era,%20kotlin.Int,%20kotlin.Int)(era: https://developer.android.com/reference/kotlin/java/time/chrono/Era!, yearOfEra: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, dayOfYear: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Obtains a local date in this chronology from the era, year-of-era and day-of-year fields. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#epochSecond(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20java.time.ZoneOffset)(prolepticYear: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, month: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, dayOfMonth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, hour: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, minute: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, second: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, zoneOffset: https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#!)` Gets the number of seconds from the epoch of 1970-01-01T00:00:00Z. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#epochSecond(java.time.chrono.Era,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20java.time.ZoneOffset)(era: https://developer.android.com/reference/kotlin/java/time/chrono/Era!, yearOfEra: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, month: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, dayOfMonth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, hour: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, minute: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, second: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, zoneOffset: https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#!)` Gets the number of seconds from the epoch of 1970-01-01T00:00:00Z. |
| abstract [Era](https://developer.android.com/reference/kotlin/java/time/chrono/Era)! | `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#eraOf(kotlin.Int)(eraValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Creates the chronology era object from the numeric value. |
| abstract [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Era](https://developer.android.com/reference/kotlin/java/time/chrono/Era)!\>! | `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#eras()()` Gets the list of eras for the chronology. |
| open static [Chronology](https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#)! | `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#from(java.time.temporal.TemporalAccessor)(temporal: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor.html#!)` Obtains an instance of `Chronology` from a temporal object. |
| open static [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [Chronology](https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#)!\>! | `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#getAvailableChronologies()()` Returns the available chronologies. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#getCalendarType()()` Gets the calendar type of the calendar system. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#getDisplayName(java.time.format.TextStyle,%20java.util.Locale)(style: https://developer.android.com/reference/kotlin/java/time/format/TextStyle.html#!, locale: https://developer.android.com/reference/kotlin/java/util/Locale.html#!)` Gets the textual representation of this chronology. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#getId()()` Gets the ID of the chronology. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#isIsoBased()()` Checks if this chronology is ISO based. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#isLeapYear(kotlin.Long)(prolepticYear: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Checks if the specified year is a leap year. |
| open [ChronoLocalDateTime](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime)\<out [ChronoLocalDate](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate)!\>! | `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#localDateTime(java.time.temporal.TemporalAccessor)(temporal: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor.html#!)` Obtains a local date-time in this chronology from another temporal object. |
| open static [Chronology](https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#)! | `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#of(kotlin.String)(id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Obtains an instance of `Chronology` from a chronology ID or calendar system type. |
| open static [Chronology](https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#)! | `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#ofLocale(java.util.Locale)(locale: https://developer.android.com/reference/kotlin/java/util/Locale.html#!)` Obtains an instance of `Chronology` from a locale. |
| open [ChronoPeriod](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoPeriod)! | `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#period(kotlin.Int,%20kotlin.Int,%20kotlin.Int)(years: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, months: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, days: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Obtains a period for this chronology based on years, months and days. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#prolepticYear(java.time.chrono.Era,%20kotlin.Int)(era: https://developer.android.com/reference/kotlin/java/time/chrono/Era!, yearOfEra: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Calculates the proleptic-year given the era and year-of-era. |
| abstract [ValueRange](https://developer.android.com/reference/kotlin/java/time/temporal/ValueRange.html#)! | `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#range(java.time.temporal.ChronoField)(field: https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#!)` Gets the range of valid values for the specified field. |
| abstract [ChronoLocalDate](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate)! | `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#resolveDate(kotlin.collections.MutableMap,%20java.time.format.ResolverStyle)(fieldValues: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html!>!, resolverStyle: https://developer.android.com/reference/kotlin/java/time/format/ResolverStyle.html#!)` Resolves parsed `ChronoField` values into a date during parsing. |
| open [ChronoZonedDateTime](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime)\<out [ChronoLocalDate](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate)!\>! | `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#zonedDateTime(java.time.Instant,%20java.time.ZoneId)(instant: https://developer.android.com/reference/kotlin/java/time/Instant.html#!, zone: https://developer.android.com/reference/kotlin/java/time/ZoneId.html#!)` Obtains a `ChronoZonedDateTime` in this chronology from an `Instant`. |
| open [ChronoZonedDateTime](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime)\<out [ChronoLocalDate](https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate)!\>! | `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#zonedDateTime(java.time.temporal.TemporalAccessor)(temporal: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor.html#!)` Obtains a `ChronoZonedDateTime` in this chronology from another temporal object. |

## Public methods

### compareTo

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun compareTo(other: Chronology!): Int
```

Compares this chronology to another chronology.

The comparison order first by the chronology ID string, then by any additional information specific to the subclass. It is "consistent with equals", as defined by `https://developer.android.com/reference/kotlin/java/lang/Comparable.html#`.

| Parameters ||
|---|---|
| `o` | the object to be compared. |
| `other` | [Chronology](https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#)!: the other chronology to compare to, not null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the comparator value, that is this ID string compared with the `other`'s ID string unless the ID strings are equal and the chronology distinguishes instances using additional information |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the specified object's type prevents it from being compared to this object. |
| `java.lang.NullPointerException` | if the specified object is null |

### date

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun date(
    prolepticYear: Int, 
    month: Int, 
    dayOfMonth: Int
): ChronoLocalDate!
```

Obtains a local date in this chronology from the proleptic-year, month-of-year and day-of-month fields.

| Parameters ||
|---|---|
| `prolepticYear` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the chronology proleptic-year |
| `month` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the chronology month-of-year |
| `dayOfMonth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the chronology day-of-month |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate!` | the local date in this chronology, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if unable to create the date |

### date

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun date(
    era: Era!, 
    yearOfEra: Int, 
    month: Int, 
    dayOfMonth: Int
): ChronoLocalDate!
```

Obtains a local date in this chronology from the era, year-of-era, month-of-year and day-of-month fields.

| Parameters ||
|---|---|
| `era` | [Era](https://developer.android.com/reference/kotlin/java/time/chrono/Era)!: the era of the correct type for the chronology, not null |
| `yearOfEra` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the chronology year-of-era |
| `month` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the chronology month-of-year |
| `dayOfMonth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the chronology day-of-month |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate!` | the local date in this chronology, not null |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the `era` is not of the correct type for the chronology |
| `java.time.DateTimeException` | if unable to create the date |

### date

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun date(temporal: TemporalAccessor!): ChronoLocalDate!
```

Obtains a local date in this chronology from another temporal object.

This obtains a date in this chronology based on the specified temporal. A `TemporalAccessor` represents an arbitrary set of date and time information, which this factory converts to an instance of `ChronoLocalDate`.

The conversion typically uses the `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#` field, which is standardized across calendar systems.

This method matches the signature of the functional interface `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery.html#` allowing it to be used as a query via method reference, `aChronology::date`.

| Parameters ||
|---|---|
| `temporal` | [TemporalAccessor](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor.html#)!: the temporal object to convert, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate!` | the local date in this chronology, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if unable to create the date |

**See Also**

- `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate#from(java.time.temporal.TemporalAccessor)`

### dateEpochDay

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun dateEpochDay(epochDay: Long): ChronoLocalDate!
```

Obtains a local date in this chronology from the epoch-day.

The definition of `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#` is the same for all calendar systems, thus it can be used for conversion.

| Parameters ||
|---|---|
| `epochDay` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the epoch day |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate!` | the local date in this chronology, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if unable to create the date |

### dateNow

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dateNow(): ChronoLocalDate!
```

Obtains the current local date in this chronology from the system clock in the default time-zone.

This will query the `https://developer.android.com/reference/kotlin/java/time/Clock.html#systemDefaultZone()` in the default time-zone to obtain the current date.

Using this method will prevent the ability to use an alternate clock for testing because the clock is hard-coded.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate!` | the current local date using the system clock and default time-zone, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if unable to create the date |

### dateNow

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dateNow(clock: Clock!): ChronoLocalDate!
```

Obtains the current local date in this chronology from the specified clock.

This will query the specified clock to obtain the current date - today. Using this method allows the use of an alternate clock for testing. The alternate clock may be introduced using `https://developer.android.com/reference/kotlin/java/time/Clock.html#`.

| Parameters ||
|---|---|
| `clock` | [Clock](https://developer.android.com/reference/kotlin/java/time/Clock.html#)!: the clock to use, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate!` | the current local date, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if unable to create the date |

### dateNow

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dateNow(zone: ZoneId!): ChronoLocalDate!
```

Obtains the current local date in this chronology from the system clock in the specified time-zone.

This will query the `https://developer.android.com/reference/kotlin/java/time/Clock.html#system(java.time.ZoneId)` to obtain the current date. Specifying the time-zone avoids dependence on the default time-zone.

Using this method will prevent the ability to use an alternate clock for testing because the clock is hard-coded.

| Parameters ||
|---|---|
| `zone` | [ZoneId](https://developer.android.com/reference/kotlin/java/time/ZoneId.html#)!: the zone ID to use, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate!` | the current local date using the system clock, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if unable to create the date |

### dateYearDay

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun dateYearDay(
    prolepticYear: Int, 
    dayOfYear: Int
): ChronoLocalDate!
```

Obtains a local date in this chronology from the proleptic-year and day-of-year fields.

| Parameters ||
|---|---|
| `prolepticYear` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the chronology proleptic-year |
| `dayOfYear` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the chronology day-of-year |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate!` | the local date in this chronology, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if unable to create the date |

### dateYearDay

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dateYearDay(
    era: Era!, 
    yearOfEra: Int, 
    dayOfYear: Int
): ChronoLocalDate!
```

Obtains a local date in this chronology from the era, year-of-era and day-of-year fields.

| Parameters ||
|---|---|
| `era` | [Era](https://developer.android.com/reference/kotlin/java/time/chrono/Era)!: the era of the correct type for the chronology, not null |
| `yearOfEra` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the chronology year-of-era |
| `dayOfYear` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the chronology day-of-year |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate!` | the local date in this chronology, not null |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the `era` is not of the correct type for the chronology |
| `java.time.DateTimeException` | if unable to create the date |

### epochSecond

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun epochSecond(
    prolepticYear: Int, 
    month: Int, 
    dayOfMonth: Int, 
    hour: Int, 
    minute: Int, 
    second: Int, 
    zoneOffset: ZoneOffset!
): Long
```

Gets the number of seconds from the epoch of 1970-01-01T00:00:00Z.

The number of seconds is calculated using the proleptic-year, month, day-of-month, hour, minute, second, and zoneOffset.

| Parameters ||
|---|---|
| `prolepticYear` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the chronology proleptic-year |
| `month` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the chronology month-of-year |
| `dayOfMonth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the chronology day-of-month |
| `hour` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the hour-of-day, from 0 to 23 |
| `minute` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the minute-of-hour, from 0 to 59 |
| `second` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the second-of-minute, from 0 to 59 |
| `zoneOffset` | [ZoneOffset](https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#)!: the zone offset, not null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the number of seconds relative to 1970-01-01T00:00:00Z, may be negative |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if any of the values are out of range |

### epochSecond

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun epochSecond(
    era: Era!, 
    yearOfEra: Int, 
    month: Int, 
    dayOfMonth: Int, 
    hour: Int, 
    minute: Int, 
    second: Int, 
    zoneOffset: ZoneOffset!
): Long
```

Gets the number of seconds from the epoch of 1970-01-01T00:00:00Z.

The number of seconds is calculated using the era, year-of-era, month, day-of-month, hour, minute, second, and zoneOffset.

| Parameters ||
|---|---|
| `era` | [Era](https://developer.android.com/reference/kotlin/java/time/chrono/Era)!: the era of the correct type for the chronology, not null |
| `yearOfEra` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the chronology year-of-era |
| `month` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the chronology month-of-year |
| `dayOfMonth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the chronology day-of-month |
| `hour` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the hour-of-day, from 0 to 23 |
| `minute` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the minute-of-hour, from 0 to 59 |
| `second` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the second-of-minute, from 0 to 59 |
| `zoneOffset` | [ZoneOffset](https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#)!: the zone offset, not null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the number of seconds relative to 1970-01-01T00:00:00Z, may be negative |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if any of the values are out of range |

### eraOf

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun eraOf(eraValue: Int): Era!
```

Creates the chronology era object from the numeric value.

The era is, conceptually, the largest division of the time-line. Most calendar systems have a single epoch dividing the time-line into two eras. However, some have multiple eras, such as one for the reign of each leader. The exact meaning is determined by the chronology according to the following constraints.

The era in use at 1970-01-01 must have the value 1. Later eras must have sequentially higher values. Earlier eras must have sequentially lower values. Each chronology must refer to an enum or similar singleton to provide the era values.

This method returns the singleton era of the correct type for the specified era value.

| Parameters ||
|---|---|
| `eraValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the era value |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/chrono/Era!` | the calendar system era, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if unable to create the era |

### eras

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun eras(): MutableList<Era!>!
```

Gets the list of eras for the chronology.

Most calendar systems have an era, within which the year has meaning. If the calendar system does not support the concept of eras, an empty list must be returned.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/java/time/chrono/Era!>!` | the list of eras for the chronology, may be immutable, not null |

### from

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun from(temporal: TemporalAccessor!): Chronology!
```

Obtains an instance of `Chronology` from a temporal object.

This obtains a chronology based on the specified temporal. A `TemporalAccessor` represents an arbitrary set of date and time information, which this factory converts to an instance of `Chronology`.

The conversion will obtain the chronology using `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQueries.html#chronology()`. If the specified temporal object does not have a chronology, `https://developer.android.com/reference/kotlin/java/time/chrono/IsoChronology` is returned.

This method matches the signature of the functional interface `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery.html#` allowing it to be used as a query via method reference, `Chronology::from`.

| Parameters ||
|---|---|
| `temporal` | [TemporalAccessor](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor.html#)!: the temporal to convert, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#!` | the chronology, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if unable to convert to a `Chronology` |

### getAvailableChronologies

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getAvailableChronologies(): MutableSet<Chronology!>!
```

Returns the available chronologies.

Each returned `Chronology` is available for use in the system. The set of chronologies includes the system chronologies and any chronologies provided by the application via ServiceLoader configuration.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#!>!` | the independent, modifiable set of the available chronology IDs, not null |

### getCalendarType

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getCalendarType(): String!
```

Gets the calendar type of the calendar system.

The calendar type is an identifier defined by the CLDR and *Unicode Locale Data Markup Language (LDML)* specifications to uniquely identify a calendar. The `getCalendarType` is the concatenation of the CLDR calendar type and the variant, if applicable, is appended separated by "-". The calendar type is used to lookup the `Chronology` using `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#of(kotlin.String)`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the calendar system type, null if the calendar is not defined by CLDR/LDML |

**See Also**

- `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#getId()`

### getDisplayName

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDisplayName(
    style: TextStyle!, 
    locale: Locale!
): String!
```

Gets the textual representation of this chronology.

This returns the textual name used to identify the chronology, suitable for presentation to the user. The parameters control the style of the returned text and the locale.

| Parameters ||
|---|---|
| `style` | [TextStyle](https://developer.android.com/reference/kotlin/java/time/format/TextStyle.html#)!: the style of the text required, not null |
| `locale` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!: the locale to use, not null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the text value of the chronology, not null |

### getId

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getId(): String!
```

Gets the ID of the chronology.

The ID uniquely identifies the `Chronology`. It can be used to lookup the `Chronology` using `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#of(kotlin.String)`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the chronology ID, not null |

**See Also**

- `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#getCalendarType()`

### isIsoBased

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isIsoBased(): Boolean
```

Checks if this chronology is ISO based.

An ISO based chronology has the same basic structure as the `https://developer.android.com/reference/kotlin/java/time/chrono/IsoChronology`, i.e., the chronology has the same number of months, the number of days in each month, and day-of-year and leap years are the same as ISO chronology. It also supports the concept of week-based-year of ISO chronology. For example, the `https://developer.android.com/reference/kotlin/java/time/chrono/MinguoChronology`, `https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistChronology` and `https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseChronology` chronologies are ISO based.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` only if all the fields of `https://developer.android.com/reference/kotlin/java/time/temporal/IsoFields.html#` are supported by this chronology. Otherwise, returns `false`. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/time/chrono/IsoChronology`
- `https://developer.android.com/reference/kotlin/java/time/chrono/JapaneseChronology`
- `https://developer.android.com/reference/kotlin/java/time/chrono/MinguoChronology`
- `https://developer.android.com/reference/kotlin/java/time/chrono/ThaiBuddhistChronology`
- `https://developer.android.com/reference/kotlin/java/time/temporal/IsoFields.html#`

### isLeapYear

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun isLeapYear(prolepticYear: Long): Boolean
```

Checks if the specified year is a leap year.

A leap-year is a year of a longer length than normal. The exact meaning is determined by the chronology according to the following constraints.

- a leap-year must imply a year-length longer than a non leap-year.
- a chronology that does not support the concept of a year must return false.
- the correct result must be returned for all years within the valid range of years for the chronology.

Outside the range of valid years an implementation is free to return either a best guess or false. An implementation must not throw an exception, even if the year is outside the range of valid years.

| Parameters ||
|---|---|
| `prolepticYear` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the proleptic-year to check, not validated for range |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the year is a leap year |

### localDateTime

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun localDateTime(temporal: TemporalAccessor!): ChronoLocalDateTime<out ChronoLocalDate!>!
```

Obtains a local date-time in this chronology from another temporal object.

This obtains a date-time in this chronology based on the specified temporal. A `TemporalAccessor` represents an arbitrary set of date and time information, which this factory converts to an instance of `ChronoLocalDateTime`.

The conversion extracts and combines the `ChronoLocalDate` and the `LocalTime` from the temporal object. Implementations are permitted to perform optimizations such as accessing those fields that are equivalent to the relevant objects. The result uses this chronology.

This method matches the signature of the functional interface `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery.html#` allowing it to be used as a query via method reference, `aChronology::localDateTime`.

| Parameters ||
|---|---|
| `temporal` | [TemporalAccessor](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor.html#)!: the temporal object to convert, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime<out https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate!>!` | the local date-time in this chronology, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if unable to create the date-time |

**See Also**

- `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDateTime#from(java.time.temporal.TemporalAccessor)`

### of

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun of(id: String!): Chronology!
```

Obtains an instance of `Chronology` from a chronology ID or calendar system type.

This returns a chronology based on either the ID or the type. The `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#getId()` uniquely identifies the chronology. The `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#getCalendarType()` is defined by the CLDR specification.

The chronology may be a system chronology or a chronology provided by the application via ServiceLoader configuration.

Since some calendars can be customized, the ID or type typically refers to the default customization. For example, the Gregorian calendar can have multiple cutover dates from the Julian, but the lookup only provides the default cutover date.

| Parameters ||
|---|---|
| `id` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the chronology ID or calendar system type, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#!` | the chronology with the identifier requested, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the chronology cannot be found |

### ofLocale

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun ofLocale(locale: Locale!): Chronology!
```

Obtains an instance of `Chronology` from a locale.

This returns a `Chronology` based on the specified locale, typically returning `IsoChronology`. Other calendar systems are only returned if they are explicitly selected within the locale.

The `https://developer.android.com/reference/kotlin/java/util/Locale.html#` class provide access to a range of information useful for localizing an application. This includes the language and region, such as "en-GB" for English as used in Great Britain.

The `Locale` class also supports an extension mechanism that can be used to identify a calendar system. The mechanism is a form of key-value pairs, where the calendar system has the key "ca". For example, the locale "en-JP-u-ca-japanese" represents the English language as used in Japan with the Japanese calendar system.

This method finds the desired calendar system in a manner equivalent to passing "ca" to `https://developer.android.com/reference/kotlin/java/util/Locale.html#getUnicodeLocaleType(kotlin.String)`. If the "ca" key is not present, then `IsoChronology` is returned.

Note that the behavior of this method differs from the older `https://developer.android.com/reference/kotlin/java/util/Calendar.html#getInstance(java.util.Locale)` method. If that method receives a locale of "th_TH" it will return `BuddhistCalendar`. By contrast, this method will return `IsoChronology`. Passing the locale "th-TH-u-ca-buddhist" into either method will result in the Thai Buddhist calendar system and is therefore the recommended approach going forward for Thai calendar system localization.

A similar, but simpler, situation occurs for the Japanese calendar system. The locale "jp_JP_JP" has previously been used to access the calendar. However, unlike the Thai locale, "ja_JP_JP" is automatically converted by `Locale` to the modern and recommended form of "ja-JP-u-ca-japanese". Thus, there is no difference in behavior between this method and `Calendar#getInstance(Locale)`.

| Parameters ||
|---|---|
| `locale` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!: the locale to use to obtain the calendar system, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology#!` | the calendar system associated with the locale, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the locale-specified calendar cannot be found |

### period

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun period(
    years: Int, 
    months: Int, 
    days: Int
): ChronoPeriod!
```

Obtains a period for this chronology based on years, months and days.

This returns a period tied to this chronology using the specified years, months and days. All supplied chronologies use periods based on years, months and days, however the `ChronoPeriod` API allows the period to be represented using other units.

| Parameters ||
|---|---|
| `years` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the number of years, may be negative |
| `months` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the number of years, may be negative |
| `days` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the number of years, may be negative |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoPeriod!` | the period in terms of this chronology, not null |

### prolepticYear

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun prolepticYear(
    era: Era!, 
    yearOfEra: Int
): Int
```

Calculates the proleptic-year given the era and year-of-era.

This combines the era and year-of-era into the single proleptic-year field.

If the chronology makes active use of eras, such as `JapaneseChronology` then the year-of-era will be validated against the era. For other chronologies, validation is optional.

| Parameters ||
|---|---|
| `era` | [Era](https://developer.android.com/reference/kotlin/java/time/chrono/Era)!: the era of the correct type for the chronology, not null |
| `yearOfEra` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the chronology year-of-era |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the proleptic-year |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the `era` is not of the correct type for the chronology |
| `java.time.DateTimeException` | if unable to convert to a proleptic-year, such as if the year is invalid for the era |

### range

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun range(field: ChronoField!): ValueRange!
```

Gets the range of valid values for the specified field.

All fields can be expressed as a `long` integer. This method returns an object that describes the valid range for that value.

Note that the result only describes the minimum and maximum valid values and it is important not to read too much into them. For example, there could be values within the range that are invalid for the field.

This method will return a result whether or not the chronology supports the field.

| Parameters ||
|---|---|
| `field` | [ChronoField](https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField.html#)!: the field to get the range for, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/temporal/ValueRange.html#!` | the range of valid values for the field, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the range for the field cannot be obtained |

### resolveDate

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun resolveDate(
    fieldValues: MutableMap<TemporalField!, Long!>!, 
    resolverStyle: ResolverStyle!
): ChronoLocalDate!
```

Resolves parsed `ChronoField` values into a date during parsing.

Most `TemporalField` implementations are resolved using the resolve method on the field. By contrast, the `ChronoField` class defines fields that only have meaning relative to the chronology. As such, `ChronoField` date fields are resolved here in the context of a specific chronology.

The default implementation, which explains typical resolve behaviour, is provided in `https://developer.android.com/reference/kotlin/java/time/chrono/AbstractChronology`.

| Parameters ||
|---|---|
| `fieldValues` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField.html#)!, [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)!\>!: the map of fields to values, which can be updated, not null |
| `resolverStyle` | [ResolverStyle](https://developer.android.com/reference/kotlin/java/time/format/ResolverStyle.html#)!: the requested type of resolve, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate!` | the resolved date, null if insufficient information to create a date |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the date cannot be resolved, typically because of a conflict in the input data |

### zonedDateTime

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun zonedDateTime(
    instant: Instant!, 
    zone: ZoneId!
): ChronoZonedDateTime<out ChronoLocalDate!>!
```

Obtains a `ChronoZonedDateTime` in this chronology from an `Instant`.

This obtains a zoned date-time with the same instant as that specified.

| Parameters ||
|---|---|
| `instant` | [Instant](https://developer.android.com/reference/kotlin/java/time/Instant.html#)!: the instant to create the date-time from, not null |
| `zone` | [ZoneId](https://developer.android.com/reference/kotlin/java/time/ZoneId.html#)!: the time-zone, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime<out https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate!>!` | the zoned date-time, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the result exceeds the supported range |

### zonedDateTime

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun zonedDateTime(temporal: TemporalAccessor!): ChronoZonedDateTime<out ChronoLocalDate!>!
```

Obtains a `ChronoZonedDateTime` in this chronology from another temporal object.

This obtains a zoned date-time in this chronology based on the specified temporal. A `TemporalAccessor` represents an arbitrary set of date and time information, which this factory converts to an instance of `ChronoZonedDateTime`.

The conversion will first obtain a `ZoneId` from the temporal object, falling back to a `ZoneOffset` if necessary. It will then try to obtain an `Instant`, falling back to a `ChronoLocalDateTime` if necessary. The result will be either the combination of `ZoneId` or `ZoneOffset` with `Instant` or `ChronoLocalDateTime`. Implementations are permitted to perform optimizations such as accessing those fields that are equivalent to the relevant objects. The result uses this chronology.

This method matches the signature of the functional interface `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery.html#` allowing it to be used as a query via method reference, `aChronology::zonedDateTime`.

| Parameters ||
|---|---|
| `temporal` | [TemporalAccessor](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor.html#)!: the temporal object to convert, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime<out https://developer.android.com/reference/kotlin/java/time/chrono/ChronoLocalDate!>!` | the zoned date-time in this chronology, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if unable to create the date-time |

**See Also**

- `https://developer.android.com/reference/kotlin/java/time/chrono/ChronoZonedDateTime#from(java.time.temporal.TemporalAccessor)`
