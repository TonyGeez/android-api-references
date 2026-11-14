Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TtsSpan

Kotlin | [Java](TtsSpan.md)
| --- | --- |

```
open class TtsSpan : ParcelableSpan
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.text.style.TtsSpan](TtsSpan.md) |

A span that supplies additional meta-data for the associated text intended for text-to-speech engines. If the text is being processed by a text-to-speech engine, the engine may use the data in this span in addition to or instead of its associated text. Each instance of a TtsSpan has a type, for example `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_DATE:kotlin.String` or `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_MEASURE:kotlin.String`. And a list of arguments, provided as key-value pairs in a bundle. The inner classes are there for convenience and provide builders for each TtsSpan type.

## Summary

| Nested classes ||
|---|---|
| open | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan.Builder` A simple builder for TtsSpans. |
| open | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan.CardinalBuilder` A builder for TtsSpans of type `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_CARDINAL:kotlin.String`. |
| open | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan.DateBuilder` A builder for TtsSpans of type `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_DATE:kotlin.String`. |
| --- | --- |
| open | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan.DecimalBuilder` A builder for TtsSpans of type `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_DECIMAL:kotlin.String`. |
| open | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan.DigitsBuilder` A builder for TtsSpans of type `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_DIGITS:kotlin.String`. |
| open | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan.DurationBuilder` A builder for TtsSpans of type `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_DURATION:kotlin.String`. |
| --- | --- |
| open | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan.ElectronicBuilder` A builder for TtsSpans of type `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_ELECTRONIC:kotlin.String`. |
| open | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan.FractionBuilder` A builder for TtsSpans of type `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_FRACTION:kotlin.String`. |
| open | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan.MeasureBuilder` A builder for TtsSpans of type `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_MEASURE:kotlin.String`. |
| --- | --- |
| open | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan.MoneyBuilder` A builder for TtsSpans of type `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_MONEY:kotlin.String`. |
| open | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan.OrdinalBuilder` A builder for TtsSpans of type `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_ORDINAL:kotlin.String`. |
| open | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan.SemioticClassBuilder` A builder for TtsSpans, has setters for morphosyntactic features. |
| --- | --- |
| open | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan.TelephoneBuilder` A builder for TtsSpans of type `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_TELEPHONE:kotlin.String`. |
| open | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan.TextBuilder` A builder for TtsSpans of type `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_TEXT:kotlin.String`. |
| open | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan.TimeBuilder` A builder for TtsSpans of type `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_TIME:kotlin.String`. |
| --- | --- |
| open | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan.VerbatimBuilder` A builder for TtsSpans of type `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_VERBATIM:kotlin.String`. |

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ANIMACY_ANIMATE:kotlin.String` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ANIMACY_INANIMATE:kotlin.String` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_ANIMACY:kotlin.String` String argument supplying animacy information. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_CASE:kotlin.String` String argument supplying case information. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_COUNTRY_CODE:kotlin.String` Argument used to specify the country code of a telephone number. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_CURRENCY:kotlin.String` Argument used to specify the currency. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_DAY:kotlin.String` Argument used to specify the day of the month of a date. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_DENOMINATOR:kotlin.String` Argument used to specify the denominator of a fraction. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_DIGITS:kotlin.String` Argument used to specify a string of digits. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_DOMAIN:kotlin.String` Argument used to specify the domain part of a URI. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_EXTENSION:kotlin.String` Argument used to specify the extension part of a telephone number. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_FRACTIONAL_PART:kotlin.String` Argument used to specify the fractional part of a decimal. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_FRAGMENT_ID:kotlin.String` Argument used to specify the fragment id of a URI. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_GENDER:kotlin.String` String argument supplying gender information. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_HOURS:kotlin.String` Argument used to specify the hours of a time or duration. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_INTEGER_PART:kotlin.String` Argument used to specify the integer part of a decimal or fraction. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_MINUTES:kotlin.String` Argument used to specify the minutes of a time or duration. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_MONTH:kotlin.String` Argument used to specify the month of a date. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_MULTIPLICITY:kotlin.String` String argument supplying multiplicity information. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_NUMBER:kotlin.String` Argument used to specify a whole number. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_NUMBER_PARTS:kotlin.String` Argument used to specify the main number part of a telephone number. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_NUMERATOR:kotlin.String` Argument used to specify the numerator of a fraction. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_PASSWORD:kotlin.String` Argument used to specify the password part of a URI. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_PATH:kotlin.String` Argument used to specify the path part of a URI. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_PORT:kotlin.String` Argument used to specify the port number of a URI. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_PROTOCOL:kotlin.String` Argument used to specify the protocol of a URI. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_QUANTITY:kotlin.String` Argument used to choose the suffix (thousand, million, etc) that is used to pronounce large amounts of money. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_QUERY_STRING:kotlin.String` Argument used to specify the query string of a URI. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_SECONDS:kotlin.String` Argument used to specify the seconds of a time or duration. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_TEXT:kotlin.String` String supplying the text to be synthesized. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_UNIT:kotlin.String` Argument used to specify the unit of a measure. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_USERNAME:kotlin.String` Argument used to specify the username part of a URI. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_VERBATIM:kotlin.String` Argument used to specify a string where the characters are read verbatim, except whitespace. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_WEEKDAY:kotlin.String` Argument used to specify the weekday of a date. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_YEAR:kotlin.String` Argument used to specify the year of a date. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#CASE_ABLATIVE:kotlin.String` <br /> |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#CASE_ACCUSATIVE:kotlin.String` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#CASE_DATIVE:kotlin.String` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#CASE_GENITIVE:kotlin.String` <br /> |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#CASE_INSTRUMENTAL:kotlin.String` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#CASE_LOCATIVE:kotlin.String` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#CASE_NOMINATIVE:kotlin.String` <br /> |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#CASE_VOCATIVE:kotlin.String` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#GENDER_FEMALE:kotlin.String` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#GENDER_MALE:kotlin.String` <br /> |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#GENDER_NEUTRAL:kotlin.String` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#MONTH_APRIL:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#MONTH_AUGUST:kotlin.Int` <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#MONTH_DECEMBER:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#MONTH_FEBRUARY:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#MONTH_JANUARY:kotlin.Int` <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#MONTH_JULY:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#MONTH_JUNE:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#MONTH_MARCH:kotlin.Int` <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#MONTH_MAY:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#MONTH_NOVEMBER:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#MONTH_OCTOBER:kotlin.Int` <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#MONTH_SEPTEMBER:kotlin.Int` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#MULTIPLICITY_DUAL:kotlin.String` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#MULTIPLICITY_PLURAL:kotlin.String` <br /> |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#MULTIPLICITY_SINGLE:kotlin.String` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_CARDINAL:kotlin.String` The text associated with this span is a cardinal. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_DATE:kotlin.String` The text associated with this span is a date. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_DECIMAL:kotlin.String` The text associated with this span is a decimal number. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_DIGITS:kotlin.String` The text associated with this span is a series of digits that have to be read sequentially. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_DURATION:kotlin.String` The text associated with this span is a duration, consisting of a number of hours, minutes, and seconds specified with `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_HOURS:kotlin.String`, `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_MINUTES:kotlin.String`, and `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_SECONDS:kotlin.String`. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_ELECTRONIC:kotlin.String` The text associated with this span is a URI (can be used for URLs and email addresses). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_FRACTION:kotlin.String` The text associated with this span is a fractional number. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_MEASURE:kotlin.String` The text associated with this span is a measure, consisting of a number and a unit. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_MONEY:kotlin.String` The text associated with this span is an amount of money. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_ORDINAL:kotlin.String` The text associated with this span is an ordinal. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_TELEPHONE:kotlin.String` The text associated with this span is a telephone number. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_TEXT:kotlin.String` This span type can be used to add morphosyntactic features to the text it spans over, or synthesize a something else than the spanned text. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_TIME:kotlin.String` The text associated with this span is a time, consisting of a number of hours, minutes, and seconds specified with `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_HOURS:kotlin.String`, `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_MINUTES:kotlin.String`, and `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_SECONDS:kotlin.String`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_VERBATIM:kotlin.String` The text associated with this span is a series of characters that have to be read verbatim. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#WEEKDAY_FRIDAY:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#WEEKDAY_MONDAY:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#WEEKDAY_SATURDAY:kotlin.Int` <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#WEEKDAY_SUNDAY:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#WEEKDAY_THURSDAY:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#WEEKDAY_TUESDAY:kotlin.Int` <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#WEEKDAY_WEDNESDAY:kotlin.Int` <br /> |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TtsSpan(android.os.Parcel)(src: https://developer.android.com/reference/kotlin/android/os/Parcel.html#!)` <br /> |
| `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TtsSpan(kotlin.String,%20android.os.PersistableBundle)(type: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, args: https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#!)` <br /> |

| Public methods ||
|---|---|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| open [PersistableBundle](../android.os/PersistableBundle.md)! | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#getArgs()()` Returns a bundle of the arguments set. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#getSpanTypeId()()` Return a special type identifier for this span class. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#getType()()` Returns the type. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

## Constants

### ANIMACY_ANIMATE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ANIMACY_ANIMATE: String
```

 Value: "android.animate"

### ANIMACY_INANIMATE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ANIMACY_INANIMATE: String
```

 Value: "android.inanimate"

### ARG_ANIMACY

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ARG_ANIMACY: String
```

String argument supplying animacy information. Can be `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ANIMACY_ANIMATE:kotlin.String` or `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ANIMACY_INANIMATE:kotlin.String`

 Value: "android.arg.animacy"

### ARG_CASE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ARG_CASE: String
```

String argument supplying case information. Can be any of `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#CASE_NOMINATIVE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#CASE_ACCUSATIVE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#CASE_DATIVE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#CASE_ABLATIVE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#CASE_GENITIVE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#CASE_VOCATIVE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#CASE_LOCATIVE:kotlin.String` and `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#CASE_INSTRUMENTAL:kotlin.String`

 Value: "android.arg.case"

### ARG_COUNTRY_CODE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ARG_COUNTRY_CODE: String
```

Argument used to specify the country code of a telephone number. Can be a string of digits optionally prefixed with a "+". Can be used with `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_TELEPHONE:kotlin.String`.

 Value: "android.arg.country_code"

### ARG_CURRENCY

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ARG_CURRENCY: String
```

Argument used to specify the currency. Should be a ISO4217 currency code, e.g. "USD". Can be used with `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_MONEY:kotlin.String`.

 Value: "android.arg.money"

### ARG_DAY

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ARG_DAY: String
```

Argument used to specify the day of the month of a date. The value should be provided as an integer in the range from 1 up to and including 31. Can be used with `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_DATE:kotlin.String`.

 Value: "android.arg.day"

### ARG_DENOMINATOR

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ARG_DENOMINATOR: String
```

Argument used to specify the denominator of a fraction. The value can be a string of digits of any size optionally prefixed with a + or -. Can be used with `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_FRACTION:kotlin.String`.

 Value: "android.arg.denominator"

### ARG_DIGITS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ARG_DIGITS: String
```

Argument used to specify a string of digits. Can be used with `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_DIGITS:kotlin.String`.

 Value: "android.arg.digits"

### ARG_DOMAIN

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ARG_DOMAIN: String
```

Argument used to specify the domain part of a URI. For example "source.android.com". Can be used with `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_ELECTRONIC:kotlin.String`.

 Value: "android.arg.domain"

### ARG_EXTENSION

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ARG_EXTENSION: String
```

Argument used to specify the extension part of a telephone number. Can be a string of digits. Can be used with `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_TELEPHONE:kotlin.String`.

 Value: "android.arg.extension"

### ARG_FRACTIONAL_PART

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ARG_FRACTIONAL_PART: String
```

Argument used to specify the fractional part of a decimal. The value can be a string of digits of any size. Can be used with `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_DECIMAL:kotlin.String`.

 Value: "android.arg.fractional_part"

### ARG_FRAGMENT_ID

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ARG_FRAGMENT_ID: String
```

Argument used to specify the fragment id of a URI. Should be specified as a string. Can be used with `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_ELECTRONIC:kotlin.String`.

 Value: "android.arg.fragment_id"

### ARG_GENDER

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ARG_GENDER: String
```

String argument supplying gender information. Can be any of `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#GENDER_NEUTRAL:kotlin.String`, `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#GENDER_MALE:kotlin.String` and `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#GENDER_FEMALE:kotlin.String`.

 Value: "android.arg.gender"

### ARG_HOURS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ARG_HOURS: String
```

Argument used to specify the hours of a time or duration. The hours should be provided as an integer in the range from 0 up to and including 24 for `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_TIME:kotlin.String`. Can be used with `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_TIME:kotlin.String` or `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_DURATION:kotlin.String`.

 Value: "android.arg.hours"

### ARG_INTEGER_PART

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ARG_INTEGER_PART: String
```

Argument used to specify the integer part of a decimal or fraction. The value can be a string of digits of any size optionally prefixed with a - or +. Can be used with `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_DECIMAL:kotlin.String` and `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_FRACTION:kotlin.String`.

 Value: "android.arg.integer_part"

### ARG_MINUTES

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ARG_MINUTES: String
```

Argument used to specify the minutes of a time or duration. The minutes should be provided as an integer in the range from 0 up to and including 59 for `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_TIME:kotlin.String`. Can be used with `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_TIME:kotlin.String` or `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_DURATION:kotlin.String`.

 Value: "android.arg.minutes"

### ARG_MONTH

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ARG_MONTH: String
```

Argument used to specify the month of a date. The value should be provided as an integer and can be any of `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#MONTH_JANUARY:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#MONTH_FEBRUARY:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#MONTH_MARCH:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#MONTH_APRIL:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#MONTH_MAY:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#MONTH_JUNE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#MONTH_JULY:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#MONTH_AUGUST:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#MONTH_SEPTEMBER:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#MONTH_OCTOBER:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#MONTH_NOVEMBER:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#MONTH_DECEMBER:kotlin.Int`. Can be used with `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_DATE:kotlin.String`.

 Value: "android.arg.month"

### ARG_MULTIPLICITY

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ARG_MULTIPLICITY: String
```

String argument supplying multiplicity information. Can be any of `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#MULTIPLICITY_SINGLE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#MULTIPLICITY_DUAL:kotlin.String` and `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#MULTIPLICITY_PLURAL:kotlin.String`

 Value: "android.arg.multiplicity"

### ARG_NUMBER

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ARG_NUMBER: String
```

Argument used to specify a whole number. The value can be a string of digits of any size optionally prefixed with a - or +. Can be used with `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_CARDINAL:kotlin.String` and `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_ORDINAL:kotlin.String`.

 Value: "android.arg.number"

### ARG_NUMBER_PARTS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ARG_NUMBER_PARTS: String
```

Argument used to specify the main number part of a telephone number. Can be a string of digits where the different parts of the telephone number can be separated with a space, '-', '/' or '.'. Can be used with `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_TELEPHONE:kotlin.String`.

 Value: "android.arg.number_parts"

### ARG_NUMERATOR

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ARG_NUMERATOR: String
```

Argument used to specify the numerator of a fraction. The value can be a string of digits of any size optionally prefixed with a - or +. Can be used with `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_FRACTION:kotlin.String`.

 Value: "android.arg.numerator"

### ARG_PASSWORD

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ARG_PASSWORD: String
```

Argument used to specify the password part of a URI. Should be set as a string. Can be used with `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_ELECTRONIC:kotlin.String`.

 Value: "android.arg.password"

### ARG_PATH

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ARG_PATH: String
```

Argument used to specify the path part of a URI. For example "source/index.html". Can be used with `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_ELECTRONIC:kotlin.String`.

 Value: "android.arg.path"

### ARG_PORT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ARG_PORT: String
```

Argument used to specify the port number of a URI. Should be specified as an integer. Can be used with `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_ELECTRONIC:kotlin.String`.

 Value: "android.arg.port"

### ARG_PROTOCOL

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ARG_PROTOCOL: String
```

Argument used to specify the protocol of a URI. Examples are "http" and "ftp". Can be used with `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_ELECTRONIC:kotlin.String`.

 Value: "android.arg.protocol"

### ARG_QUANTITY

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ARG_QUANTITY: String
```

Argument used to choose the suffix (thousand, million, etc) that is used to pronounce large amounts of money. For example it can be used to disambiguate between "two thousand five hundred dollars" and "two point five thousand dollars". If implemented, engines should support at least "1000", "1000000", "1000000000" and "1000000000000". Example: if the `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_INTEGER_PART:kotlin.String` argument is "10", the `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_FRACTIONAL_PART:kotlin.String` argument is "4", the `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_QUANTITY:kotlin.String` argument is "1000" and the `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_CURRENCY:kotlin.String` argument is "usd", the TTS engine may pronounce the span as "ten point four thousand dollars". With the same example but with the quantity set as "1000000" the TTS engine may pronounce the span as "ten point four million dollars". Can be used with `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_MONEY:kotlin.String`.

 Value: "android.arg.quantity"

### ARG_QUERY_STRING

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ARG_QUERY_STRING: String
```

Argument used to specify the query string of a URI. For example "arg=value\&argtwo=value". Can be used with `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_ELECTRONIC:kotlin.String`.

 Value: "android.arg.query_string"

### ARG_SECONDS

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ARG_SECONDS: String
```

Argument used to specify the seconds of a time or duration. The seconds should be provided as an integer in the range from 0 up to and including 59 for `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_TIME:kotlin.String`. Can be used with `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_TIME:kotlin.String` or `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_DURATION:kotlin.String`.

 Value: "android.arg.seconds"

### ARG_TEXT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ARG_TEXT: String
```

String supplying the text to be synthesized. The synthesizer is free to decide how to interpret the text. Can be used with `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_TEXT:kotlin.String`.

 Value: "android.arg.text"

### ARG_UNIT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ARG_UNIT: String
```

Argument used to specify the unit of a measure. The unit should always be specified in English singular form. Prefixes may be used. Engines will do their best to pronounce them correctly in the language used. Engines are expected to at least support the most common ones like "meter", "second", "degree celsius" and "degree fahrenheit" with some common prefixes like "milli" and "kilo". Can be used with `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_MEASURE:kotlin.String`.

 Value: "android.arg.unit"

### ARG_USERNAME

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ARG_USERNAME: String
```

Argument used to specify the username part of a URI. Should be set as a string. Can be used with `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_ELECTRONIC:kotlin.String`.

 Value: "android.arg.username"

### ARG_VERBATIM

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ARG_VERBATIM: String
```

Argument used to specify a string where the characters are read verbatim, except whitespace. Can be used with `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_VERBATIM:kotlin.String`.

 Value: "android.arg.verbatim"

### ARG_WEEKDAY

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ARG_WEEKDAY: String
```

Argument used to specify the weekday of a date. The value should be provided as an integer and can be any of `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#WEEKDAY_SUNDAY:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#WEEKDAY_MONDAY:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#WEEKDAY_TUESDAY:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#WEEKDAY_WEDNESDAY:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#WEEKDAY_THURSDAY:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#WEEKDAY_FRIDAY:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#WEEKDAY_SATURDAY:kotlin.Int`. Can be used with `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_DATE:kotlin.String`.

 Value: "android.arg.weekday"

### ARG_YEAR

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ARG_YEAR: String
```

Argument used to specify the year of a date. The value should be provided as a positive integer. Can be used with `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_DATE:kotlin.String`.

 Value: "android.arg.year"

### CASE_ABLATIVE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CASE_ABLATIVE: String
```

 Value: "android.ablative"

### CASE_ACCUSATIVE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CASE_ACCUSATIVE: String
```

 Value: "android.accusative"

### CASE_DATIVE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CASE_DATIVE: String
```

 Value: "android.dative"

### CASE_GENITIVE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CASE_GENITIVE: String
```

 Value: "android.genitive"

### CASE_INSTRUMENTAL

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CASE_INSTRUMENTAL: String
```

 Value: "android.instrumental"

### CASE_LOCATIVE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CASE_LOCATIVE: String
```

 Value: "android.locative"

### CASE_NOMINATIVE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CASE_NOMINATIVE: String
```

 Value: "android.nominative"

### CASE_VOCATIVE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CASE_VOCATIVE: String
```

 Value: "android.vocative"

### GENDER_FEMALE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GENDER_FEMALE: String
```

 Value: "android.female"

### GENDER_MALE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GENDER_MALE: String
```

 Value: "android.male"

### GENDER_NEUTRAL

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GENDER_NEUTRAL: String
```

 Value: "android.neutral"

### MONTH_APRIL

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MONTH_APRIL: Int
```

 Value: 3

### MONTH_AUGUST

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MONTH_AUGUST: Int
```

 Value: 7

### MONTH_DECEMBER

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MONTH_DECEMBER: Int
```

 Value: 11

### MONTH_FEBRUARY

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MONTH_FEBRUARY: Int
```

 Value: 1

### MONTH_JANUARY

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MONTH_JANUARY: Int
```

 Value: 0

### MONTH_JULY

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MONTH_JULY: Int
```

 Value: 6

### MONTH_JUNE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MONTH_JUNE: Int
```

 Value: 5

### MONTH_MARCH

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MONTH_MARCH: Int
```

 Value: 2

### MONTH_MAY

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MONTH_MAY: Int
```

 Value: 4

### MONTH_NOVEMBER

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MONTH_NOVEMBER: Int
```

 Value: 10

### MONTH_OCTOBER

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MONTH_OCTOBER: Int
```

 Value: 9

### MONTH_SEPTEMBER

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MONTH_SEPTEMBER: Int
```

 Value: 8

### MULTIPLICITY_DUAL

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MULTIPLICITY_DUAL: String
```

 Value: "android.dual"

### MULTIPLICITY_PLURAL

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MULTIPLICITY_PLURAL: String
```

 Value: "android.plural"

### MULTIPLICITY_SINGLE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MULTIPLICITY_SINGLE: String
```

 Value: "android.single"

### TYPE_CARDINAL

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_CARDINAL: String
```

The text associated with this span is a cardinal. Must include the number to be synthesized with `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_NUMBER:kotlin.String`. Also accepts the arguments `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_GENDER:kotlin.String`, `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_ANIMACY:kotlin.String`, `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_MULTIPLICITY:kotlin.String` and `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_CASE:kotlin.String`.

 Value: "android.type.cardinal"

### TYPE_DATE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_DATE: String
```

The text associated with this span is a date. At least one of the arguments `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_MONTH:kotlin.String` and `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_YEAR:kotlin.String` has to be provided. The argument `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_DAY:kotlin.String` is optional if `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_MONTH:kotlin.String` is set. The argument `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_WEEKDAY:kotlin.String` is optional if `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_DAY:kotlin.String` is set. Also accepts the arguments `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_GENDER:kotlin.String`, `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_ANIMACY:kotlin.String`, `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_MULTIPLICITY:kotlin.String` and `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_CASE:kotlin.String`.

 Value: "android.type.date"

### TYPE_DECIMAL

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_DECIMAL: String
```

The text associated with this span is a decimal number. Must include the number to be synthesized with `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_INTEGER_PART:kotlin.String` and `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_FRACTIONAL_PART:kotlin.String`. Also accepts the arguments `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_GENDER:kotlin.String`, `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_ANIMACY:kotlin.String`, `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_MULTIPLICITY:kotlin.String` and `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_CASE:kotlin.String`.

 Value: "android.type.decimal"

### TYPE_DIGITS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_DIGITS: String
```

The text associated with this span is a series of digits that have to be read sequentially. The digits can be set with `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_DIGITS:kotlin.String`. Also accepts the arguments `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_GENDER:kotlin.String`, `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_ANIMACY:kotlin.String`, `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_MULTIPLICITY:kotlin.String` and `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_CASE:kotlin.String`.

 Value: "android.type.digits"

### TYPE_DURATION

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_DURATION: String
```

The text associated with this span is a duration, consisting of a number of hours, minutes, and seconds specified with `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_HOURS:kotlin.String`, `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_MINUTES:kotlin.String`, and `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_SECONDS:kotlin.String`. This is different from `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_TIME:kotlin.String`. This should be used to convey an interval of time, while `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_TIME:kotlin.String` should be used to convey a particular moment in time, such as a clock time.

 Value: "android.type.duration"

### TYPE_ELECTRONIC

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_ELECTRONIC: String
```

The text associated with this span is a URI (can be used for URLs and email addresses). The full schema for URLs, which email addresses can effectively be seen as a subset of, is: protocol://username:password@domain:port/path?query_string#fragment_id Hence populating just username and domain will read as an email address. All arguments are optional, but at least one has to be provided: `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_PROTOCOL:kotlin.String`, `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_USERNAME:kotlin.String`, `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_PASSWORD:kotlin.String`, `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_DOMAIN:kotlin.String`, `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_PORT:kotlin.String`, `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_PATH:kotlin.String`, `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_QUERY_STRING:kotlin.String` and `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_FRAGMENT_ID:kotlin.String`. Also accepts the arguments `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_GENDER:kotlin.String`, `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_ANIMACY:kotlin.String`, `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_MULTIPLICITY:kotlin.String` and `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_CASE:kotlin.String`.

 Value: "android.type.electronic"

### TYPE_FRACTION

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_FRACTION: String
```

The text associated with this span is a fractional number. Must include the number to be synthesized with `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_NUMERATOR:kotlin.String` and `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_DENOMINATOR:kotlin.String`. `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_INTEGER_PART:kotlin.String` is optional Also accepts the arguments `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_GENDER:kotlin.String`, `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_ANIMACY:kotlin.String`, `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_MULTIPLICITY:kotlin.String` and `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_CASE:kotlin.String`.

 Value: "android.type.fraction"

### TYPE_MEASURE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_MEASURE: String
```

The text associated with this span is a measure, consisting of a number and a unit. The number can be a cardinal, decimal or a fraction. Set the number with the same arguments as `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_CARDINAL:kotlin.String`, `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_DECIMAL:kotlin.String` or `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_FRACTION:kotlin.String`. The unit can be specified with `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_UNIT:kotlin.String`. Also accepts the arguments `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_GENDER:kotlin.String`, `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_ANIMACY:kotlin.String`, `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_MULTIPLICITY:kotlin.String` and `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_CASE:kotlin.String`.

 Value: "android.type.measure"

### TYPE_MONEY

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_MONEY: String
```

The text associated with this span is an amount of money. Set the amount with the same arguments as `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_DECIMAL:kotlin.String`. `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_CURRENCY:kotlin.String` is used to set the currency. `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_QUANTITY:kotlin.String` is optional. Also accepts the arguments `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_GENDER:kotlin.String`, `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_ANIMACY:kotlin.String`, `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_MULTIPLICITY:kotlin.String` and `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_CASE:kotlin.String`.

 Value: "android.type.money"

### TYPE_ORDINAL

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_ORDINAL: String
```

The text associated with this span is an ordinal. Must include the number to be synthesized with `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_NUMBER:kotlin.String`. Also accepts the arguments `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_GENDER:kotlin.String`, `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_ANIMACY:kotlin.String`, `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_MULTIPLICITY:kotlin.String` and `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_CASE:kotlin.String`.

 Value: "android.type.ordinal"

### TYPE_TELEPHONE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_TELEPHONE: String
```

The text associated with this span is a telephone number. The argument `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_NUMBER_PARTS:kotlin.String` is required. `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_COUNTRY_CODE:kotlin.String` and `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_EXTENSION:kotlin.String` are optional. Also accepts the arguments `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_GENDER:kotlin.String`, `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_ANIMACY:kotlin.String`, `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_MULTIPLICITY:kotlin.String` and `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_CASE:kotlin.String`.

 Value: "android.type.telephone"

### TYPE_TEXT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_TEXT: String
```

This span type can be used to add morphosyntactic features to the text it spans over, or synthesize a something else than the spanned text. Use the argument `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_TEXT:kotlin.String` to set a different text. Accepts the arguments `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_GENDER:kotlin.String`, `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_ANIMACY:kotlin.String`, `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_MULTIPLICITY:kotlin.String` and `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_CASE:kotlin.String`.

 Value: "android.type.text"

### TYPE_TIME

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_TIME: String
```

The text associated with this span is a time, consisting of a number of hours, minutes, and seconds specified with `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_HOURS:kotlin.String`, `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_MINUTES:kotlin.String`, and `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_SECONDS:kotlin.String`. Also accepts the arguments `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_GENDER:kotlin.String`, `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_ANIMACY:kotlin.String`, `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_MULTIPLICITY:kotlin.String` and `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_CASE:kotlin.String`. This is different from `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_DURATION:kotlin.String`. This should be used to convey a particular moment in time, such as a clock time, while `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#TYPE_DURATION:kotlin.String` should be used to convey an interval of time.

 Value: "android.type.time"

### TYPE_VERBATIM

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_VERBATIM: String
```

The text associated with this span is a series of characters that have to be read verbatim. The engine will attempt to read out any character like punctuation but excluding whitespace. `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_VERBATIM:kotlin.String` is required. Also accepts the arguments `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_GENDER:kotlin.String`, `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_ANIMACY:kotlin.String`, `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_MULTIPLICITY:kotlin.String` and `https://developer.android.com/reference/kotlin/android/text/style/TtsSpan#ARG_CASE:kotlin.String`.

 Value: "android.type.verbatim"

### WEEKDAY_FRIDAY

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WEEKDAY_FRIDAY: Int
```

 Value: 6

### WEEKDAY_MONDAY

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WEEKDAY_MONDAY: Int
```

 Value: 2

### WEEKDAY_SATURDAY

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WEEKDAY_SATURDAY: Int
```

 Value: 7

### WEEKDAY_SUNDAY

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WEEKDAY_SUNDAY: Int
```

 Value: 1

### WEEKDAY_THURSDAY

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WEEKDAY_THURSDAY: Int
```

 Value: 5

### WEEKDAY_TUESDAY

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WEEKDAY_TUESDAY: Int
```

 Value: 3

### WEEKDAY_WEDNESDAY

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WEEKDAY_WEDNESDAY: Int
```

 Value: 4

## Public constructors

### TtsSpan

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
TtsSpan(src: Parcel!)
```

### TtsSpan

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
TtsSpan(
    type: String!, 
    args: PersistableBundle!)
```

## Public methods

### describeContents

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getArgs

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getArgs(): PersistableBundle!
```

Returns a bundle of the arguments set.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#!` | The bundle of the arguments set. |

### getSpanTypeId

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSpanTypeId(): Int
```

Return a special type identifier for this span class.

### getType

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getType(): String!
```

Returns the type.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | The type of this instance. |

### writeToParcel

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | [Parcel](../android.os/Parcel.md): The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |
