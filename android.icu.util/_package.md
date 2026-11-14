# android.icu.util

# android.icu.util

Kotlin | [Java](_package.md)
| --- | --- |

## Interfaces

| [Freezable](Freezable.md) | Provides a flexible mechanism for controlling access, without requiring that a class be immutable. |
| --- | --- |
| [RangeValueIterator](RangeValueIterator.md) | Interface for enabling iteration over sets of \<int index, int value\>, where index is the sorted integer index in ascending order and value, its associated integer value. |
| [ValueIterator](ValueIterator.md) | Interface for enabling iteration over sets of \<int, Object\>, where int is the sorted integer index in ascending order, and Object its associated value. |

## Classes

| [BuddhistCalendar](BuddhistCalendar.md) | `BuddhistCalendar` is a subclass of `GregorianCalendar` that numbers years since the birth of the Buddha. |
| --- | --- |
| [Calendar](Calendar.md) | **\[icu enhancement\]** ICU's replacement for [java.util.Calendar](../java.util/Calendar.md). |
| [ChineseCalendar](ChineseCalendar.md) | `ChineseCalendar` is a concrete subclass of [Calendar](Calendar.md) that implements a traditional Chinese calendar. |
| [CopticCalendar](../android/icu/util/CopticCalendar.md) | Implement the Coptic calendar system. |
| --- | --- |
| [Currency](Currency.md) | A class encapsulating a currency, as defined by ISO 4217. |
| [CurrencyAmount](CurrencyAmount.md) | An amount of currency, consisting of a Number and a Currency. |
| [DateInterval](DateInterval.md) | This class represents date interval. |
| --- | --- |
| [EthiopicCalendar](../android/icu/util/EthiopicCalendar.md) | Implement the Ethiopic calendar system. |
| [GregorianCalendar](GregorianCalendar.md) | **\[icu enhancement\]** ICU's replacement for [java.util.GregorianCalendar](../java.util/GregorianCalendar.md). |
| [HebrewCalendar](HebrewCalendar.md) | `HebrewCalendar` is a subclass of `Calendar` that that implements the traditional Hebrew calendar. |
| --- | --- |
| [IndianCalendar](../android/icu/util/IndianCalendar.md) | `IndianCalendar` is a subclass of `GregorianCalendar` that numbers years since the birth of the Buddha. |
| [IslamicCalendar](IslamicCalendar.md) | `IslamicCalendar` is a subclass of `Calendar` that that implements the Islamic civil and religious calendars. |
| [JapaneseCalendar](JapaneseCalendar.md) | `JapaneseCalendar` is a subclass of `GregorianCalendar` that numbers years and eras based on the reigns of the Japanese emperors. |
| --- | --- |
| [LocaleData](LocaleData.md) | A class for accessing miscellaneous data in the locale bundles |
| [Measure](Measure.md) | An amount of a specified unit, consisting of a Number and a Unit. |
| [MeasureUnit](MeasureUnit.md) | A unit such as length, mass, volume, currency, etc. |
| --- | --- |
| [Output](Output.md) | Simple struct-like class for output parameters. |
| [TaiwanCalendar](TaiwanCalendar.md) | `TaiwanCalendar` is a subclass of `GregorianCalendar` that numbers years since 1912. |
| [TimeUnit](TimeUnit.md) | Measurement unit for time units. |
| --- | --- |
| [TimeZone](TimeZone.md) | **\[icu enhancement\]** ICU's replacement for [java.util.TimeZone](../java.util/TimeZone.md). |
| [ULocale](ULocale.md) | **\[icu enhancement\]** ICU's replacement for [java.util.Locale](../java.util/Locale.md). |
| [UniversalTimeScale](UniversalTimeScale.md) | There are quite a few different conventions for binary datetime, depending on different platforms and protocols. |
| --- | --- |
| [VersionInfo](VersionInfo.md) | Class to store version numbers of the form major. |

## Exceptions

| [ICUUncheckedIOException](ICUUncheckedIOException.md) | Unchecked version of [java.io.IOException](../java.io/IOException.md). |
| --- | --- |
| [IllformedLocaleException](IllformedLocaleException.md) | Thrown by methods in [ULocale](ULocale.md) and [ULocale.Builder](../android/icu/util/ULocale.Builder.md) to indicate that an argument is not a well-formed BCP 47 tag. |
