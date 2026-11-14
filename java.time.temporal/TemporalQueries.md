Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TemporalQueries

```
class TemporalQueries
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.time.temporal.TemporalQueries](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQueries#) |

Common implementations of `TemporalQuery`.

This class provides common implementations of `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery`. These are defined here as they must be constants, and the definition of lambdas does not guarantee that. By assigning them once here, they become 'normal' Java constants.

Queries are a key tool for extracting information from temporal objects. They exist to externalize the process of querying, permitting different approaches, as per the strategy design pattern. Examples might be a query that checks if the date is the day before February 29th in a leap year, or calculates the number of days to your next birthday.

The `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField` interface provides another mechanism for querying temporal objects. That interface is limited to returning a `long`. By contrast, queries can return any type.

There are two equivalent ways of using a `TemporalQuery`. The first is to invoke the method on this interface directly. The second is to use `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor#query(java.time.temporal.TemporalQuery)`:

```kotlin
// these two lines are equivalent, but the second approach is recommended
    temporal = thisQuery.queryFrom(temporal);
    temporal = temporal.query(thisQuery);
  
```
It is recommended to use the second approach, `query(TemporalQuery)`, as it is a lot clearer to read in code.

The most common implementations are method references, such as `LocalDate::from` and `ZoneId::from`. Additional common queries are provided to return:

- a Chronology,
- a LocalDate,
- a LocalTime,
- a ZoneOffset,
- a precision,
- a zone, or
- a zoneId.

## Summary

| Public methods ||
|---|---|
| static [TemporalQuery](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery)\< [Chronology](https://developer.android.com/reference/kotlin/java/time/chrono/Chronology.html#)!\>! | `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQueries#chronology()()` A query for the `Chronology`. |
| static [TemporalQuery](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery)\< [LocalDate](https://developer.android.com/reference/kotlin/java/time/LocalDate.html#)!\>! | `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQueries#localDate()()` A query for `LocalDate` returning null if not found. |
| static [TemporalQuery](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery)\< [LocalTime](https://developer.android.com/reference/kotlin/java/time/LocalTime.html#)!\>! | `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQueries#localTime()()` A query for `LocalTime` returning null if not found. |
| static [TemporalQuery](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery)\< [ZoneOffset](https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#)!\>! | `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQueries#offset()()` A query for `ZoneOffset` returning null if not found. |
| static [TemporalQuery](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery)\< [TemporalUnit](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit)!\>! | `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQueries#precision()()` A query for the smallest supported unit. |
| static [TemporalQuery](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery)\< [ZoneId](https://developer.android.com/reference/kotlin/java/time/ZoneId.html#)!\>! | `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQueries#zone()()` A lenient query for the `ZoneId`, falling back to the `ZoneOffset`. |
| static [TemporalQuery](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery)\< [ZoneId](https://developer.android.com/reference/kotlin/java/time/ZoneId.html#)!\>! | `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQueries#zoneId()()` A strict query for the `ZoneId`. |

## Public methods

### chronology

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun chronology(): TemporalQuery<Chronology!>!
```

A query for the `Chronology`.

This queries a `TemporalAccessor` for the chronology. If the target `TemporalAccessor` represents a date, or part of a date, then it should return the chronology that the date is expressed in. As a result of this definition, objects only representing time, such as `LocalTime`, will return null.

The result from JDK classes implementing `TemporalAccessor` is as follows: 
`LocalDate` returns `IsoChronology.INSTANCE` 
`LocalTime` returns null (does not represent a date) 
`LocalDateTime` returns `IsoChronology.INSTANCE` 
`ZonedDateTime` returns `IsoChronology.INSTANCE` 
`OffsetTime` returns null (does not represent a date) 
`OffsetDateTime` returns `IsoChronology.INSTANCE` 
`ChronoLocalDate` returns the associated chronology 
`ChronoLocalDateTime` returns the associated chronology 
`ChronoZonedDateTime` returns the associated chronology 
`Era` returns the associated chronology 
`DayOfWeek` returns null (shared across chronologies) 
`Month` returns `IsoChronology.INSTANCE` 
`Year` returns `IsoChronology.INSTANCE` 
`YearMonth` returns `IsoChronology.INSTANCE` 
`MonthDay` returns null `IsoChronology.INSTANCE` 
`ZoneOffset` returns null (does not represent a date) 
`Instant` returns null (does not represent a date) 

The method `https://developer.android.com/reference/kotlin/java/time/chrono/Chronology.html#from(java.time.temporal.TemporalAccessor)` can be used as a `TemporalQuery` via a method reference, `Chronology::from`. That method is equivalent to this query, except that it throws an exception if a chronology cannot be obtained.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery<https://developer.android.com/reference/kotlin/java/time/chrono/Chronology.html#!>!` | a query that can obtain the chronology of a temporal, not null |

### localDate

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun localDate(): TemporalQuery<LocalDate!>!
```

A query for `LocalDate` returning null if not found.

This returns a `TemporalQuery` that can be used to query a temporal object for the local date. The query will return null if the temporal object cannot supply a local date.

The query implementation examines the `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField` field and uses it to create a `LocalDate`.

The method java.time.LocalDate#from(java.time.temporal.TemporalAccessor) can be used as a `TemporalQuery` via a method reference, `LocalDate::from`. This query and `LocalDate::from` will return the same result if the temporal object contains a date. If the temporal object does not contain a date, then the method reference will throw an exception, whereas this query will return null.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery<https://developer.android.com/reference/kotlin/java/time/LocalDate.html#!>!` | a query that can obtain the date of a temporal, not null |

### localTime

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun localTime(): TemporalQuery<LocalTime!>!
```

A query for `LocalTime` returning null if not found.

This returns a `TemporalQuery` that can be used to query a temporal object for the local time. The query will return null if the temporal object cannot supply a local time.

The query implementation examines the `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField` field and uses it to create a `LocalTime`.

The method `https://developer.android.com/reference/kotlin/java/time/LocalTime.html#from(java.time.temporal.TemporalAccessor)` can be used as a `TemporalQuery` via a method reference, `LocalTime::from`. This query and `LocalTime::from` will return the same result if the temporal object contains a time. If the temporal object does not contain a time, then the method reference will throw an exception, whereas this query will return null.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery<https://developer.android.com/reference/kotlin/java/time/LocalTime.html#!>!` | a query that can obtain the time of a temporal, not null |

### offset

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun offset(): TemporalQuery<ZoneOffset!>!
```

A query for `ZoneOffset` returning null if not found.

This returns a `TemporalQuery` that can be used to query a temporal object for the offset. The query will return null if the temporal object cannot supply an offset.

The query implementation examines the `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField` field and uses it to create a `ZoneOffset`.

The method `https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#from(java.time.temporal.TemporalAccessor)` can be used as a `TemporalQuery` via a method reference, `ZoneOffset::from`. This query and `ZoneOffset::from` will return the same result if the temporal object contains an offset. If the temporal object does not contain an offset, then the method reference will throw an exception, whereas this query will return null.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery<https://developer.android.com/reference/kotlin/java/time/ZoneOffset.html#!>!` | a query that can obtain the offset of a temporal, not null |

### precision

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun precision(): TemporalQuery<TemporalUnit!>!
```

A query for the smallest supported unit.

This queries a `TemporalAccessor` for the time precision. If the target `TemporalAccessor` represents a consistent or complete date-time, date or time then this must return the smallest precision actually supported. Note that fields such as `NANO_OF_DAY` and `NANO_OF_SECOND` are defined to always return ignoring the precision, thus this is the only way to find the actual smallest supported unit. For example, were `GregorianCalendar` to implement `TemporalAccessor` it would return a precision of `MILLIS`.

The result from JDK classes implementing `TemporalAccessor` is as follows: 
`LocalDate` returns `DAYS` 
`LocalTime` returns `NANOS` 
`LocalDateTime` returns `NANOS` 
`ZonedDateTime` returns `NANOS` 
`OffsetTime` returns `NANOS` 
`OffsetDateTime` returns `NANOS` 
`ChronoLocalDate` returns `DAYS` 
`ChronoLocalDateTime` returns `NANOS` 
`ChronoZonedDateTime` returns `NANOS` 
`Era` returns `ERAS` 
`DayOfWeek` returns `DAYS` 
`Month` returns `MONTHS` 
`Year` returns `YEARS` 
`YearMonth` returns `MONTHS` 
`MonthDay` returns null (does not represent a complete date or time) 
`ZoneOffset` returns null (does not represent a date or time) 
`Instant` returns `NANOS` 

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery<https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit!>!` | a query that can obtain the precision of a temporal, not null |

### zone

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun zone(): TemporalQuery<ZoneId!>!
```

A lenient query for the `ZoneId`, falling back to the `ZoneOffset`.

This queries a `TemporalAccessor` for the zone. It first tries to obtain the zone, using `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQueries#zoneId()`. If that is not found it tries to obtain the `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQueries#offset()`. Thus a `https://developer.android.com/reference/kotlin/java/time/ZonedDateTime.html#` will return the result of `getZone()`, while an `https://developer.android.com/reference/kotlin/java/time/OffsetDateTime.html#` will return the result of `getOffset()`.

In most cases, applications should use this query rather than `zoneId()`.

The method `https://developer.android.com/reference/kotlin/java/time/ZoneId.html#from(java.time.temporal.TemporalAccessor)` can be used as a `TemporalQuery` via a method reference, `ZoneId::from`. That method is equivalent to this query, except that it throws an exception if a zone cannot be obtained.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery<https://developer.android.com/reference/kotlin/java/time/ZoneId.html#!>!` | a query that can obtain the zone ID or offset of a temporal, not null |

### zoneId

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun zoneId(): TemporalQuery<ZoneId!>!
```

A strict query for the `ZoneId`.

This queries a `TemporalAccessor` for the zone. The zone is only returned if the date-time conceptually contains a `ZoneId`. It will not be returned if the date-time only conceptually has an `ZoneOffset`. Thus a `https://developer.android.com/reference/kotlin/java/time/ZonedDateTime.html#` will return the result of `getZone()`, but an `https://developer.android.com/reference/kotlin/java/time/OffsetDateTime.html#` will return null.

In most cases, applications should use `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQueries#zone()` as this query is too strict.

The result from JDK classes implementing `TemporalAccessor` is as follows: 
`LocalDate` returns null 
`LocalTime` returns null 
`LocalDateTime` returns null 
`ZonedDateTime` returns the associated zone 
`OffsetTime` returns null 
`OffsetDateTime` returns null 
`ChronoLocalDate` returns null 
`ChronoLocalDateTime` returns null 
`ChronoZonedDateTime` returns the associated zone 
`Era` returns null 
`DayOfWeek` returns null 
`Month` returns null 
`Year` returns null 
`YearMonth` returns null 
`MonthDay` returns null 
`ZoneOffset` returns null 
`Instant` returns null 

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery<https://developer.android.com/reference/kotlin/java/time/ZoneId.html#!>!` | a query that can obtain the zone ID of a temporal, not null |
