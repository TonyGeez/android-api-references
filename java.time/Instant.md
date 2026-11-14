Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Instant

```
class Instant : Comparable<Instant!>, Serializable, Temporal, TemporalAdjuster
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.time.Instant](https://developer.android.com/reference/kotlin/java/time/Instant#) |

An instantaneous point on the time-line.

This class models a single instantaneous point on the time-line. This might be used to record event time-stamps in the application.

The range of an instant requires the storage of a number larger than a `long`. To achieve this, the class stores a `long` representing epoch-seconds and an `int` representing nanosecond-of-second, which will always be between 0 and 999,999,999. The epoch-seconds are measured from the standard Java epoch of `1970-01-01T00:00:00Z` where instants after the epoch have positive values, and earlier instants have negative values. For both the epoch-second and nanosecond parts, a larger value is always later on the time-line than a smaller value.

## Time-scale

The length of the solar day is the standard way that humans measure time. This has traditionally been subdivided into 24 hours of 60 minutes of 60 seconds, forming a 86400 second day.

Modern timekeeping is based on atomic clocks which precisely define an SI second relative to the transitions of a Caesium atom. The length of an SI second was defined to be very close to the 86400th fraction of a day.

Unfortunately, as the Earth rotates the length of the day varies. In addition, over time the average length of the day is getting longer as the Earth slows. As a result, the length of a solar day in 2012 is slightly longer than 86400 SI seconds. The actual length of any given day and the amount by which the Earth is slowing are not predictable and can only be determined by measurement. The UT1 time-scale captures the accurate length of day, but is only available some time after the day has completed.

The UTC time-scale is a standard approach to bundle up all the additional fractions of a second from UT1 into whole seconds, known as *leap-seconds*. A leap-second may be added or removed depending on the Earth's rotational changes. As such, UTC permits a day to have 86399 SI seconds or 86401 SI seconds where necessary in order to keep the day aligned with the Sun.

The modern UTC time-scale was introduced in 1972, introducing the concept of whole leap-seconds. Between 1958 and 1972, the definition of UTC was complex, with minor sub-second leaps and alterations to the length of the notional second. As of 2012, discussions are underway to change the definition of UTC again, with the potential to remove leap seconds or introduce other changes.

Given the complexity of accurate timekeeping described above, this Java API defines its own time-scale, the *Java Time-Scale*.

The Java Time-Scale divides each calendar day into exactly 86400 subdivisions, known as seconds. These seconds may differ from the SI second. It closely matches the de facto international civil time scale, the definition of which changes from time to time.

The Java Time-Scale has slightly different definitions for different segments of the time-line, each based on the consensus international time scale that is used as the basis for civil time. Whenever the internationally-agreed time scale is modified or replaced, a new segment of the Java Time-Scale must be defined for it. Each segment must meet these requirements:

- the Java Time-Scale shall closely match the underlying international civil time scale;
- the Java Time-Scale shall exactly match the international civil time scale at noon each day;
- the Java Time-Scale shall have a precisely-defined relationship to the international civil time scale.

There are currently, as of 2013, two segments in the Java time-scale.

For the segment from 1972-11-03 (exact boundary discussed below) until further notice, the consensus international time scale is UTC (with leap seconds). In this segment, the Java Time-Scale is identical to [UTC-SLS](http://www.cl.cam.ac.uk/~mgk25/time/utc-sls/). This is identical to UTC on days that do not have a leap second. On days that do have a leap second, the leap second is spread equally over the last 1000 seconds of the day, maintaining the appearance of exactly 86400 seconds per day.

For the segment prior to 1972-11-03, extending back arbitrarily far, the consensus international time scale is defined to be UT1, applied proleptically, which is equivalent to the (mean) solar time on the prime meridian (Greenwich). In this segment, the Java Time-Scale is identical to the consensus international time scale. The exact boundary between the two segments is the instant where UT1 = UTC between 1972-11-03T00:00 and 1972-11-04T12:00.

Implementations of the Java time-scale using the JSR-310 API are not required to provide any clock that is sub-second accurate, or that progresses monotonically or smoothly. Implementations are therefore not required to actually perform the UTC-SLS slew or to otherwise be aware of leap seconds. JSR-310 does, however, require that implementations must document the approach they use when defining a clock representing the current instant. See `https://developer.android.com/reference/kotlin/java/time/Clock` for details on the available clocks.

The Java time-scale is used for all date-time classes. This includes `Instant`, `LocalDate`, `LocalTime`, `OffsetDateTime`, `ZonedDateTime` and `Duration`.

This is a [value-based](https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/lang/doc-files/ValueBased.html) class; programmers should treat instances that are [equal](https://developer.android.com/reference/kotlin/java/time/Instant#equals(kotlin.Any)) as interchangeable and should not use instances for synchronization, or unpredictable behavior may occur. For example, in a future release, synchronization may fail. The `equals` method should be used for comparisons.

## Summary

| Public methods ||
|---|---|
| [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal)! | `https://developer.android.com/reference/kotlin/java/time/Instant#adjustInto(java.time.temporal.Temporal)(temporal: https://developer.android.com/reference/kotlin/java/time/temporal/Temporal!)` Adjusts the specified temporal object to have this instant. |
| [OffsetDateTime](https://developer.android.com/reference/kotlin/java/time/OffsetDateTime)! | `https://developer.android.com/reference/kotlin/java/time/Instant#atOffset(java.time.ZoneOffset)(offset: https://developer.android.com/reference/kotlin/java/time/ZoneOffset!)` Combines this instant with an offset to create an `OffsetDateTime`. |
| [ZonedDateTime](https://developer.android.com/reference/kotlin/java/time/ZonedDateTime)! | `https://developer.android.com/reference/kotlin/java/time/Instant#atZone(java.time.ZoneId)(zone: https://developer.android.com/reference/kotlin/java/time/ZoneId!)` Combines this instant with a time-zone to create a `ZonedDateTime`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/time/Instant#compareTo(java.time.Instant)(other: https://developer.android.com/reference/kotlin/java/time/Instant#!)` Compares this instant to the specified instant. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/time/Instant#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Checks if this instant is equal to the specified instant. |
| static [Instant](https://developer.android.com/reference/kotlin/java/time/Instant#)! | `https://developer.android.com/reference/kotlin/java/time/Instant#from(java.time.temporal.TemporalAccessor)(temporal: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor!)` Obtains an instance of `Instant` from a temporal object. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/time/Instant#get(java.time.temporal.TemporalField)(field: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField!)` Gets the value of the specified field from this instant as an `int`. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/time/Instant#getEpochSecond()()` Gets the number of seconds from the Java epoch of 1970-01-01T00:00:00Z. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/time/Instant#getLong(java.time.temporal.TemporalField)(field: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField!)` Gets the value of the specified field from this instant as a `long`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/time/Instant#getNano()()` Gets the number of nanoseconds, later along the time-line, from the start of the second. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/time/Instant#hashCode()()` Returns a hash code for this instant. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/time/Instant#isAfter(java.time.Instant)(otherInstant: https://developer.android.com/reference/kotlin/java/time/Instant#!)` Checks if this instant is after the specified instant. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/time/Instant#isBefore(java.time.Instant)(otherInstant: https://developer.android.com/reference/kotlin/java/time/Instant#!)` Checks if this instant is before the specified instant. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/time/Instant#isSupported(java.time.temporal.TemporalField)(field: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField!)` Checks if the specified field is supported. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/time/Instant#isSupported(java.time.temporal.TemporalUnit)(unit: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit!)` Checks if the specified unit is supported. |
| [Instant](https://developer.android.com/reference/kotlin/java/time/Instant#)! | `https://developer.android.com/reference/kotlin/java/time/Instant#minus(java.time.temporal.TemporalAmount)(amountToSubtract: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount!)` Returns a copy of this instant with the specified amount subtracted. |
| [Instant](https://developer.android.com/reference/kotlin/java/time/Instant#)! | `https://developer.android.com/reference/kotlin/java/time/Instant#minus(kotlin.Long,%20java.time.temporal.TemporalUnit)(amountToSubtract: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, unit: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit!)` Returns a copy of this instant with the specified amount subtracted. |
| [Instant](https://developer.android.com/reference/kotlin/java/time/Instant#)! | `https://developer.android.com/reference/kotlin/java/time/Instant#minusMillis(kotlin.Long)(millisToSubtract: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns a copy of this instant with the specified duration in milliseconds subtracted. |
| [Instant](https://developer.android.com/reference/kotlin/java/time/Instant#)! | `https://developer.android.com/reference/kotlin/java/time/Instant#minusNanos(kotlin.Long)(nanosToSubtract: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns a copy of this instant with the specified duration in nanoseconds subtracted. |
| [Instant](https://developer.android.com/reference/kotlin/java/time/Instant#)! | `https://developer.android.com/reference/kotlin/java/time/Instant#minusSeconds(kotlin.Long)(secondsToSubtract: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns a copy of this instant with the specified duration in seconds subtracted. |
| static [Instant](https://developer.android.com/reference/kotlin/java/time/Instant#)! | `https://developer.android.com/reference/kotlin/java/time/Instant#now()()` Obtains the current instant from the system clock. |
| static [Instant](https://developer.android.com/reference/kotlin/java/time/Instant#)! | `https://developer.android.com/reference/kotlin/java/time/Instant#now(java.time.Clock)(clock: https://developer.android.com/reference/kotlin/java/time/Clock!)` Obtains the current instant from the specified clock. |
| static [Instant](https://developer.android.com/reference/kotlin/java/time/Instant#)! | `https://developer.android.com/reference/kotlin/java/time/Instant#ofEpochMilli(kotlin.Long)(epochMilli: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Obtains an instance of `Instant` using milliseconds from the epoch of 1970-01-01T00:00:00Z. |
| static [Instant](https://developer.android.com/reference/kotlin/java/time/Instant#)! | `https://developer.android.com/reference/kotlin/java/time/Instant#ofEpochSecond(kotlin.Long)(epochSecond: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Obtains an instance of `Instant` using seconds from the epoch of 1970-01-01T00:00:00Z. |
| static [Instant](https://developer.android.com/reference/kotlin/java/time/Instant#)! | `https://developer.android.com/reference/kotlin/java/time/Instant#ofEpochSecond(kotlin.Long,%20kotlin.Long)(epochSecond: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, nanoAdjustment: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Obtains an instance of `Instant` using seconds from the epoch of 1970-01-01T00:00:00Z and nanosecond fraction of second. |
| static [Instant](https://developer.android.com/reference/kotlin/java/time/Instant#)! | `https://developer.android.com/reference/kotlin/java/time/Instant#parse(kotlin.CharSequence)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!)` Obtains an instance of `Instant` from a text string such as `2007-12-03T10:15:30.00Z`. |
| [Instant](https://developer.android.com/reference/kotlin/java/time/Instant#)! | `https://developer.android.com/reference/kotlin/java/time/Instant#plus(java.time.temporal.TemporalAmount)(amountToAdd: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount!)` Returns a copy of this instant with the specified amount added. |
| [Instant](https://developer.android.com/reference/kotlin/java/time/Instant#)! | `https://developer.android.com/reference/kotlin/java/time/Instant#plus(kotlin.Long,%20java.time.temporal.TemporalUnit)(amountToAdd: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, unit: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit!)` Returns a copy of this instant with the specified amount added. |
| [Instant](https://developer.android.com/reference/kotlin/java/time/Instant#)! | `https://developer.android.com/reference/kotlin/java/time/Instant#plusMillis(kotlin.Long)(millisToAdd: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns a copy of this instant with the specified duration in milliseconds added. |
| [Instant](https://developer.android.com/reference/kotlin/java/time/Instant#)! | `https://developer.android.com/reference/kotlin/java/time/Instant#plusNanos(kotlin.Long)(nanosToAdd: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns a copy of this instant with the specified duration in nanoseconds added. |
| [Instant](https://developer.android.com/reference/kotlin/java/time/Instant#)! | `https://developer.android.com/reference/kotlin/java/time/Instant#plusSeconds(kotlin.Long)(secondsToAdd: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns a copy of this instant with the specified duration in seconds added. |
| R | `https://developer.android.com/reference/kotlin/java/time/Instant#query(java.time.temporal.TemporalQuery)(query: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery<R>!)` Queries this instant using the specified query. |
| [ValueRange](https://developer.android.com/reference/kotlin/java/time/temporal/ValueRange)! | `https://developer.android.com/reference/kotlin/java/time/Instant#range(java.time.temporal.TemporalField)(field: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField!)` Gets the range of valid values for the specified field. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/time/Instant#toEpochMilli()()` Converts this instant to the number of milliseconds from the epoch of 1970-01-01T00:00:00Z. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/time/Instant#toString()()` A string representation of this instant using ISO-8601 representation. |
| [Instant](https://developer.android.com/reference/kotlin/java/time/Instant#)! | `https://developer.android.com/reference/kotlin/java/time/Instant#truncatedTo(java.time.temporal.TemporalUnit)(unit: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit!)` Returns a copy of this `Instant` truncated to the specified unit. |
| [Duration](https://developer.android.com/reference/kotlin/java/time/Duration) | `https://developer.android.com/reference/kotlin/java/time/Instant#until(java.time.Instant)(endExclusive: https://developer.android.com/reference/kotlin/java/time/Instant#)` Calculates the `Duration` until another `Instant`. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/time/Instant#until(java.time.temporal.Temporal,%20java.time.temporal.TemporalUnit)(endExclusive: https://developer.android.com/reference/kotlin/java/time/temporal/Temporal!, unit: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit!)` Calculates the amount of time until another instant in terms of the specified unit. |
| [Instant](https://developer.android.com/reference/kotlin/java/time/Instant#)! | `https://developer.android.com/reference/kotlin/java/time/Instant#with(java.time.temporal.TemporalAdjuster)(adjuster: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAdjuster!)` Returns an adjusted copy of this instant. |
| [Instant](https://developer.android.com/reference/kotlin/java/time/Instant#)! | `https://developer.android.com/reference/kotlin/java/time/Instant#with(java.time.temporal.TemporalField,%20kotlin.Long)(field: https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField!, newValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns a copy of this instant with the specified field set to a new value. |

| Properties ||
|---|---|
| static [Instant](https://developer.android.com/reference/kotlin/java/time/Instant#)! | `https://developer.android.com/reference/kotlin/java/time/Instant#EPOCH:java.time.Instant` Constant for the 1970-01-01T00:00:00Z epoch instant. |
| static [Instant](https://developer.android.com/reference/kotlin/java/time/Instant#)! | `https://developer.android.com/reference/kotlin/java/time/Instant#MAX:java.time.Instant` The maximum supported `Instant`, '1000000000-12-31T23:59:59. |
| static [Instant](https://developer.android.com/reference/kotlin/java/time/Instant#)! | `https://developer.android.com/reference/kotlin/java/time/Instant#MIN:java.time.Instant` The minimum supported `Instant`, '-1000000000-01-01T00:00Z'. |

## Public methods

### adjustInto

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun adjustInto(temporal: Temporal!): Temporal!
```

Adjusts the specified temporal object to have this instant.

This returns a temporal object of the same observable type as the input with the instant changed to be the same as this.

The adjustment is equivalent to using `https://developer.android.com/reference/kotlin/java/time/temporal/Temporal#with(java.time.temporal.TemporalField,%20kotlin.Long)` twice, passing `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField` and `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField` as the fields.

In most cases, it is clearer to reverse the calling pattern by using `https://developer.android.com/reference/kotlin/java/time/temporal/Temporal#with(java.time.temporal.TemporalAdjuster)`:

```kotlin
// these two lines are equivalent, but the second approach is recommended
    temporal = thisInstant.adjustInto(temporal);
    temporal = temporal.with(thisInstant);
  
```

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `temporal` | [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal)!: the target object to be adjusted, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/temporal/Temporal!` | the adjusted object, not null |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if unable to make the adjustment |

### atOffset

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun atOffset(offset: ZoneOffset!): OffsetDateTime!
```

Combines this instant with an offset to create an `OffsetDateTime`.

This returns an `OffsetDateTime` formed from this instant at the specified offset from UTC/Greenwich. An exception will be thrown if the instant is too large to fit into an offset date-time.

This method is equivalent to `https://developer.android.com/reference/kotlin/java/time/OffsetDateTime#ofInstant(java.time.Instant,%20java.time.ZoneId)`.

| Parameters ||
|---|---|
| `offset` | [ZoneOffset](https://developer.android.com/reference/kotlin/java/time/ZoneOffset)!: the offset to combine with, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/OffsetDateTime!` | the offset date-time formed from this instant and the specified offset, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the result exceeds the supported range |

### atZone

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun atZone(zone: ZoneId!): ZonedDateTime!
```

Combines this instant with a time-zone to create a `ZonedDateTime`.

This returns an `ZonedDateTime` formed from this instant at the specified time-zone. An exception will be thrown if the instant is too large to fit into a zoned date-time.

This method is equivalent to `https://developer.android.com/reference/kotlin/java/time/ZonedDateTime#ofInstant(java.time.Instant,%20java.time.ZoneId)`.

| Parameters ||
|---|---|
| `zone` | [ZoneId](https://developer.android.com/reference/kotlin/java/time/ZoneId)!: the zone to combine with, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/ZonedDateTime!` | the zoned date-time formed from this instant and the specified zone, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the result exceeds the supported range |

### compareTo

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun compareTo(other: Instant!): Int
```

Compares this instant to the specified instant.

The comparison is based on the time-line position of the instants. It is "consistent with equals", as defined by `https://developer.android.com/reference/kotlin/java/lang/Comparable.html#`.

| Parameters ||
|---|---|
| `o` | the object to be compared. |
| `otherInstant` | the other instant to compare to, not null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the comparator value, that is less than zero if this instant is before `otherInstant`, zero if they are equal, or greater than zero if this instant is after `otherInstant` |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the specified object's type prevents it from being compared to this object. |
| `java.lang.NullPointerException` | if otherInstant is null |

**See Also**

- `https://developer.android.com/reference/kotlin/java/time/Instant#isBefore(java.time.Instant)`
- `https://developer.android.com/reference/kotlin/java/time/Instant#isAfter(java.time.Instant)`

### equals

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

Checks if this instant is equal to the specified instant.

The comparison is based on the time-line position of the instants.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |
| `other` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?: the other instant, null returns false |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the other instant is equal to this one |

### from

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun from(temporal: TemporalAccessor!): Instant!
```

Obtains an instance of `Instant` from a temporal object.

This obtains an instant based on the specified temporal. A `TemporalAccessor` represents an arbitrary set of date and time information, which this factory converts to an instance of `Instant`.

The conversion extracts the `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField` and `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField` fields.

This method matches the signature of the functional interface `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery` allowing it to be used as a query via method reference, `Instant::from`.

| Parameters ||
|---|---|
| `temporal` | [TemporalAccessor](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAccessor)!: the temporal object to convert, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/Instant#!` | the instant, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if unable to convert to an `Instant` |

### get

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun get(field: TemporalField!): Int
```

Gets the value of the specified field from this instant as an `int`.

This queries this instant for the value of the specified field. The returned value will always be within the valid range of values for the field. If it is not possible to return the value, because the field is not supported or for some other reason, an exception is thrown.

If the field is a `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField` then the query is implemented here. The `https://developer.android.com/reference/kotlin/java/time/Instant#isSupported(java.time.temporal.TemporalField)` will return valid values based on this date-time, except `INSTANT_SECONDS` which is too large to fit in an `int` and throws a `DateTimeException`. All other `ChronoField` instances will throw an `UnsupportedTemporalTypeException`.

If the field is not a `ChronoField`, then the result of this method is obtained by invoking `TemporalField.getFrom(TemporalAccessor)` passing `this` as the argument. Whether the value can be obtained, and what the value represents, is determined by the field.

| Parameters ||
|---|---|
| `field` | [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField)!: the field to get, not null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the value for the field |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if a value for the field cannot be obtained or the value is outside the range of valid values for the field |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the field is not supported or the range of values exceeds an `int` |

### getEpochSecond

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getEpochSecond(): Long
```

Gets the number of seconds from the Java epoch of 1970-01-01T00:00:00Z.

The epoch second count is a simple incrementing count of seconds where second 0 is 1970-01-01T00:00:00Z. The nanosecond part is returned by `https://developer.android.com/reference/kotlin/java/time/Instant#getNano()`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the seconds from the epoch of 1970-01-01T00:00:00Z |

### getLong

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getLong(field: TemporalField!): Long
```

Gets the value of the specified field from this instant as a `long`.

This queries this instant for the value of the specified field. If it is not possible to return the value, because the field is not supported or for some other reason, an exception is thrown.

If the field is a `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField` then the query is implemented here. The `https://developer.android.com/reference/kotlin/java/time/Instant#isSupported(java.time.temporal.TemporalField)` will return valid values based on this date-time. All other `ChronoField` instances will throw an `UnsupportedTemporalTypeException`.

If the field is not a `ChronoField`, then the result of this method is obtained by invoking `TemporalField.getFrom(TemporalAccessor)` passing `this` as the argument. Whether the value can be obtained, and what the value represents, is determined by the field.

| Parameters ||
|---|---|
| `field` | [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField)!: the field to get, not null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the value for the field |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if a value for the field cannot be obtained |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the field is not supported |

### getNano

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getNano(): Int
```

Gets the number of nanoseconds, later along the time-line, from the start of the second.

The nanosecond-of-second value measures the total number of nanoseconds from the second returned by `https://developer.android.com/reference/kotlin/java/time/Instant#getEpochSecond()`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the nanoseconds within the second, always positive, never exceeds 999,999,999 |

### hashCode

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

Returns a hash code for this instant.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a suitable hash code |

### isAfter

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isAfter(otherInstant: Instant!): Boolean
```

Checks if this instant is after the specified instant.

The comparison is based on the time-line position of the instants.

| Parameters ||
|---|---|
| `otherInstant` | [Instant](https://developer.android.com/reference/kotlin/java/time/Instant#)!: the other instant to compare to, not null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this instant is after the specified instant |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if otherInstant is null |

### isBefore

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isBefore(otherInstant: Instant!): Boolean
```

Checks if this instant is before the specified instant.

The comparison is based on the time-line position of the instants.

| Parameters ||
|---|---|
| `otherInstant` | [Instant](https://developer.android.com/reference/kotlin/java/time/Instant#)!: the other instant to compare to, not null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this instant is before the specified instant |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if otherInstant is null |

### isSupported

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isSupported(field: TemporalField!): Boolean
```

Checks if the specified field is supported.

This checks if this instant can be queried for the specified field. If false, then calling the `https://developer.android.com/reference/kotlin/java/time/Instant#range(java.time.temporal.TemporalField)`, `https://developer.android.com/reference/kotlin/java/time/Instant#get(java.time.temporal.TemporalField)` and `https://developer.android.com/reference/kotlin/java/time/Instant#with(java.time.temporal.TemporalField,%20kotlin.Long)` methods will throw an exception.

If the field is a `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField` then the query is implemented here. The supported fields are:

- `NANO_OF_SECOND`
- `MICRO_OF_SECOND`
- `MILLI_OF_SECOND`
- `INSTANT_SECONDS`

All other `ChronoField` instances will return false.

If the field is not a `ChronoField`, then the result of this method is obtained by invoking `TemporalField.isSupportedBy(TemporalAccessor)` passing `this` as the argument. Whether the field is supported is determined by the field.

| Parameters ||
|---|---|
| `field` | [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField)!: the field to check, null returns false |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the field is supported on this instant, false if not |

### isSupported

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isSupported(unit: TemporalUnit!): Boolean
```

Checks if the specified unit is supported.

This checks if the specified unit can be added to, or subtracted from, this date-time. If false, then calling the `https://developer.android.com/reference/kotlin/java/time/Instant#plus(kotlin.Long,%20java.time.temporal.TemporalUnit)` and `https://developer.android.com/reference/kotlin/java/time/Instant#minus(kotlin.Long,%20java.time.temporal.TemporalUnit)` methods will throw an exception.

If the unit is a `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit` then the query is implemented here. The supported units are:

- `NANOS`
- `MICROS`
- `MILLIS`
- `SECONDS`
- `MINUTES`
- `HOURS`
- `HALF_DAYS`
- `DAYS`

All other `ChronoUnit` instances will return false.

If the unit is not a `ChronoUnit`, then the result of this method is obtained by invoking `TemporalUnit.isSupportedBy(Temporal)` passing `this` as the argument. Whether the unit is supported is determined by the unit.

| Parameters ||
|---|---|
| `unit` | [TemporalUnit](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit)!: the unit to check, null returns false |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the unit can be added/subtracted, false if not |

### minus

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun minus(amountToSubtract: TemporalAmount!): Instant!
```

Returns a copy of this instant with the specified amount subtracted.

This returns an `Instant`, based on this one, with the specified amount subtracted. The amount is typically `https://developer.android.com/reference/kotlin/java/time/Duration` but may be any other type implementing the `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount` interface.

The calculation is delegated to the amount object by calling `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount#subtractFrom(java.time.temporal.Temporal)`. The amount implementation is free to implement the subtraction in any way it wishes, however it typically calls back to `https://developer.android.com/reference/kotlin/java/time/Instant#minus(kotlin.Long,%20java.time.temporal.TemporalUnit)`. Consult the documentation of the amount implementation to determine if it can be successfully subtracted.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `amount` | the amount to subtract, not null |
| `amountToSubtract` | [TemporalAmount](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount)!: the amount to subtract, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/Instant#!` | an `Instant` based on this instant with the subtraction made, not null |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if the subtraction cannot be made |

### minus

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun minus(
    amountToSubtract: Long, 
    unit: TemporalUnit!
): Instant!
```

Returns a copy of this instant with the specified amount subtracted.

This returns an `Instant`, based on this one, with the amount in terms of the unit subtracted. If it is not possible to subtract the amount, because the unit is not supported or for some other reason, an exception is thrown.

This method is equivalent to `https://developer.android.com/reference/kotlin/java/time/Instant#plus(kotlin.Long,%20java.time.temporal.TemporalUnit)` with the amount negated. See that method for a full description of how addition, and thus subtraction, works.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `amountToSubtract` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the amount of the unit to subtract from the result, may be negative |
| `unit` | [TemporalUnit](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit)!: the unit of the amount to subtract, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/Instant#!` | an `Instant` based on this instant with the specified amount subtracted, not null |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if the subtraction cannot be made |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the unit is not supported |

### minusMillis

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun minusMillis(millisToSubtract: Long): Instant!
```

Returns a copy of this instant with the specified duration in milliseconds subtracted.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `millisToSubtract` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the milliseconds to subtract, positive or negative |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/Instant#!` | an `Instant` based on this instant with the specified milliseconds subtracted, not null |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if the result exceeds the maximum or minimum instant |

### minusNanos

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun minusNanos(nanosToSubtract: Long): Instant!
```

Returns a copy of this instant with the specified duration in nanoseconds subtracted.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `nanosToSubtract` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the nanoseconds to subtract, positive or negative |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/Instant#!` | an `Instant` based on this instant with the specified nanoseconds subtracted, not null |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if the result exceeds the maximum or minimum instant |

### minusSeconds

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun minusSeconds(secondsToSubtract: Long): Instant!
```

Returns a copy of this instant with the specified duration in seconds subtracted.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `secondsToSubtract` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the seconds to subtract, positive or negative |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/Instant#!` | an `Instant` based on this instant with the specified seconds subtracted, not null |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if the result exceeds the maximum or minimum instant |

### now

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun now(): Instant!
```

Obtains the current instant from the system clock.

This will query the `https://developer.android.com/reference/kotlin/java/time/Clock#systemUTC()` to obtain the current instant.

Using this method will prevent the ability to use an alternate time-source for testing because the clock is effectively hard-coded.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/Instant#!` | the current instant using the system clock, not null |

### now

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun now(clock: Clock!): Instant!
```

Obtains the current instant from the specified clock.

This will query the specified clock to obtain the current time.

Using this method allows the use of an alternate clock for testing. The alternate clock may be introduced using `https://developer.android.com/reference/kotlin/java/time/Clock`.

| Parameters ||
|---|---|
| `clock` | [Clock](https://developer.android.com/reference/kotlin/java/time/Clock)!: the clock to use, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/Instant#!` | the current instant, not null |

### ofEpochMilli

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun ofEpochMilli(epochMilli: Long): Instant!
```

Obtains an instance of `Instant` using milliseconds from the epoch of 1970-01-01T00:00:00Z.

The seconds and nanoseconds are extracted from the specified milliseconds.

| Parameters ||
|---|---|
| `epochMilli` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the number of milliseconds from 1970-01-01T00:00:00Z |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/Instant#!` | an instant, not null |

### ofEpochSecond

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun ofEpochSecond(epochSecond: Long): Instant!
```

Obtains an instance of `Instant` using seconds from the epoch of 1970-01-01T00:00:00Z.

The nanosecond field is set to zero.

| Parameters ||
|---|---|
| `epochSecond` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the number of seconds from 1970-01-01T00:00:00Z |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/Instant#!` | an instant, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the instant exceeds the maximum or minimum instant |

### ofEpochSecond

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun ofEpochSecond(
    epochSecond: Long, 
    nanoAdjustment: Long
): Instant!
```

Obtains an instance of `Instant` using seconds from the epoch of 1970-01-01T00:00:00Z and nanosecond fraction of second.

This method allows an arbitrary number of nanoseconds to be passed in. The factory will alter the values of the second and nanosecond in order to ensure that the stored nanosecond is in the range 0 to 999,999,999. For example, the following will result in exactly the same instant:

```kotlin
Instant.ofEpochSecond(3, 1);
   Instant.ofEpochSecond(4, -999_999_999);
   Instant.ofEpochSecond(2, 1000_000_001);
  
```

| Parameters ||
|---|---|
| `epochSecond` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the number of seconds from 1970-01-01T00:00:00Z |
| `nanoAdjustment` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the nanosecond adjustment to the number of seconds, positive or negative |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/Instant#!` | an instant, not null |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if the instant exceeds the maximum or minimum instant |

### parse

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun parse(text: CharSequence!): Instant!
```

Obtains an instance of `Instant` from a text string such as `2007-12-03T10:15:30.00Z`.

The string must represent a valid instant in UTC and is parsed using `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#ISO_INSTANT:java.time.format.DateTimeFormatter`.

| Parameters ||
|---|---|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: the text to parse, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/Instant#!` | the parsed instant, not null |

| Exceptions ||
|---|---|
| `java.time.format.DateTimeParseException` | if the text cannot be parsed |

### plus

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun plus(amountToAdd: TemporalAmount!): Instant!
```

Returns a copy of this instant with the specified amount added.

This returns an `Instant`, based on this one, with the specified amount added. The amount is typically `https://developer.android.com/reference/kotlin/java/time/Duration` but may be any other type implementing the `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount` interface.

The calculation is delegated to the amount object by calling `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount#addTo(java.time.temporal.Temporal)`. The amount implementation is free to implement the addition in any way it wishes, however it typically calls back to `https://developer.android.com/reference/kotlin/java/time/Instant#plus(kotlin.Long,%20java.time.temporal.TemporalUnit)`. Consult the documentation of the amount implementation to determine if it can be successfully added.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `amount` | the amount to add, not null |
| `amountToAdd` | [TemporalAmount](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAmount)!: the amount to add, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/Instant#!` | an `Instant` based on this instant with the addition made, not null |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if the addition cannot be made |

### plus

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun plus(
    amountToAdd: Long, 
    unit: TemporalUnit!
): Instant!
```

Returns a copy of this instant with the specified amount added.

This returns an `Instant`, based on this one, with the amount in terms of the unit added. If it is not possible to add the amount, because the unit is not supported or for some other reason, an exception is thrown.

If the field is a `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit` then the addition is implemented here. The supported fields behave as follows:

- `NANOS` - Returns an `Instant` with the specified number of nanoseconds added. This is equivalent to `https://developer.android.com/reference/kotlin/java/time/Instant#plusNanos(kotlin.Long)`.
- `MICROS` - Returns an `Instant` with the specified number of microseconds added. This is equivalent to `https://developer.android.com/reference/kotlin/java/time/Instant#plusNanos(kotlin.Long)` with the amount multiplied by 1,000.
- `MILLIS` - Returns an `Instant` with the specified number of milliseconds added. This is equivalent to `https://developer.android.com/reference/kotlin/java/time/Instant#plusNanos(kotlin.Long)` with the amount multiplied by 1,000,000.
- `SECONDS` - Returns an `Instant` with the specified number of seconds added. This is equivalent to `https://developer.android.com/reference/kotlin/java/time/Instant#plusSeconds(kotlin.Long)`.
- `MINUTES` - Returns an `Instant` with the specified number of minutes added. This is equivalent to `https://developer.android.com/reference/kotlin/java/time/Instant#plusSeconds(kotlin.Long)` with the amount multiplied by 60.
- `HOURS` - Returns an `Instant` with the specified number of hours added. This is equivalent to `https://developer.android.com/reference/kotlin/java/time/Instant#plusSeconds(kotlin.Long)` with the amount multiplied by 3,600.
- `HALF_DAYS` - Returns an `Instant` with the specified number of half-days added. This is equivalent to `https://developer.android.com/reference/kotlin/java/time/Instant#plusSeconds(kotlin.Long)` with the amount multiplied by 43,200 (12 hours).
- `DAYS` - Returns an `Instant` with the specified number of days added. This is equivalent to `https://developer.android.com/reference/kotlin/java/time/Instant#plusSeconds(kotlin.Long)` with the amount multiplied by 86,400 (24 hours).

All other `ChronoUnit` instances will throw an `UnsupportedTemporalTypeException`.

If the field is not a `ChronoUnit`, then the result of this method is obtained by invoking `TemporalUnit.addTo(Temporal, long)` passing `this` as the argument. In this case, the unit determines whether and how to perform the addition.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `amountToAdd` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the amount of the unit to add to the result, may be negative |
| `unit` | [TemporalUnit](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit)!: the unit of the amount to add, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/Instant#!` | an `Instant` based on this instant with the specified amount added, not null |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if the addition cannot be made |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the unit is not supported |

### plusMillis

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun plusMillis(millisToAdd: Long): Instant!
```

Returns a copy of this instant with the specified duration in milliseconds added.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `millisToAdd` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the milliseconds to add, positive or negative |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/Instant#!` | an `Instant` based on this instant with the specified milliseconds added, not null |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if the result exceeds the maximum or minimum instant |

### plusNanos

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun plusNanos(nanosToAdd: Long): Instant!
```

Returns a copy of this instant with the specified duration in nanoseconds added.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `nanosToAdd` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the nanoseconds to add, positive or negative |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/Instant#!` | an `Instant` based on this instant with the specified nanoseconds added, not null |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if the result exceeds the maximum or minimum instant |

### plusSeconds

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun plusSeconds(secondsToAdd: Long): Instant!
```

Returns a copy of this instant with the specified duration in seconds added.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `secondsToAdd` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the seconds to add, positive or negative |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/Instant#!` | an `Instant` based on this instant with the specified seconds added, not null |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if the result exceeds the maximum or minimum instant |

### query

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <R : Any!> query(query: TemporalQuery<R>!): R
```

Queries this instant using the specified query.

This queries this instant using the specified query strategy object. The `TemporalQuery` object defines the logic to be used to obtain the result. Read the documentation of the query to understand what the result of this method will be.

The result of this method is obtained by invoking the `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery#queryFrom(java.time.temporal.TemporalAccessor)` method on the specified query passing `this` as the argument.

| Parameters ||
|---|---|
| `<R>` | the type of the result |
| `query` | [TemporalQuery](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalQuery)\<R\>!: the query to invoke, not null |

| Return ||
|---|---|
| `R` | the query result, null may be returned (defined by the query) |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs (defined by the query) |
| `java.time.DateTimeException` | if unable to query (defined by the query) |

### range

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun range(field: TemporalField!): ValueRange!
```

Gets the range of valid values for the specified field.

The range object expresses the minimum and maximum valid values for a field. This instant is used to enhance the accuracy of the returned range. If it is not possible to return the range, because the field is not supported or for some other reason, an exception is thrown.

If the field is a `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField` then the query is implemented here. The `https://developer.android.com/reference/kotlin/java/time/Instant#isSupported(java.time.temporal.TemporalField)` will return appropriate range instances. All other `ChronoField` instances will throw an `UnsupportedTemporalTypeException`.

If the field is not a `ChronoField`, then the result of this method is obtained by invoking `TemporalField.rangeRefinedBy(TemporalAccessor)` passing `this` as the argument. Whether the range can be obtained is determined by the field.

| Parameters ||
|---|---|
| `field` | [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField)!: the field to query the range for, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/temporal/ValueRange!` | the range of valid values for the field, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the range for the field cannot be obtained |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the field is not supported |

### toEpochMilli

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toEpochMilli(): Long
```

Converts this instant to the number of milliseconds from the epoch of 1970-01-01T00:00:00Z.

If this instant represents a point on the time-line too far in the future or past to fit in a `long` milliseconds, then an exception is thrown.

If this instant has greater than millisecond precision, then the conversion will drop any excess precision information as though the amount in nanoseconds was subject to integer division by one million.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the number of milliseconds since the epoch of 1970-01-01T00:00:00Z |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs |

### toString

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

A string representation of this instant using ISO-8601 representation.

The format used is the same as `https://developer.android.com/reference/kotlin/java/time/format/DateTimeFormatter#ISO_INSTANT:java.time.format.DateTimeFormatter`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | an ISO-8601 representation of this instant, not null |

### truncatedTo

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun truncatedTo(unit: TemporalUnit!): Instant!
```

Returns a copy of this `Instant` truncated to the specified unit.

Truncating the instant returns a copy of the original with fields smaller than the specified unit set to zero. The fields are calculated on the basis of using a UTC offset as seen in `toString`. For example, truncating with the `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit` unit will round down to the nearest minute, setting the seconds and nanoseconds to zero.

The unit must have a [duration](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit#getDuration()) that divides into the length of a standard day without remainder. This includes all supplied time units on `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit` and `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit`. Other units throw an exception.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `unit` | [TemporalUnit](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit)!: the unit to truncate to, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/Instant#!` | an `Instant` based on this instant with the time truncated, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the unit is invalid for truncation |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the unit is not supported |

### until

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun until(endExclusive: Instant): Duration
```

Calculates the `Duration` until another `Instant`.

The start and end points are `this` and the specified instant. The result will be negative if the end is before the start. Calling this method is equivalent to `https://developer.android.com/reference/kotlin/java/time/Duration#between(java.time.temporal.Temporal,%20java.time.temporal.Temporal)`.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `endExclusive` | [Instant](https://developer.android.com/reference/kotlin/java/time/Instant#): the end `Instant`, exclusive, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/Duration` | the `Duration` from this `Instant` until the specified `endExclusive` `Instant` |

**See Also**

- `https://developer.android.com/reference/kotlin/java/time/Duration#between(java.time.temporal.Temporal,%20java.time.temporal.Temporal)`

### until

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun until(
    endExclusive: Temporal!, 
    unit: TemporalUnit!
): Long
```

Calculates the amount of time until another instant in terms of the specified unit.

This calculates the amount of time between two `Instant` objects in terms of a single `TemporalUnit`. The start and end points are `this` and the specified instant. The result will be negative if the end is before the start. The calculation returns a whole number, representing the number of complete units between the two instants. The `Temporal` passed to this method is converted to a `Instant` using `https://developer.android.com/reference/kotlin/java/time/Instant#from(java.time.temporal.TemporalAccessor)`. For example, the amount in seconds between two dates can be calculated using `startInstant.until(endInstant, SECONDS)`.

There are two equivalent ways of using this method. The first is to invoke this method. The second is to use `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit#between(java.time.temporal.Temporal,%20java.time.temporal.Temporal)`:

```kotlin
// these two lines are equivalent
    amount = start.until(end, SECONDS);
    amount = SECONDS.between(start, end);
  
```
The choice should be made based on which makes the code more readable.

The calculation is implemented in this method for `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoUnit`. The units `NANOS`, `MICROS`, `MILLIS`, `SECONDS`, `MINUTES`, `HOURS`, `HALF_DAYS` and `DAYS` are supported. Other `ChronoUnit` values will throw an exception.

If the unit is not a `ChronoUnit`, then the result of this method is obtained by invoking `TemporalUnit.between(Temporal, Temporal)` passing `this` as the first argument and the converted input temporal as the second argument.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `endExclusive` | [Temporal](https://developer.android.com/reference/kotlin/java/time/temporal/Temporal)!: the end date, exclusive, which is converted to an `Instant`, not null |
| `unit` | [TemporalUnit](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalUnit)!: the unit to measure the amount in, not null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the amount of time between this instant and the end instant |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if the amount cannot be calculated, or the end temporal cannot be converted to an `Instant` |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the unit is not supported |

### with

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun with(adjuster: TemporalAdjuster!): Instant!
```

Returns an adjusted copy of this instant.

This returns an `Instant`, based on this one, with the instant adjusted. The adjustment takes place using the specified adjuster strategy object. Read the documentation of the adjuster to understand what adjustment will be made.

The result of this method is obtained by invoking the `https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAdjuster#adjustInto(java.time.temporal.Temporal)` method on the specified adjuster passing `this` as the argument.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `adjuster` | [TemporalAdjuster](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalAdjuster)!: the adjuster to use, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/Instant#!` | an `Instant` based on `this` with the adjustment made, not null |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if the adjustment cannot be made |

### with

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun with(
    field: TemporalField!, 
    newValue: Long
): Instant!
```

Returns a copy of this instant with the specified field set to a new value.

This returns an `Instant`, based on this one, with the value for the specified field changed. If it is not possible to set the value, because the field is not supported or for some other reason, an exception is thrown.

If the field is a `https://developer.android.com/reference/kotlin/java/time/temporal/ChronoField` then the adjustment is implemented here. The supported fields behave as follows:

- `NANO_OF_SECOND` - Returns an `Instant` with the specified nano-of-second. The epoch-second will be unchanged.
- `MICRO_OF_SECOND` - Returns an `Instant` with the nano-of-second replaced by the specified micro-of-second multiplied by 1,000. The epoch-second will be unchanged.
- `MILLI_OF_SECOND` - Returns an `Instant` with the nano-of-second replaced by the specified milli-of-second multiplied by 1,000,000. The epoch-second will be unchanged.
- `INSTANT_SECONDS` - Returns an `Instant` with the specified epoch-second. The nano-of-second will be unchanged.

In all cases, if the new value is outside the valid range of values for the field then a `DateTimeException` will be thrown.

All other `ChronoField` instances will throw an `UnsupportedTemporalTypeException`.

If the field is not a `ChronoField`, then the result of this method is obtained by invoking `TemporalField.adjustInto(Temporal, long)` passing `this` as the argument. In this case, the field determines whether and how to adjust the instant.

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `field` | [TemporalField](https://developer.android.com/reference/kotlin/java/time/temporal/TemporalField)!: the field to set in the result, not null |
| `newValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the new value of the field in the result |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/Instant#!` | an `Instant` based on `this` with the specified field set, not null |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if the field cannot be set |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the field is not supported |

## Properties

### EPOCH

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EPOCH: Instant!
```

Constant for the 1970-01-01T00:00:00Z epoch instant.

### MAX

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MAX: Instant!
```

The maximum supported `Instant`, '1000000000-12-31T23:59:59.999999999Z'. This could be used by an application as a "far future" instant.

This is one year later than the maximum `LocalDateTime`. This provides sufficient values to handle the range of `ZoneOffset` which affect the instant in addition to the local date-time. The value is also chosen such that the value of the year fits in an `int`.

### MIN

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIN: Instant!
```

The minimum supported `Instant`, '-1000000000-01-01T00:00Z'. This could be used by an application as a "far past" instant.

This is one year earlier than the minimum `LocalDateTime`. This provides sufficient values to handle the range of `ZoneOffset` which affect the instant in addition to the local date-time. The value is also chosen such that the value of the year fits in an `int`.
