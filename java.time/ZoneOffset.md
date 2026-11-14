Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ZoneOffset

```
class ZoneOffset : ZoneId, Comparable<ZoneOffset!>, Serializable, TemporalAccessor, TemporalAdjuster
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.time.ZoneId](ZoneId.md) ||
| | ↳ | [java.time.ZoneOffset](ZoneOffset.md) |

A time-zone offset from Greenwich/UTC, such as `+02:00`.

A time-zone offset is the amount of time that a time-zone differs from Greenwich/UTC. This is usually a fixed number of hours and minutes.

Different parts of the world have different time-zone offsets. The rules for how offsets vary by place and time of year are captured in the ZoneId class.

For example, Paris is one hour ahead of Greenwich/UTC in winter and two hours ahead in summer. The `ZoneId` instance for Paris will reference two `ZoneOffset` instances - a `+01:00` instance for winter, and a `+02:00` instance for summer.

In 2008, time-zone offsets around the world extended from -12:00 to +14:00. To prevent any problems with that range being extended, yet still provide validation, the range of offsets is restricted to -18:00 to 18:00 inclusive.

This class is designed for use with the ISO calendar system. The fields of hours, minutes and seconds make assumptions that are valid for the standard ISO definitions of those fields. This class may be used with other calendar systems providing the definition of the time fields matches those of the ISO calendar system.

Instances of `ZoneOffset` must be compared using equals. Implementations may choose to cache certain common offsets, however applications must not rely on such caching.

This is a [value-based](https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/lang/doc-files/ValueBased.html) class; programmers should treat instances that are [equal](ZoneOffset.md)) as interchangeable and should not use instances for synchronization, or unpredictable behavior may occur. For example, in a future release, synchronization may fail. The `equals` method should be used for comparisons.

## Summary

| Public methods ||
|---|---|
| [Temporal](../java.time.temporal/Temporal.md)! | adjustInto Adjusts the specified temporal object to have the same offset as this object. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | compareTo Compares this offset to another offset in descending order. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | equals Checks if this offset is equal to another offset. |
| --- | --- |
| static [ZoneOffset](ZoneOffset.md)! | from Obtains an instance of `ZoneOffset` from a temporal object. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | get Gets the value of the specified field from this offset as an `int`. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getId Gets the normalized zone offset ID. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | getLong Gets the value of the specified field from this offset as a `long`. |
| [ZoneRules](../java.time.zone/ZoneRules.md)! | getRules Gets the associated time-zone rules. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getTotalSeconds Gets the total zone offset in seconds. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | hashCode A hash code for this offset. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isSupported Checks if the specified field is supported. |
| static [ZoneOffset](ZoneOffset.md)! | of Obtains an instance of `ZoneOffset` using the ID. |
| --- | --- |
| static [ZoneOffset](ZoneOffset.md)! | ofHours Obtains an instance of `ZoneOffset` using an offset in hours. |
| static [ZoneOffset](ZoneOffset.md)! | ofHoursMinutes Obtains an instance of `ZoneOffset` using an offset in hours and minutes. |
| static [ZoneOffset](ZoneOffset.md)! | ofHoursMinutesSeconds Obtains an instance of `ZoneOffset` using an offset in hours, minutes and seconds. |
| --- | --- |
| static [ZoneOffset](ZoneOffset.md)! | ofTotalSeconds Obtains an instance of `ZoneOffset` specifying the total offset in seconds |
| R | query Queries this offset using the specified query. |
| [ValueRange](../java.time.temporal/ValueRange.md)! | range Gets the range of valid values for the specified field. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | toString Outputs this offset as a `String`, using the normalized ID. |

| Inherited functions ||
|---|---|
| From class ZoneId |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | getAvailableZoneIds Gets the set of available zone IDs. This set includes the string form of all available region-based IDs. Offset-based zone IDs are not included in the returned set. The ID can be passed to of to create a `ZoneId`. The set of zone IDs can increase over time, although in a typical application the set of IDs is fixed. Each call to this method is thread-safe. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | getDisplayName Gets the textual representation of the zone, such as 'British Time' or '+02:00'. This returns the textual name used to identify the time-zone ID, suitable for presentation to the user. The parameters control the style of the returned text and the locale. If no textual mapping is found then the getId is returned. <br /> | | `https://developer.android.com/reference/kotlin/java/time/ZoneId!` | normalized Normalizes the time-zone ID, returning a `ZoneOffset` where possible. The returns a normalized `ZoneId` that can be used in place of this ID. The result will have `ZoneRules` equivalent to those returned by this object, however the ID returned by `getId()` may be different. The normalization checks if the rules of this `ZoneId` have a fixed offset. If they do, then the `ZoneOffset` equal to that offset is returned. Otherwise `this` is returned. <br /> | | `https://developer.android.com/reference/kotlin/java/time/ZoneId!` | of Obtains an instance of `ZoneId` using its ID using a map of aliases to supplement the standard zone IDs. Many users of time-zones use short abbreviations, such as PST for 'Pacific Standard Time' and PDT for 'Pacific Daylight Time'. These abbreviations are not unique, and so cannot be used as IDs. This method allows a map of string to time-zone to be setup and reused within an application. <br /> | | `https://developer.android.com/reference/kotlin/java/time/ZoneId!` | ofOffset Obtains an instance of `ZoneId` wrapping an offset. If the prefix is "GMT", "UTC", or "UT" a `ZoneId` with the prefix and the non-zero offset is returned. If the prefix is empty `""` the `ZoneOffset` is returned. <br /> | | `https://developer.android.com/reference/kotlin/java/time/ZoneId!` | systemDefault Gets the system default time-zone. This queries getDefault to find the default time-zone and converts it to a `ZoneId`. If the system default time-zone is changed, then the result of this method will also change. <br /> | ||

| Properties ||
|---|---|
| static [ZoneOffset](ZoneOffset.md)! | `https://developer.android.com/reference/kotlin/java/time/ZoneOffset#MAX:java.time.ZoneOffset` Constant for the maximum supported offset. |
| static [ZoneOffset](ZoneOffset.md)! | `https://developer.android.com/reference/kotlin/java/time/ZoneOffset#MIN:java.time.ZoneOffset` Constant for the minimum supported offset. |
| static [ZoneOffset](ZoneOffset.md)! | `https://developer.android.com/reference/kotlin/java/time/ZoneOffset#UTC:java.time.ZoneOffset` The time-zone offset for UTC, with an ID of 'Z'. |
| --- | --- |

| Inherited properties ||
|---|---|
| From class ZoneId |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | `https://developer.android.com/reference/kotlin/java/time/ZoneId#SHORT_IDS:kotlin.collections.MutableMap` A map of zone overrides to enable the short time-zone names to be used. Use of short zone IDs has been deprecated in `java.util.TimeZone`. This map allows the IDs to continue to be used via the of factory method. This map contains a mapping of the IDs that is in line with TZDB 2005r and later, where 'EST', 'MST' and 'HST' map to IDs which do not include daylight savings. This maps as follows: - EST - -05:00 - HST - -10:00 - MST - -07:00 - ACT - Australia/Darwin - AET - Australia/Sydney - AGT - America/Argentina/Buenos_Aires - ART - Africa/Cairo - AST - America/Anchorage - BET - America/Sao_Paulo - BST - Asia/Dhaka - CAT - Africa/Harare - CNT - America/St_Johns - CST - America/Chicago - CTT - Asia/Shanghai - EAT - Africa/Addis_Ababa - ECT - Europe/Paris - IET - America/Indiana/Indianapolis - IST - Asia/Kolkata - JST - Asia/Tokyo - MIT - Pacific/Apia - NET - Asia/Yerevan - NST - Pacific/Auckland - PLT - Asia/Karachi - PNT - America/Phoenix - PRT - America/Puerto_Rico - PST - America/Los_Angeles - SST - Pacific/Guadalcanal - VST - Asia/Ho_Chi_Minh The map is unmodifiable. <br /> | ||

## Public methods

### adjustInto

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun adjustInto(temporal: Temporal!): Temporal!
```

Adjusts the specified temporal object to have the same offset as this object.

This returns a temporal object of the same observable type as the input with the offset changed to be the same as this.

The adjustment is equivalent to using with passing ChronoField as the field.

In most cases, it is clearer to reverse the calling pattern by using with:

```kotlin
// these two lines are equivalent, but the second approach is recommended
    temporal = thisOffset.adjustInto(temporal);
    temporal = temporal.with(thisOffset);
  
```

This instance is immutable and unaffected by this method call.

| Parameters ||
|---|---|
| `temporal` | [Temporal](../java.time.temporal/Temporal.md)!: the target object to be adjusted, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/temporal/Temporal!` | the adjusted object, not null |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if unable to make the adjustment |

### compareTo

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun compareTo(other: ZoneOffset!): Int
```

Compares this offset to another offset in descending order.

The offsets are compared in the order that they occur for the same time of day around the world. Thus, an offset of `+10:00` comes before an offset of `+09:00` and so on down to `-18:00`.

The comparison is "consistent with equals", as defined by `https://developer.android.com/reference/kotlin/java/lang/Comparable.html#`.

| Parameters ||
|---|---|
| `o` | the object to be compared. |
| `other` | [ZoneOffset](ZoneOffset.md)!: the other date to compare to, not null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the comparator value, negative if less, positive if greater |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the specified object's type prevents it from being compared to this object. |
| `java.lang.NullPointerException` | if `other` is null |

### equals

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

Checks if this offset is equal to another offset.

The comparison is based on the amount of the offset in seconds. This is equivalent to a comparison by ID.

| Parameters ||
|---|---|
| `obj` | the object to check, null returns false |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this is equal to the other offset |

### from

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun from(temporal: TemporalAccessor!): ZoneOffset!
```

Obtains an instance of `ZoneOffset` from a temporal object.

This obtains an offset based on the specified temporal. A `TemporalAccessor` represents an arbitrary set of date and time information, which this factory converts to an instance of `ZoneOffset`.

A `TemporalAccessor` represents some form of date and time information. This factory converts the arbitrary temporal object to an instance of `ZoneOffset`.

The conversion uses the offset query, which relies on extracting the ChronoField field.

This method matches the signature of the functional interface TemporalQuery allowing it to be used as a query via method reference, `ZoneOffset::from`.

| Parameters ||
|---|---|
| `temporal` | [TemporalAccessor](../java.time.temporal/TemporalAccessor.md)!: the temporal object to convert, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/ZoneOffset#!` | the zone-offset, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if unable to convert to an `ZoneOffset` |

### get

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun get(field: TemporalField!): Int
```

Gets the value of the specified field from this offset as an `int`.

This queries this offset for the value of the specified field. The returned value will always be within the valid range of values for the field. If it is not possible to return the value, because the field is not supported or for some other reason, an exception is thrown.

If the field is a ChronoField then the query is implemented here. The `OFFSET_SECONDS` field returns the value of the offset. All other `ChronoField` instances will throw an `UnsupportedTemporalTypeException`.

If the field is not a `ChronoField`, then the result of this method is obtained by invoking `TemporalField.getFrom(TemporalAccessor)` passing `this` as the argument. Whether the value can be obtained, and what the value represents, is determined by the field.

| Parameters ||
|---|---|
| `field` | [TemporalField](../java.time.temporal/TemporalField.md)!: the field to get, not null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the value for the field |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if a value for the field cannot be obtained or the value is outside the range of valid values for the field |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the field is not supported or the range of values exceeds an `int` |
| --- | --- |

### getId

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getId(): String!
```

Gets the normalized zone offset ID.

The ID is minor variation to the standard ISO-8601 formatted string for the offset. There are three formats:

- `Z` - for UTC (ISO-8601)
- `+hh:mm` or `-hh:mm` - if the seconds are zero (ISO-8601)
- `+hh:mm:ss` or `-hh:mm:ss` - if the seconds are non-zero (not ISO-8601)

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the zone offset ID, not null |

### getLong

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getLong(field: TemporalField!): Long
```

Gets the value of the specified field from this offset as a `long`.

This queries this offset for the value of the specified field. If it is not possible to return the value, because the field is not supported or for some other reason, an exception is thrown.

If the field is a ChronoField then the query is implemented here. The `OFFSET_SECONDS` field returns the value of the offset. All other `ChronoField` instances will throw an `UnsupportedTemporalTypeException`.

If the field is not a `ChronoField`, then the result of this method is obtained by invoking `TemporalField.getFrom(TemporalAccessor)` passing `this` as the argument. Whether the value can be obtained, and what the value represents, is determined by the field.

| Parameters ||
|---|---|
| `field` | [TemporalField](../java.time.temporal/TemporalField.md)!: the field to get, not null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the value for the field |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | if numeric overflow occurs |
| `java.time.DateTimeException` | if a value for the field cannot be obtained |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the field is not supported |
| --- | --- |

### getRules

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getRules(): ZoneRules!
```

Gets the associated time-zone rules.

The rules will always return this offset when queried. The implementation class is immutable, thread-safe and serializable.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/zone/ZoneRules!` | the rules, not null |

| Exceptions ||
|---|---|
| `java.time.zone.ZoneRulesException` | if no rules are available for this ID |

### getTotalSeconds

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTotalSeconds(): Int
```

Gets the total zone offset in seconds.

This is the primary way to access the offset amount. It returns the total of the hours, minutes and seconds fields as a single offset that can be added to a time.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the total zone offset amount in seconds |

### hashCode

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

A hash code for this offset.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a suitable hash code |

### isSupported

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isSupported(field: TemporalField!): Boolean
```

Checks if the specified field is supported.

This checks if this offset can be queried for the specified field. If false, then calling the range and get methods will throw an exception.

If the field is a ChronoField then the query is implemented here. The `OFFSET_SECONDS` field returns true. All other `ChronoField` instances will return false.

If the field is not a `ChronoField`, then the result of this method is obtained by invoking `TemporalField.isSupportedBy(TemporalAccessor)` passing `this` as the argument. Whether the field is supported is determined by the field.

| Parameters ||
|---|---|
| `field` | [TemporalField](../java.time.temporal/TemporalField.md)!: the field to check, null returns false |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the field is supported on this offset, false if not |

### of

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun of(offsetId: String!): ZoneOffset!
```

Obtains an instance of `ZoneOffset` using the ID.

This method parses the string ID of a `ZoneOffset` to return an instance. The parsing accepts all the formats generated by getId, plus some additional formats:

- `Z` - for UTC
- `+h`
- `+hh`
- `+hh:mm`
- `-hh:mm`
- `+hhmm`
- `-hhmm`
- `+hh:mm:ss`
- `-hh:mm:ss`
- `+hhmmss`
- `-hhmmss`

Note that ± means either the plus or minus symbol.

The ID of the returned offset will be normalized to one of the formats described by getId.

The maximum supported range is from +18:00 to -18:00 inclusive.

| Parameters ||
|---|---|
| `offsetId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the offset ID, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/ZoneOffset#!` | the zone-offset, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the offset ID is invalid |

### ofHours

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun ofHours(hours: Int): ZoneOffset!
```

Obtains an instance of `ZoneOffset` using an offset in hours.

| Parameters ||
|---|---|
| `hours` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the time-zone offset in hours, from -18 to +18 |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/ZoneOffset#!` | the zone-offset, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the offset is not in the required range |

### ofHoursMinutes

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun ofHoursMinutes(
    hours: Int, 
    minutes: Int
): ZoneOffset!
```

Obtains an instance of `ZoneOffset` using an offset in hours and minutes.

The sign of the hours and minutes components must match. Thus, if the hours is negative, the minutes must be negative or zero. If the hours is zero, the minutes may be positive, negative or zero.

| Parameters ||
|---|---|
| `hours` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the time-zone offset in hours, from -18 to +18 |
| `minutes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the time-zone offset in minutes, from 0 to ±59, sign matches hours |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/ZoneOffset#!` | the zone-offset, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the offset is not in the required range |

### ofHoursMinutesSeconds

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun ofHoursMinutesSeconds(
    hours: Int, 
    minutes: Int, 
    seconds: Int
): ZoneOffset!
```

Obtains an instance of `ZoneOffset` using an offset in hours, minutes and seconds.

The sign of the hours, minutes and seconds components must match. Thus, if the hours is negative, the minutes and seconds must be negative or zero.

| Parameters ||
|---|---|
| `hours` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the time-zone offset in hours, from -18 to +18 |
| `minutes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the time-zone offset in minutes, from 0 to ±59, sign matches hours and seconds |
| `seconds` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the time-zone offset in seconds, from 0 to ±59, sign matches hours and minutes |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/ZoneOffset#!` | the zone-offset, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the offset is not in the required range |

### ofTotalSeconds

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun ofTotalSeconds(totalSeconds: Int): ZoneOffset!
```

Obtains an instance of `ZoneOffset` specifying the total offset in seconds

The offset must be in the range `-18:00` to `+18:00`, which corresponds to -64800 to +64800.

| Parameters ||
|---|---|
| `totalSeconds` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the total time-zone offset in seconds, from -64800 to +64800 |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/ZoneOffset#!` | the ZoneOffset, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the offset is not in the required range |

### query

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <R : Any!> query(query: TemporalQuery<R>!): R
```

Queries this offset using the specified query.

This queries this offset using the specified query strategy object. The `TemporalQuery` object defines the logic to be used to obtain the result. Read the documentation of the query to understand what the result of this method will be.

The result of this method is obtained by invoking the queryFrom method on the specified query passing `this` as the argument.

| Parameters ||
|---|---|
| `<R>` | the type of the result |
| `query` | [TemporalQuery](../java.time.temporal/TemporalQuery.md)\<R\>!: the query to invoke, not null |

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

The range object expresses the minimum and maximum valid values for a field. This offset is used to enhance the accuracy of the returned range. If it is not possible to return the range, because the field is not supported or for some other reason, an exception is thrown.

If the field is a ChronoField then the query is implemented here. The isSupported will return appropriate range instances. All other `ChronoField` instances will throw an `UnsupportedTemporalTypeException`.

If the field is not a `ChronoField`, then the result of this method is obtained by invoking `TemporalField.rangeRefinedBy(TemporalAccessor)` passing `this` as the argument. Whether the range can be obtained is determined by the field.

| Parameters ||
|---|---|
| `field` | [TemporalField](../java.time.temporal/TemporalField.md)!: the field to query the range for, not null |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/temporal/ValueRange!` | the range of valid values for the field, not null |

| Exceptions ||
|---|---|
| `java.time.DateTimeException` | if the range for the field cannot be obtained |
| `java.time.temporal.UnsupportedTemporalTypeException` | if the field is not supported |

### toString

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Outputs this offset as a `String`, using the normalized ID.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of this offset, not null |

## Properties

### MAX

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MAX: ZoneOffset!
```

Constant for the maximum supported offset.

### MIN

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIN: ZoneOffset!
```

Constant for the minimum supported offset.

### UTC

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UTC: ZoneOffset!
```

The time-zone offset for UTC, with an ID of 'Z'.
