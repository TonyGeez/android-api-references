Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TimeZoneFormat

```
open class TimeZoneFormat : UFormat, Freezable<TimeZoneFormat!>, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [java.text.Format](https://developer.android.com/reference/kotlin/java/text/Format.html#) |||
| | ↳ | [android.icu.text.UFormat](https://developer.android.com/reference/kotlin/android/icu/text/UFormat) ||
| | | ↳ | [android.icu.text.TimeZoneFormat](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#) |
| --- | --- | --- | --- |

`TimeZoneFormat` supports time zone display name formatting and parsing. An instance of TimeZoneFormat works as a subformatter of `https://developer.android.com/reference/kotlin/android/icu/text/SimpleDateFormat`, but you can also directly get a new instance of `TimeZoneFormat` and formatting/parsing time zone display names.

ICU implements the time zone display names defined by [UTS#35 Unicode Locale Data Markup Language (LDML)](http://www.unicode.org/reports/tr35/). `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneNames` represents the time zone display name data model and this class implements the algorithm for actual formatting and parsing.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat.GMTOffsetPatternType` Offset pattern type enum. |
| | `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat.ParseOption` Parse option enum, used for specifying optional parse behavior. |
| | `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat.Style` Time zone display format style enum used by format/parse APIs in `TimeZoneFormat`. |
| --- | --- |
| | `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat.TimeType` Time type enum used for receiving time type (standard time, daylight time or unknown) in `TimeZoneFormat` APIs. |

| Protected constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#TimeZoneFormat(android.icu.util.ULocale)(locale: https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#!)` The protected constructor for subclassing. |

| Public methods ||
|---|---|
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#clone()()` Creates and returns a copy of this object. |
| open [TimeZoneFormat](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#)! | `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#cloneAsThawed()()` Provides for the clone operation. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#format(android.icu.text.TimeZoneFormat.Style,%20android.icu.util.TimeZone,%20kotlin.Long)(style: https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat.Style!, tz: https://developer.android.com/reference/kotlin/android/icu/util/TimeZone.html#!, date: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns the display name of the time zone at the given date for the style. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#format(android.icu.text.TimeZoneFormat.Style,%20android.icu.util.TimeZone,%20kotlin.Long,%20android.icu.util.Output)(style: https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat.Style!, tz: https://developer.android.com/reference/kotlin/android/icu/util/TimeZone.html#!, date: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, timeType: https://developer.android.com/reference/kotlin/android/icu/util/Output.html#<https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat.TimeType!>!)` Returns the display name of the time zone at the given date for the style. |
| open [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#)! | `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#format(kotlin.Any,%20java.lang.StringBuffer,%20java.text.FieldPosition)(obj: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!, toAppendTo: https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#!, pos: https://developer.android.com/reference/kotlin/java/text/FieldPosition.html#!)` Formats an object and appends the resulting text to a given string buffer. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#formatOffsetISO8601Basic(kotlin.Int,%20kotlin.Boolean,%20kotlin.Boolean,%20kotlin.Boolean)(offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, useUtcIndicator: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, isShort: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, ignoreSeconds: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Returns the ISO 8601 basic time zone string for the given offset. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#formatOffsetISO8601Extended(kotlin.Int,%20kotlin.Boolean,%20kotlin.Boolean,%20kotlin.Boolean)(offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, useUtcIndicator: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, isShort: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, ignoreSeconds: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Returns the ISO 8601 extended time zone string for the given offset. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#formatOffsetLocalizedGMT(kotlin.Int)(offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the localized GMT(UTC) offset format for the given offset. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#formatOffsetShortLocalizedGMT(kotlin.Int)(offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the short localized GMT(UTC) offset format for the given offset. |
| --- | --- |
| open [AttributedCharacterIterator](https://developer.android.com/reference/kotlin/java/text/AttributedCharacterIterator.html#)! | `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#formatToCharacterIterator(kotlin.Any)(obj: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!)` Formats an Object producing an `AttributedCharacterIterator`. |
| open [TimeZoneFormat](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#)! | `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#freeze()()` Freezes the object. |
| open [EnumSet](https://developer.android.com/reference/kotlin/java/util/EnumSet.html#)\< [TimeZoneFormat.ParseOption](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat.ParseOption)!\>! | `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#getDefaultParseOptions()()` Returns the default parse options used by this `TimeZoneFormat` instance. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#getGMTOffsetDigits()()` Returns the decimal digit characters used for localized GMT format in a single string containing from 0 to 9 in the ascending order. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#getGMTOffsetPattern(android.icu.text.TimeZoneFormat.GMTOffsetPatternType)(type: https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat.GMTOffsetPatternType!)` Returns the offset pattern used for localized GMT format. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#getGMTPattern()()` Returns the localized GMT format pattern. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#getGMTZeroFormat()()` Returns the localized GMT format string for GMT(UTC) itself (GMT offset is 0). |
| open static [TimeZoneFormat](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#)! | `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#getInstance(android.icu.util.ULocale)(locale: https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#!)` Returns a frozen instance of `TimeZoneFormat` for the given locale. |
| open static [TimeZoneFormat](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#)! | `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#getInstance(java.util.Locale)(locale: https://developer.android.com/reference/kotlin/java/util/Locale.html#!)` Returns a frozen instance of `TimeZoneFormat` for the given `https://developer.android.com/reference/kotlin/java/util/Locale.html#`. |
| --- | --- |
| open [TimeZoneNames](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneNames)! | `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#getTimeZoneNames()()` Returns the time zone display name data used by this instance. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#isFrozen()()` Determines whether the object has been frozen or not. |
| open [TimeZone](https://developer.android.com/reference/kotlin/android/icu/util/TimeZone.html#)! | `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#parse(android.icu.text.TimeZoneFormat.Style,%20kotlin.String,%20java.text.ParsePosition,%20android.icu.util.Output)(style: https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat.Style!, text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, pos: https://developer.android.com/reference/kotlin/java/text/ParsePosition.html#!, timeType: https://developer.android.com/reference/kotlin/android/icu/util/Output.html#<https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat.TimeType!>!)` Returns a `TimeZone` by parsing the time zone string according to the parse position, the style and the default parse options. |
| --- | --- |
| open [TimeZone](https://developer.android.com/reference/kotlin/android/icu/util/TimeZone.html#)! | `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#parse(android.icu.text.TimeZoneFormat.Style,%20kotlin.String,%20java.text.ParsePosition,%20java.util.EnumSet,%20android.icu.util.Output)(style: https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat.Style!, text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, pos: https://developer.android.com/reference/kotlin/java/text/ParsePosition.html#!, options: https://developer.android.com/reference/kotlin/java/util/EnumSet.html#<https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat.ParseOption!>!, timeType: https://developer.android.com/reference/kotlin/android/icu/util/Output.html#<https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat.TimeType!>!)` Returns a `TimeZone` by parsing the time zone string according to the parse position, the style and the parse options. |
| [TimeZone](https://developer.android.com/reference/kotlin/android/icu/util/TimeZone.html#)! | `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#parse(kotlin.String)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Returns a `TimeZone` for the given text. |
| [TimeZone](https://developer.android.com/reference/kotlin/android/icu/util/TimeZone.html#)! | `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#parse(kotlin.String,%20java.text.ParsePosition)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, pos: https://developer.android.com/reference/kotlin/java/text/ParsePosition.html#!)` Returns a `TimeZone` by parsing the time zone string according to the given parse position. |
| --- | --- |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#parseObject(kotlin.String,%20java.text.ParsePosition)(source: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, pos: https://developer.android.com/reference/kotlin/java/text/ParsePosition.html#!)` Parses text from a string to produce an object. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#parseOffsetISO8601(kotlin.String,%20java.text.ParsePosition)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, pos: https://developer.android.com/reference/kotlin/java/text/ParsePosition.html#!)` Returns offset from GMT(UTC) in milliseconds for the given ISO 8601 basic or extended time zone string. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#parseOffsetLocalizedGMT(kotlin.String,%20java.text.ParsePosition)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, pos: https://developer.android.com/reference/kotlin/java/text/ParsePosition.html#!)` Returns offset from GMT(UTC) in milliseconds for the given localized GMT offset format string. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#parseOffsetShortLocalizedGMT(kotlin.String,%20java.text.ParsePosition)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, pos: https://developer.android.com/reference/kotlin/java/text/ParsePosition.html#!)` Returns offset from GMT(UTC) in milliseconds for the given short localized GMT offset format string. |
| open [TimeZoneFormat](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#)! | `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#setDefaultParseOptions(java.util.EnumSet)(options: https://developer.android.com/reference/kotlin/java/util/EnumSet.html#<https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat.ParseOption!>!)` Sets the default parse options. |
| open [TimeZoneFormat](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#)! | `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#setGMTOffsetDigits(kotlin.String)(digits: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Sets the decimal digit characters used for localized GMT format. |
| --- | --- |
| open [TimeZoneFormat](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#)! | `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#setGMTOffsetPattern(android.icu.text.TimeZoneFormat.GMTOffsetPatternType,%20kotlin.String)(type: https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat.GMTOffsetPatternType!, pattern: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Sets the offset pattern for the given offset type. |
| open [TimeZoneFormat](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#)! | `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#setGMTPattern(kotlin.String)(pattern: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Sets the localized GMT format pattern. |
| open [TimeZoneFormat](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#)! | `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#setGMTZeroFormat(kotlin.String)(gmtZeroFormat: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Sets the localized GMT format string for GMT(UTC) itself (GMT offset is 0). |
| --- | --- |
| open [TimeZoneFormat](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#)! | `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#setTimeZoneNames(android.icu.text.TimeZoneNames)(tznames: https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneNames!)` Sets the time zone display name data to this instance. |

## Protected constructors

### TimeZoneFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected TimeZoneFormat(locale: ULocale!)
```

The protected constructor for subclassing.

| Parameters ||
|---|---|
| `locale` | [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!: the locale |

## Public methods

### clone

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clone(): Any
```

Creates and returns a copy of this object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html` | a clone of this instance. |

| Exceptions ||
|---|---|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the `Cloneable` interface. Subclasses that override the `clone` method can also throw this exception to indicate that an instance cannot be cloned. |

### cloneAsThawed

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun cloneAsThawed(): TimeZoneFormat!
```

Provides for the clone operation. Any clone is initially unfrozen.

### format

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun format(
    style: TimeZoneFormat.Style!, 
    tz: TimeZone!, 
    date: Long
): String!
```

Returns the display name of the time zone at the given date for the style.

**Note** : A style may have fallback styles defined. For example, when `GENERIC_LONG` is requested, but there is no display name data available for `GENERIC_LONG` style, the implementation may use `GENERIC_LOCATION` or `LOCALIZED_GMT`. See UTS#35 UNICODE LOCALE DATA MARKUP LANGUAGE (LDML) [Appendix J: Time Zone Display Name](http://www.unicode.org/reports/tr35/#Time_Zone_Fallback) for the details.

| Parameters ||
|---|---|
| `style` | [TimeZoneFormat.Style](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat.Style)!: the style enum (e.g. `GENERIC_LONG`, `LOCALIZED_GMT`...) |
| `tz` | [TimeZone](https://developer.android.com/reference/kotlin/android/icu/util/TimeZone.html#)!: the time zone. |
| `date` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the date. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the display name of the time zone. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat.Style`
- `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#format(android.icu.text.TimeZoneFormat.Style,%20android.icu.util.TimeZone,%20kotlin.Long,%20android.icu.util.Output)`

### format

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun format(
    style: TimeZoneFormat.Style!, 
    tz: TimeZone!, 
    date: Long, 
    timeType: Output<TimeZoneFormat.TimeType!>!
): String!
```

Returns the display name of the time zone at the given date for the style. This method takes an extra argument `Output<TimeType> timeType` in addition to the argument list of `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#format(android.icu.text.TimeZoneFormat.Style,%20android.icu.util.TimeZone,%20kotlin.Long)`. The argument is used for receiving the time type (standard time or daylight saving time, or unknown) actually used for the display name.

| Parameters ||
|---|---|
| `style` | [TimeZoneFormat.Style](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat.Style)!: the style enum (e.g. `GENERIC_LONG`, `LOCALIZED_GMT`...) |
| `tz` | [TimeZone](https://developer.android.com/reference/kotlin/android/icu/util/TimeZone.html#)!: the time zone. |
| `date` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the date. |
| --- | --- |
| `timeType` | [Output](https://developer.android.com/reference/kotlin/android/icu/util/Output.html#)\< [TimeZoneFormat.TimeType](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat.TimeType)!\>!: the output argument for receiving the time type (standard/daylight/unknown) used for the display name, or specify null if the information is not necessary. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the display name of the time zone. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat.Style`
- `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#format(android.icu.text.TimeZoneFormat.Style,%20android.icu.util.TimeZone,%20kotlin.Long)`

### format

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun format(
    obj: Any!, 
    toAppendTo: StringBuffer!, 
    pos: FieldPosition!
): StringBuffer!
```

Formats an object and appends the resulting text to a given string buffer. If the `pos` argument identifies a field used by the format, then its indices are set to the beginning and end of the first such field encountered.

| Parameters ||
|---|---|
| `obj` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: The object to format |
| `toAppendTo` | [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#)!: where the text is to be appended |
| `pos` | [FieldPosition](https://developer.android.com/reference/kotlin/java/text/FieldPosition.html#)!: A `FieldPosition` identifying a field in the formatted text |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#!` | the string buffer passed in as `toAppendTo`, with formatted text appended |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the Format cannot format the given object |
| `java.lang.NullPointerException` | if `toAppendTo` or `pos` is null |

### formatOffsetISO8601Basic

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun formatOffsetISO8601Basic(
    offset: Int, 
    useUtcIndicator: Boolean, 
    isShort: Boolean, 
    ignoreSeconds: Boolean
): String!
```

Returns the ISO 8601 basic time zone string for the given offset. For example, "-08", "-0830" and "Z"

| Parameters ||
|---|---|
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the offset from GMT(UTC) in milliseconds. |
| `useUtcIndicator` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true if ISO 8601 UTC indicator "Z" is used when the offset is 0. |
| `isShort` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true if shortest form is used. |
| --- | --- |
| `ignoreSeconds` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true if non-zero offset seconds is appended. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the ISO 8601 basic format. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the specified offset is out of supported range (-24 hours \< offset \< +24 hours). |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#formatOffsetISO8601Extended(kotlin.Int,%20kotlin.Boolean,%20kotlin.Boolean,%20kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#parseOffsetISO8601(kotlin.String,%20java.text.ParsePosition)`

### formatOffsetISO8601Extended

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun formatOffsetISO8601Extended(
    offset: Int, 
    useUtcIndicator: Boolean, 
    isShort: Boolean, 
    ignoreSeconds: Boolean
): String!
```

Returns the ISO 8601 extended time zone string for the given offset. For example, "-08:00", "-08:30" and "Z"

| Parameters ||
|---|---|
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the offset from GMT(UTC) in milliseconds. |
| `useUtcIndicator` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true if ISO 8601 UTC indicator "Z" is used when the offset is 0. |
| `isShort` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true if shortest form is used. |
| --- | --- |
| `ignoreSeconds` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true if non-zero offset seconds is appended. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the ISO 8601 extended format. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the specified offset is out of supported range (-24 hours \< offset \< +24 hours). |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#formatOffsetISO8601Basic(kotlin.Int,%20kotlin.Boolean,%20kotlin.Boolean,%20kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#parseOffsetISO8601(kotlin.String,%20java.text.ParsePosition)`

### formatOffsetLocalizedGMT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun formatOffsetLocalizedGMT(offset: Int): String!
```

Returns the localized GMT(UTC) offset format for the given offset. The localized GMT offset is defined by;

- GMT format pattern (e.g. "GMT {0}" - see `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#getGMTPattern()`)
- Offset time pattern (e.g. "+HH:mm" - see `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#getGMTOffsetPattern(android.icu.text.TimeZoneFormat.GMTOffsetPatternType)`)
- Offset digits (e.g. "0123456789" - see `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#getGMTOffsetDigits()`)
- GMT zero format (e.g. "GMT" - see `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#getGMTZeroFormat()`)

This format always uses 2 digit hours and minutes. When the given offset has non-zero seconds, 2 digit seconds field will be appended. For example, GMT+05:00 and GMT+05:28:06.

<br />

| Parameters ||
|---|---|
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the offset from GMT(UTC) in milliseconds. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the localized GMT format string |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the specified offset is out of supported range (-24 hours \< offset \< +24 hours). |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#parseOffsetLocalizedGMT(kotlin.String,%20java.text.ParsePosition)`

### formatOffsetShortLocalizedGMT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun formatOffsetShortLocalizedGMT(offset: Int): String!
```

Returns the short localized GMT(UTC) offset format for the given offset. The short localized GMT offset is defined by;

- GMT format pattern (e.g. "GMT {0}" - see `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#getGMTPattern()`)
- Offset time pattern (e.g. "+HH:mm" - see `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#getGMTOffsetPattern(android.icu.text.TimeZoneFormat.GMTOffsetPatternType)`)
- Offset digits (e.g. "0123456789" - see `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#getGMTOffsetDigits()`)
- GMT zero format (e.g. "GMT" - see `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#getGMTZeroFormat()`)

This format uses the shortest representation of offset. The hours field does not have leading zero and lower fields with zero will be truncated. For example, GMT+5 and GMT+530.

<br />

| Parameters ||
|---|---|
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the offset from GMT(UTC) in milliseconds. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the short localized GMT format string |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the specified offset is out of supported range (-24 hours \< offset \< +24 hours). |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#parseOffsetLocalizedGMT(kotlin.String,%20java.text.ParsePosition)`

### formatToCharacterIterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun formatToCharacterIterator(obj: Any!): AttributedCharacterIterator!
```

Formats an Object producing an `AttributedCharacterIterator`. You can use the returned `AttributedCharacterIterator` to build the resulting String, as well as to determine information about the resulting String.

Each attribute key of the AttributedCharacterIterator will be of type `Field`. It is up to each `Format` implementation to define what the legal values are for each attribute in the `AttributedCharacterIterator`, but typically the attribute key is also used as the attribute value.

The default implementation creates an `AttributedCharacterIterator` with no attributes. Subclasses that support fields should override this and create an `AttributedCharacterIterator` with meaningful attributes.

| Parameters ||
|---|---|
| `obj` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: The object to format |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/text/AttributedCharacterIterator.html#!` | AttributedCharacterIterator describing the formatted value. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | when the Format cannot format the given object. |
| `java.lang.NullPointerException` | if obj is null. |

### freeze

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun freeze(): TimeZoneFormat!
```

Freezes the object.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#!` | the object itself. |

### getDefaultParseOptions

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDefaultParseOptions(): EnumSet<TimeZoneFormat.ParseOption!>!
```

Returns the default parse options used by this `TimeZoneFormat` instance.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/EnumSet.html#<https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat.ParseOption!>!` | the default parse options. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat.ParseOption`

### getGMTOffsetDigits

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getGMTOffsetDigits(): String!
```

Returns the decimal digit characters used for localized GMT format in a single string containing from 0 to 9 in the ascending order.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the decimal digits for localized GMT format. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#setGMTOffsetDigits(kotlin.String)`

### getGMTOffsetPattern

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getGMTOffsetPattern(type: TimeZoneFormat.GMTOffsetPatternType!): String!
```

Returns the offset pattern used for localized GMT format.

| Parameters ||
|---|---|
| `type` | [TimeZoneFormat.GMTOffsetPatternType](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat.GMTOffsetPatternType)!: the offset pattern enum |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#setGMTOffsetPattern(android.icu.text.TimeZoneFormat.GMTOffsetPatternType,%20kotlin.String)`

### getGMTPattern

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getGMTPattern(): String!
```

Returns the localized GMT format pattern.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the localized GMT format pattern. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#setGMTPattern(kotlin.String)`

### getGMTZeroFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getGMTZeroFormat(): String!
```

Returns the localized GMT format string for GMT(UTC) itself (GMT offset is 0).

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the localized GMT string string for GMT(UTC) itself. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#setGMTZeroFormat(kotlin.String)`

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getInstance(locale: ULocale!): TimeZoneFormat!
```

Returns a frozen instance of `TimeZoneFormat` for the given locale.

**Note** : The instance returned by this method is frozen. If you want to customize a TimeZoneFormat, you must use `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#cloneAsThawed()` to get a thawed copy first.

| Parameters ||
|---|---|
| `locale` | [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!: the locale. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#!` | a frozen instance of `TimeZoneFormat` for the given locale. |

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getInstance(locale: Locale!): TimeZoneFormat!
```

Returns a frozen instance of `TimeZoneFormat` for the given `https://developer.android.com/reference/kotlin/java/util/Locale.html#`.

**Note** : The instance returned by this method is frozen. If you want to customize a TimeZoneFormat, you must use `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#cloneAsThawed()` to get a thawed copy first.

| Parameters ||
|---|---|
| `locale` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!: the `https://developer.android.com/reference/kotlin/java/util/Locale.html#`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#!` | a frozen instance of `TimeZoneFormat` for the given locale. |

### getTimeZoneNames

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTimeZoneNames(): TimeZoneNames!
```

Returns the time zone display name data used by this instance.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneNames!` | the time zone display name data. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#setTimeZoneNames(android.icu.text.TimeZoneNames)`

### isFrozen

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isFrozen(): Boolean
```

Determines whether the object has been frozen or not.

### parse

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun parse(
    style: TimeZoneFormat.Style!, 
    text: String!, 
    pos: ParsePosition!, 
    timeType: Output<TimeZoneFormat.TimeType!>!
): TimeZone!
```

Returns a `TimeZone` by parsing the time zone string according to the parse position, the style and the default parse options.

**Note** : This method is equivalent to `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#parse(android.icu.text.TimeZoneFormat.Style,%20kotlin.String,%20java.text.ParsePosition,%20java.util.EnumSet,%20android.icu.util.Output)`.

| Parameters ||
|---|---|
| `style` | [TimeZoneFormat.Style](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat.Style)!: the format style |
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the text contains a time zone string at the position. |
| `pos` | [ParsePosition](https://developer.android.com/reference/kotlin/java/text/ParsePosition.html#)!: the position. |
| --- | --- |
| `timeType` | [Output](https://developer.android.com/reference/kotlin/android/icu/util/Output.html#)\< [TimeZoneFormat.TimeType](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat.TimeType)!\>!: The output argument for receiving the time type (standard/daylight/unknown), or specify null if the information is not necessary. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/util/TimeZone.html#!` | A `TimeZone`, or null if the input could not be parsed. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat.Style`
- `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#parse(android.icu.text.TimeZoneFormat.Style,%20kotlin.String,%20java.text.ParsePosition,%20java.util.EnumSet,%20android.icu.util.Output)`
- `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#format(android.icu.text.TimeZoneFormat.Style,%20android.icu.util.TimeZone,%20kotlin.Long,%20android.icu.util.Output)`
- `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#setDefaultParseOptions(java.util.EnumSet)`

### parse

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun parse(
    style: TimeZoneFormat.Style!, 
    text: String!, 
    pos: ParsePosition!, 
    options: EnumSet<TimeZoneFormat.ParseOption!>!, 
    timeType: Output<TimeZoneFormat.TimeType!>!
): TimeZone!
```

Returns a `TimeZone` by parsing the time zone string according to the parse position, the style and the parse options.

| Parameters ||
|---|---|
| `style` | [TimeZoneFormat.Style](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat.Style)!: the format style. |
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the text contains a time zone string at the position. |
| `pos` | [ParsePosition](https://developer.android.com/reference/kotlin/java/text/ParsePosition.html#)!: the position. |
| --- | --- |
| `options` | [EnumSet](https://developer.android.com/reference/kotlin/java/util/EnumSet.html#)\< [TimeZoneFormat.ParseOption](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat.ParseOption)!\>!: the parse options. |
| `timeType` | [Output](https://developer.android.com/reference/kotlin/android/icu/util/Output.html#)\< [TimeZoneFormat.TimeType](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat.TimeType)!\>!: The output argument for receiving the time type (standard/daylight/unknown), or specify null if the information is not necessary. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/util/TimeZone.html#!` | A `TimeZone`, or null if the input could not be parsed. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat.Style`
- `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#format(android.icu.text.TimeZoneFormat.Style,%20android.icu.util.TimeZone,%20kotlin.Long,%20android.icu.util.Output)`

### parse

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun parse(text: String!): TimeZone!
```

Returns a `TimeZone` for the given text.

**Note** : The behavior of this method is equivalent to `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#parse(kotlin.String,%20java.text.ParsePosition)`.

| Parameters ||
|---|---|
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the time zone string |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/util/TimeZone.html#!` | A `TimeZone`. |

| Exceptions ||
|---|---|
| `java.text.ParseException` | when the input could not be parsed as a time zone string. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#parse(kotlin.String,%20java.text.ParsePosition)`

### parse

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun parse(
    text: String!, 
    pos: ParsePosition!
): TimeZone!
```

Returns a `TimeZone` by parsing the time zone string according to the given parse position.

**Note** : This method is equivalent to `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#parse(android.icu.text.TimeZoneFormat.Style,%20kotlin.String,%20java.text.ParsePosition,%20java.util.EnumSet,%20android.icu.util.Output)`.

| Parameters ||
|---|---|
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the text contains a time zone string at the position. |
| `pos` | [ParsePosition](https://developer.android.com/reference/kotlin/java/text/ParsePosition.html#)!: the position. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/util/TimeZone.html#!` | A `TimeZone`, or null if the input could not be parsed. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#parse(android.icu.text.TimeZoneFormat.Style,%20kotlin.String,%20java.text.ParsePosition,%20java.util.EnumSet,%20android.icu.util.Output)`

### parseObject

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun parseObject(
    source: String!, 
    pos: ParsePosition!
): Any!
```

Parses text from a string to produce an object.

The method attempts to parse text starting at the index given by `pos`. If parsing succeeds, then the index of `pos` is updated to the index after the last character used (parsing does not necessarily use all characters up to the end of the string), and the parsed object is returned. The updated `pos` can be used to indicate the starting point for the next call to this method. If an error occurs, then the index of `pos` is not changed, the error index of `pos` is set to the index of the character where the error occurred, and null is returned.

| Parameters ||
|---|---|
| `source` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: A `String`, part of which should be parsed. |
| `pos` | [ParsePosition](https://developer.android.com/reference/kotlin/java/text/ParsePosition.html#)!: A `ParsePosition` object with index and error index information as described above. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!` | An `Object` parsed from the string. In case of error, returns null. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if `source` or `pos` is null. |

### parseOffsetISO8601

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun parseOffsetISO8601(
    text: String!, 
    pos: ParsePosition!
): Int
```

Returns offset from GMT(UTC) in milliseconds for the given ISO 8601 basic or extended time zone string. When the given string is not an ISO 8601 time zone string, this method sets the current position as the error index to `ParsePosition pos` and returns 0.

| Parameters ||
|---|---|
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the text contains ISO 8601 style time zone string (e.g. "-08", "-0800", "-08:00", and "Z") at the position. |
| `pos` | [ParsePosition](https://developer.android.com/reference/kotlin/java/text/ParsePosition.html#)!: the position. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the offset from GMT(UTC) in milliseconds for the given ISO 8601 style time zone string. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#formatOffsetISO8601Basic(kotlin.Int,%20kotlin.Boolean,%20kotlin.Boolean,%20kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#formatOffsetISO8601Extended(kotlin.Int,%20kotlin.Boolean,%20kotlin.Boolean,%20kotlin.Boolean)`

### parseOffsetLocalizedGMT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun parseOffsetLocalizedGMT(
    text: String!, 
    pos: ParsePosition!
): Int
```

Returns offset from GMT(UTC) in milliseconds for the given localized GMT offset format string. When the given string cannot be parsed, this method sets the current position as the error index to `ParsePosition pos` and returns 0.

| Parameters ||
|---|---|
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the text contains a localized GMT offset string at the position. |
| `pos` | [ParsePosition](https://developer.android.com/reference/kotlin/java/text/ParsePosition.html#)!: the position. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the offset from GMT(UTC) in milliseconds for the given localized GMT offset format string. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#formatOffsetLocalizedGMT(kotlin.Int)`

### parseOffsetShortLocalizedGMT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun parseOffsetShortLocalizedGMT(
    text: String!, 
    pos: ParsePosition!
): Int
```

Returns offset from GMT(UTC) in milliseconds for the given short localized GMT offset format string. When the given string cannot be parsed, this method sets the current position as the error index to `ParsePosition pos` and returns 0.

| Parameters ||
|---|---|
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the text contains a short localized GMT offset string at the position. |
| `pos` | [ParsePosition](https://developer.android.com/reference/kotlin/java/text/ParsePosition.html#)!: the position. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the offset from GMT(UTC) in milliseconds for the given short localized GMT offset format string. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#formatOffsetShortLocalizedGMT(kotlin.Int)`

### setDefaultParseOptions

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setDefaultParseOptions(options: EnumSet<TimeZoneFormat.ParseOption!>!): TimeZoneFormat!
```

Sets the default parse options.

**Note:** By default, an instance of `TimeZoneFormat` created by `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#getInstance(android.icu.util.ULocale)` has no parse options set.

| Parameters ||
|---|---|
| `options` | [EnumSet](https://developer.android.com/reference/kotlin/java/util/EnumSet.html#)\< [TimeZoneFormat.ParseOption](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat.ParseOption)!\>!: the default parse options. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#!` | this object. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat.ParseOption`

### setGMTOffsetDigits

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setGMTOffsetDigits(digits: String!): TimeZoneFormat!
```

Sets the decimal digit characters used for localized GMT format.

| Parameters ||
|---|---|
| `digits` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: a string contains the decimal digit characters from 0 to 9 n the ascending order. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#!` | this object. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | when the string did not contain ten characters. |
| `java.lang.UnsupportedOperationException` | when this object is frozen. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#getGMTOffsetDigits()`

### setGMTOffsetPattern

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setGMTOffsetPattern(
    type: TimeZoneFormat.GMTOffsetPatternType!, 
    pattern: String!
): TimeZoneFormat!
```

Sets the offset pattern for the given offset type.

| Parameters ||
|---|---|
| `type` | [TimeZoneFormat.GMTOffsetPatternType](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat.GMTOffsetPatternType)!: the offset pattern. |
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the pattern string. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#!` | this object. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | when the pattern string does not have required time field letters. |
| `java.lang.UnsupportedOperationException` | when this object is frozen. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#getGMTOffsetPattern(android.icu.text.TimeZoneFormat.GMTOffsetPatternType)`

### setGMTPattern

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setGMTPattern(pattern: String!): TimeZoneFormat!
```

Sets the localized GMT format pattern. The pattern must contain a single argument {0}, for example "GMT {0}".

| Parameters ||
|---|---|
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the localized GMT format pattern string |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#!` | this object. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | when the pattern string does not contain "{0}" |
| `java.lang.UnsupportedOperationException` | when this object is frozen. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#getGMTPattern()`

### setGMTZeroFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setGMTZeroFormat(gmtZeroFormat: String!): TimeZoneFormat!
```

Sets the localized GMT format string for GMT(UTC) itself (GMT offset is 0).

| Parameters ||
|---|---|
| `gmtZeroFormat` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the localized GMT format string for GMT(UTC). |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#!` | this object. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | when this object is frozen. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#getGMTZeroFormat()`

### setTimeZoneNames

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTimeZoneNames(tznames: TimeZoneNames!): TimeZoneFormat!
```

Sets the time zone display name data to this instance.

| Parameters ||
|---|---|
| `tznames` | [TimeZoneNames](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneNames)!: the time zone display name data. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#!` | this object. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | when this object is frozen. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat#getTimeZoneNames()`
